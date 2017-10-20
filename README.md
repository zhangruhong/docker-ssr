# docker-ssr

## 使用方法

0x1: 直接使用
```
docker pull starriv/shadowsocksr
docker run starriv/shadowsocksr:latest -name shadowsocksr -p 50080:50080
```

0x2: 从当前项目构建(docker-native)
```
git clone https://github.com/starriv/docker-ssr.git
cd docker-ssr
修改 Dockerfile 参数
docker build -t shadowsocksr:latest .
sudo docker run -d --name shadowsocksr -p 本地端口:容器端口

```

0x3: 使用 docker-compose
```
git clone https://github.com/starriv/docker-ssr.git
cd docker-ssr
修改 .env 参数
docker-compose up -d --build

```


https://hub.docker.com/r/starriv/shadowsocksr/
源码:
https://github.com/starriv/docker-ssr.git

默认参数：

SSR 服务端开放端口

SSR_SERVER_PORT=50080

SSR 密码

SSR_PASSWORD=1q2w3e4r

SSR 加密方法

SSR_METHOD=aes-128-cfb

SSR 混淆方法

SSR_PROTOCOL=auth_aes128_md5

SSR 混淆参数

SSR_OBFS=tls1.2_ticket_auth_compatible

使用方法

docker pull starriv/shadowsocksr
docker run starriv/shadowsocksr:latest -name shadowsocksr -p 50080:50080
