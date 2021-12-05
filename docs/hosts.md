&nbsp;

<p align="center">
  <img src="../assets/hosts.svg" width="20%" alt="hosts" />
</p>

&nbsp;

## Github Hosts

#### 主要解决的痛点问题

- GitHub 访问速度慢的问题
- GitHub 项目中的图片显示不出的问题

#### 通过 SwitchHosts 自动更新

> 一个管理 hosts 文件的应用
>
> **`客户端`** [SwitchHosts](https://github.com/oldj/SwitchHosts/releases)
>
> ```ini
> # 若下载慢速或无法下载可使用 [文件代理加速下载服务]
> # 在下载链接前加上 https://ghproxy.com/
> https://ghproxy.com/https://github.com/oldj/SwitchHosts/releases/download/v4.0.3/SwitchHosts_installer_4.0.3.6070.exe
> ```

- 手动配置

  > 添加一条`hosts`规则并启用，然后复制前文`hosts`内容即可
  >
  > 如果你想保持和云端最新规则同步，可以用下面的配置方式

- 定时同步

  > 点击左上角 `➕` 添加一条规则：
  >
  > - 方案名：GitHub（可以自行命名）
  > - 类型：远程
  > - URL 地址：https://gitee.com/ineo6/hosts/raw/master/hosts
  > - 自动更新：1 个小时

  > 点击右上角 `设置` 按钮：
  >
  > `选项` > `命令`
  >
  > ```ini
  > # Windows
  > ipconfig /flushdns
  > ```
  >
  > ```ini
  > # macOS <替换123456为你电脑登陆密码>
  > echo 123456 | sudo -S killall -HUP mDNSResponder
  > ```

- 注意事项

  > **不要忘记点击侧边栏的开关哦**
  >
  > 若 Windows 下修改 hosts 文件提示 `只读 不能修改`
  >
  > - 首先打开 hosts 文件所在的位置，路径是在：`C:\Windows\System32\drivers\etc`
  > - 右键点击 hosts 文件，在打开的菜单项中，选择 `属性`
  > - hosts 属性窗口中，切换到 `安全` 选项卡，选中 `Users(xxxx)` ，点击 `编辑`
  > - hosts 的权限窗口，将用户的 `完全控制` 选中，点击 `应用`
  > - 最后别忘记点击 `确认` 保存
