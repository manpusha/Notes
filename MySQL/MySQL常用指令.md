---
title: MySQL常用指令
tags: mysql
grammar_cjkRuby: true
---
	1. 启动mysql 命令行
		C:/>mysql -h hostname -u root -p root //连接远程服器
		C:/>mysql -u root -p root //连接localhost
		C:/>mysql -uroot -proot   //连接localhost
	2. 查看mysql的帮助
		c:/>mysql --help
	3. 查询当前日期和时间
		mysql>select current_date; //伪劣
		mysql>select now();         //函数
	4. 显示所有数据库
		mysql>-- 这是注释
		mysql>show databases;
	5. 删除数据库
		mysql>drop database myhive;
	6. 创建数据库
		mysql>create database mybase;
	7. 使用指定的数据库
		mysql>use mybase;
	8. 显示所有表
		mysql>show tables;
	9. 创建表
		mysql>create table test(id int,name varchar(20),age int);
	10. 查看表结构
		mysql>describe test;
		mysql>desc test;
	11. 查询表的数据  
		mysql>select * from test; //全字段 + 全表扫描
		mysql>select id,name,age from test; //投影查询 project
		mysql>select id,name,age from test where id > 3 and id < 5      //ang类似于java中的&&
		mysql>select id,name,age from test where id > 3 or id < 5 
		mysql>select id,name,age from test where name = 'tom';      
		mysql>select id,name,age from test where name like 't%';      //模糊查询
		mysql>select id,name,age from test where name  not like 't%';   //模糊查询
		mysql>select id,name,age from test where name  not like 't\_%';   //使用转义符查询特殊字面量
		mysql>select id,name,age from test where name is null;  //null查询
		mysql>select id,name,age from test where name is not null;  //非null查询
		mysql>select id,name,age from test order by  id desc,name asc;
			//降序排序
		mysql>select id,name,age from test order by id asc;
			//升序排序
			
		mysql>select * from test limit 1,3; //分页查询
		mysql>select * from test limit 3; //分页查询
		
		聚集函数查询
		mysql>select count(*) from test; count,//查询记录总数
		mysql>select max(age) from test;    //最大值
		mysql>select min(age) from test;    // 最小值
		mysql>select avg(*) from test;     //平均值
		mysql>select sum(age) from test;   //求总和
		
	12. 插入数据
		mysql>insert into test(id,name,age) values(1,'tom',23);
		mysql>insert into test(id,name) values(4,'tom');
	13. 更新数据
		mysql>update test set name='xxx',age = 33 where id=12;   //更新id为12的记录
		mysql>update test set name='xxx',age = 33; //更新所有记录
	14. 删除数据
		mysql>delete from test where id = 1;
	15. CRUD
		[create]
		insert into table_name(field_name,…) value(value,…);
		
		[retrieve]
		select id,… from table_name where id = xxx , ..;
		
		[delete]
		delete from test where…
	16. 使用mysql命令执行sql脚本
		mysql>source d:/java/select.sql
	17. 对表重命名
		alter table test3 rename persons;
	18. 修改表,添加列
		alter table persons add column password varchar(20);
![enter description here][1]


  [1]: https://www.github.com/manpusha/githubimg/raw/master/images/1502463352504.jpg