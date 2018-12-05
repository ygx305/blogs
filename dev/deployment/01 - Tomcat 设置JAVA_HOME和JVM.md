# Tomcat 设置JAVA_HOME和JVM


## Windows 环境
Windows 下 Tomcat 的启动有两种方式，根据不同的启动方式，需要分别进行配置。

### startup.bat 启动
修改 catalina.bat 文件，找到 setlocal 后，添加以下命令：

```bash
SET JAVA_HOME=C:\Program Files\Java\jdk1.8.0_144
SET JAVA_OPTS=-Xms512m -Xmx512m
```

还可以设置cmd窗口标题

```bash
SET TITLE=tomcat8-jdk7
```

### service 启动
修改 service.bat 文件，找到 setlocal 后，添加以下命令（切记先修改文件，再执行服务添加命令）：

```bash
SET JAVA_HOME=C:\Program Files\Java\jdk1.8.0_144
SET JAVA_OPTS=-Xms512m -Xmx512m
```

## Linux 环境
修改 catalina.sh 配置文件，在文件最上方添加以下命令。

```bash
JAVA_HOME=/usr/local/lib/jdk1.8.0_121
JAVA_OPTS="-Xms2048m -Xmx2048m -Duser.timezone=GMT+08"
```

