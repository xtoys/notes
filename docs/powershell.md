![preview](../assets/terminal.png)

&nbsp;

## 终端配置主题

### 工具安装

- [Scoop 安装与使用指南](./scoop.md)

- [Windows Terminal 安装](https://www.microsoft.com/zh-cn/p/windows-terminal/9n0dx20hk701)
- [Git 官网](https://git-scm.com/downloads) | [posh-git 使用指南](http://dahlbyk.github.io/posh-git/) | [oh-my-posh 使用指南](https://ohmyposh.dev/docs/)

```powershell
# 添加软件源 功能依赖于 git，请确保电脑中已经安装 git
# 未安装可运行此条命令执行安装 scoop install git
scoop bucket add extras

# 工具安装
scoop install posh-git
scoop install oh-my-posh3
```

### 主题配置

```powershell
# 打开配置
notepad $profile

# 在记事本中输入如下内容，xtoys为主题名
Invoke-Expression (oh-my-posh --init --shell pwsh --config "$(scoop prefix oh-my-posh3)/themes/xtoys.omp.json")
# 更多主题 https://ohmyposh.dev/docs/themes

# 刷新当前主题
. $profile
```

```powershell
# powerline 字体可以通过在 scoop 里增加 nerd-fonts bucket 安装 nerd-fonts 来支持
# 比如说使用有 powerline 补丁的 hack 字体，powershell 原生的 terminal 不支持这些字体，所以请安装其他的终端模拟器来使用，比如 windows terminal
scoop bucket add nerd-fonts
scoop install Hack-NF
```

> 我的 windows terminal 主题颜色配置

```json
{
  "background": "#FFFFFF",
  "black": "#0C0C0C",
  "blue": "#0037DA",
  "brightBlack": "#000000",
  "brightBlue": "#4271AE",
  "brightCyan": "#61D6D6",
  "brightGreen": "#718C00",
  "brightPurple": "#8959A8",
  "brightRed": "#C8282B",
  "brightWhite": "#A4B4F2",
  "brightYellow": "#EAB700",
  "cursorColor": "#4D4D4C",
  "cyan": "#3A96DD",
  "foreground": "#4D4D4C",
  "green": "#13A10E",
  "name": "Tomorrow",
  "purple": "#881798",
  "red": "#C50F1F",
  "selectionBackground": "#D9D9D9",
  "white": "#CCCCCC",
  "yellow": "#C19C00"
}
```
