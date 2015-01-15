# BMS
基于PHP+SqlServer的图书管理系统

这是“数据库实用技术”课程的大作业，设计一个图书管理系统（Book Management System）。

其实PHP和SqlServer配合使用并不方便，效率也不高。

但是老师要求使用SqlServer数据库我又比较擅长PHP，所以我就用PHP和SqlServer编写的。

用PHP连接SqlServer数据库可以参考文档：PHP连接SQL SERVER 2005与2008的配置.doc

系统功能演示地址：http://v.youku.com/v_show/id_XNzMxNTE1NjUy.html

院校：山东师范大学

使用教材：《SQL Server2008应用实践教程》 

教材下载地址：http://www.jb51.net/books/110857.html

作业就是教材后面的应用实例”图书管理系统“，该作业占课程总成绩的30%~40%



读者的权限比较低，只能查询图书，查看个人信息，以及自己的图书借阅信息。

如果，读者需要借书或着还书，则需要管理员进行操作。

管理员在得知读者的借书证号，以及图书ISBN和id之后，才可以完成借书和还书的操作。

在实际的操作中，读者将借书卡放到感应区之后，相关硬件就可以识别出器借书证号，然后读者挑选好图书之后，管理员通过扫描条形码可以识别出图书的ISBN和ID，也就是说管理员获得借书证号和图书的ISBN以及图书ID的过程都是由硬件完成的。


读者信息放到TReader表中

管理员信息放到Administrator表中

图书信息使用两个表来存储：

TBook用于存储每个书的具体信息

因为每个书都可能有好多本，所以TBlend用于存储所有的图书ID以及借出状态


读者和图书的借阅关系通过两个表分别表示：

图书------>读者：使用TLend表存储读者借书信息

读者------>图书：使用HLend表存储读者还书信息




