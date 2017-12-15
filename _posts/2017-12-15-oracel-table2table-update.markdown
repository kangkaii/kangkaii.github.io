---
layout: post
title:  "Oracle中 如何用一个表的数据更新另一个表中的数据!"
date:   2017-12-15 17:19:54
categories: start
tags: start 
excerpt: 各种方式的尝试！
mathjax: true
---

#####建表语句：
create table table1(  
idd varchar2(10) ,  
val varchar2(20)  
); 
create table table2(  
idd varchar2(10),  
val varchar2(20)  
);
#####插入数据：
insert into table1 values ('01','1111');
insert into table1 values ('02','222');  
insert into table1 values ('02','2222');    
insert into table1 values ('03','3333');  
insert into table1 values ('04','4444');
insert into table1 values ('06','6666');
commit;  
insert into table2 values ('01','aaaa');
insert into table2 values ('02','bbbb');      
insert into table2 values ('03','cccc'); 
insert into table2 values ('04','dddd');
insert into table2 values ('05','eee');
insert into table2 values ('05','eeee');
commit; 
######2表如下：
![image.png](http://upload-images.jianshu.io/upload_images/5625942-c3e0c83e4cf2aa44.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![image.png](http://upload-images.jianshu.io/upload_images/5625942-778f11f0f5be1e4c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



######要将 table2中idd - val 的值，赋值给table1对应的 idd - val；
 注意：
 - table1中 有 2个 idd 为 02，val 不同；
 - table2中 有 05，table1中没有；
 - table1中 有 06，table2中没有。

sql语句：
 1. 通过子查询 ，直接 update 更新，如下：
update table1 set table1.val = (select val from table2 where table1.idd = table2.idd);
![image.png](http://upload-images.jianshu.io/upload_images/5625942-05b6dd4696c8ccfa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
 - 问题：对于 table1中idd存在，table2中不存在，val变成了null；
 2. 改进，加入限制条件，对于 table1 中有，但是table2中不存在的idd，不做修改；
update table1 set val = (select val from table2 where table1.idd = table2.idd)
where exists (select 1 from table2 where table1.idd = table2.idd)
![image.png](http://upload-images.jianshu.io/upload_images/5625942-3f3577aee29adfca.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
 - 但上述2种写法，遇到table2中继续插入数据，
insert into table2 values ('03','ccc'); 
即table2 中有一个idd对应多个val，并且在table1中有对应idd时。
 - 执行后会报错：
[ORA-01427:单行子查询返回多个行](http://blog.csdn.net/u010097777/article/details/52613600)
![image.png](http://upload-images.jianshu.io/upload_images/5625942-d7d4339e81feb0ec.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
3. 使用merge，如下：
merge into table1
using  table2
on (table1.idd = table2.idd)
when matched then
update set table1.val = table2.val
 - 遇到 table2 中有一个idd对应多个val，并且在table1中有对应idd时，报错如下：
![image.png](http://upload-images.jianshu.io/upload_images/5625942-9d68ee00361f76ae.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
[ORA-30926: 无法在源表中获得一组稳定的行](http://blog.csdn.net/ytfy12/article/details/52488797)
4. 在3的基础上，加入限制条件；
merge into table1
using  (select t.idd ,max(t.val) m from table2 t group by t.idd)table2
on (table1.idd = table2.idd)
when matched then
update set table1.val = table2.m
 - 上述写法在 using后面构造了一个新的table2，group by idd，但一定要对val做出处理，如果是varchar类型，可以选择 max，min等函数，如果number类型，可以使用sum，avg等函数，总之，要对val做出筛选，新的table2是一个idd对应一个val。

参考：[Oracle中用一个表的数据更新另一个表的数据](http://blog.csdn.net/kkdelta/article/details/7535027)








