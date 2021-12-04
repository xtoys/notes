&nbsp;

<p align="center">
  <img src="../assets/linux.svg" width="20%" alt="linux" />
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
