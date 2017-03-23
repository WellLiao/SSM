# Spring-SpringMVC-MyBatis
Spring+SpringMVC+MyBatis整合


使用Intellij IDEA整合SSM，具体环境如下：

数据库：MySQL5.7
依赖管理：Maven
IDE：Intellij IDEA
JDK：1.8
服务器：Tomcat 9

1.创建表，插入数据
CREATE TABLE user (
  id       INTEGER PRIMARY KEY AUTO_INCREMENT,
  name     CHAR(20) NOT NULL,
  password CHAR(40) NOT NULL
)
  ENGINE = InnoDB
  AUTO_INCREMENT = 16
  DEFAULT CHARSET = utf8;
  
  INSERT INTO user (id,name, password) VALUES (1,'A', '123');
  INSERT INTO user (id,name, password) VALUES (2,'B', '456');
  
2.测试

将项目部署到本地的Tomcat上，打开你的chrome，访问：
http://localhost:8080/user/1
浏览器访问服务器，服务器成功返回一个json数据
{
"id": 1,
"name": "A",
"password": "123"
}
