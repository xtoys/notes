&nbsp;

<p align="center">
  <img src="../assets/linux.svg" width="33%" alt="linux" />
</p>

&nbsp;

### 设置国内镜像软件源

```bash
# Alpine
sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories

# Debian
sudo sed -i 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list

# Ubuntu
sudo sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
```

### 设置系统时区

```bash
sudo timedatectl set-timezone Asia/Shanghai
```

### 设置终端代理

> 假设代理地址是 `127.0.0.1:7890`

```bash
# 设置代理
set http_proxy=http://127.0.0.1:7890
set https_proxy=http://127.0.0.1:7890

# 查看代理
echo $http_proxy
echo $https_proxy

# 取消代理
set http_proxy=
set https_proxy=
```

> 若无代理服务 可使用开源工具 [dev-sidecar](https://github.com/docmirror/dev-sidecar) 进行代理
