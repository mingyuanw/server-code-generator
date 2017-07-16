# server-code-generate



给定一个数据库，自动生成后台代码(spring mvc/mybatis/jquery/bootstrap)，同时能够生成一个简单的后台对应的页面
<br/>
注：生成后的工程是用maven来管理，数据库中的表注释、列注释，都会体现到代码中，所以，在建表的时候，希望尽可能的有详尽的注释
<br/>
基本功能：<br/>

1.生成数据库对应的pojo<br/>

2.生成mybatis的mapper xml<br/>

3.生成dao层代码(放置在data包下，因为mybatis官方取名为data，所以，没有写成dao/mapper报名)<br/>

4.生成service层代码<br/>

5.生成controller层代码<br/>

6.生成登录界面<br/>

7.生成各模块的页面代码（增删查改，对于一般的管理后台稍微修改一下）<br/>

8.数据库、spring配置文件自动生成<br/>

src/main/resources/config.xml文件说明：<br/>
	a.author：作者名，可以是你自己的名字，也可以是你公司的名字<br/>
	b.dbDriver:数据库驱动，如果不是mysql，或者pom中的mysql版本不是你想要的，则需要修改pom.xml文件<br/>
	c.dbUrl/dbUser/dbPswd:数据库的url、用户名、密码，用于连接数据库<br/>
	d.projectPath：生成的代码的目标位置<br/>
	e.rootPackage:所有java代码存放在此包下<br/>
	f.tablePrefix:表前缀，一般是"tb_",比如：tb_this_table<br/>
	g.tableNameSeparator:数据库表名的分隔符，一般是"_",例如：tb_this_table<br/>
	h.colNameSeparator:列分隔符，一般是"_",比如：col_name<br/>
	i.includeTable:需要处理的表，如果只处理部分表，则可以在这里设置，多个表用逗号隔开，优先级低于excludeTable<br/>
	j.excludeTable:不处理的表，必须指定表名，不能是通配符"*"<br/>
	k.table:有些表需要做一些特殊的命名，则可以自定义对应的类名，同时也可以指定生成的目标包名<br/>
	
注：列暂不能自定义名称