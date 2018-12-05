# Tomcat 添加删除 windows 服务

### 设置服务名称

修改 service.bat 文件，找到`Set default Service name`，在下方添加如下命令

```bash
SET SERVICE_NAME=Tomcat8-jdk7
```


### 添加服务

```bash
# bin 路径下执行
service.bat install
```

### 删除服务

```bash
# bin 路径下执行
services.bat remove
```