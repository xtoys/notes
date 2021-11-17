&nbsp;

<p align="center">
  <img src="../assets/esxi.svg" width="20%" alt="esxi" />
</p>

&nbsp;

- 解决 esxi 7.0 虚拟内存问题

> u 盘引导成功 倒数读秒时 按下 **`shift + o`**
>
> 在 **`cdromBoot runweasel`** 这一串字符串后 **`追加空格`** 并输入以下代码
>
> ```sh
> autoPartitionOSDataSize=8192
> ```
