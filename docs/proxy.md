&nbsp;

<p align="center">
  <img src="../assets/proxy.svg" width="20%" alt="proxy" />
</p>

&nbsp;

## 配置系统代理

### 🍪 Clash for windows

> Clash 的 Windows/macOS 图形客户端
>
> **`客户端`** [原版](https://github.com/Fndroid/clash_for_windows_pkg/releases) | [汉化](https://github.com/ender-zhao/Clash-for-Windows_Chinese/releases)

- 获取配置文件

  > - 免费订阅
  >
  >   ```ini
  >   # 可临时解决科学上网环境问题，但这并不意味着能长期使用
  >   https://raw.fastgit.org/alanbobs999/TopFreeProxies/master/Eternity.yml
  >   ```
  >
  > - 付费订阅
  >
  >   [自用机场](https://miaona.xyz/#/register?code=WTY6zBdn) | [机场导航](https://52.mk/) `需科学上网环境才能访问`

- 导入配置文件

  > - URL 导入
  >
  >   左侧菜单 `Profiles`，在顶部输入框填入 `URL` 并点击 `Download`，下载完成后点击对应的配置文件即可载入
  >
  > - 本地文件拖拽导入
  >
  >   如果无法通过 `URL` 下载配置文件，则可以尝试在浏览器中下载配置文件后通过拖拽方式导入

- 打开系统代理及开机自启选项

  > 左侧菜单 `General`，打开 `System Proxy` 及 `Starts with Windows` 两个开关
  >
  > 左侧菜单 `Settings`，打开 `General` 下的 `Silent Start` 开关

&nbsp;

## 配置终端代理

> 通过终端访问 github 等国外网站的速度感人，因此需要为终端设置代理来提高速度
>
> Clash 代理地址是 `127.0.0.1:7890`

- Windows (Run as Administrator)

```powershell
# 设置代理
netsh winhttp set proxy 127.0.0.1:7890

# 查看代理
netsh winhttp show proxy

# 取消代理
netsh winhttp reset proxy
```

- Linux

```bash
# 设置代理
set http_proxy=http://127.0.0.1:7890
set https_proxy=$http_proxy

# 查看代理
echo $http_proxy

# 取消代理
set http_proxy=
```

- Git

```bash
# 设置代理
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890

# 查看代理
git config --global --get http.proxy
git config --global --get https.proxy

# 取消代理
git config --global --unset http.proxy
git config --global --unset https.proxy
```
