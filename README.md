## MongoDB副本集Docker本地测试环境部署

## 说明

通过Docker快速的在本地部署MongoDB副本集开发环境；

副本集中有两个节点

### 支持的环境

* Linux
* Windows（已验证）
* MacOs

### 部署前准备

将环境中的**MONGO_HOST**改成你的主机地址

```json
#数据库地址;在windows和macOs下不能是127.0.0.1或localhost
MONGO_HOST=192.168.1.115
```

### 如何部署

```shell
docker-compose up
```

### 如何连接

#### 通过shell连接

```shell
mongo "mongodb://root:123456@127.0.0.1:17018,127.0.0.1:17017/?authSource=admin&replicaSet=rs0&readPreference=primary"
```

![image-20210201114246053](./img/winConnected)

#### 通过MongoDB Compass连接

![image-20210201114125325](./img/mongoDbCompass)

![image-20210201114356115](./img/mongoDbCompassConnected)
