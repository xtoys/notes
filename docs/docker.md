&nbsp;

<p align="center">
  <img src="../assets/docker.svg" width="25%" alt="docker" />
</p>

&nbsp;

> 安装 Docker
>
> 一种开源容器化技术，用于构建和容器化您的应用程序

```bash
curl -sSL https://get.daocloud.io/docker | sh
```

> 安装 Docker Compose
>
> 用于定义和运行多容器 Docker 应用程序的工具

```bash
# 可以通过修改URL中的版本，可以自定义您的需要的版本
curl -L https://get.daocloud.io/docker/compose/releases/download/v2.1.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose

# 授予执行权限
chmod +x /usr/local/bin/docker-compose
```

> 配置 Docker 镜像站
>
> 提升拉取镜像的速度和体验

```bash
curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s https://registry.hub.docker.com

# 重启 docker
systemctl restart docker
```

> 卸载 Docker

```bash
sudo apt-get remove docker docker-engine

# 卸载Docker后,/var/lib/docker/目录下会保留原Docker的镜像,网络,存储卷等文件. 如果需要全新安装Docker,需要删除/var/lib/docker/目录
rm -fr /var/lib/docker/
```
