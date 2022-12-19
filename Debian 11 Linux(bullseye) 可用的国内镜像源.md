
[原文链接](https://www.zzxworld.com/posts/available-cn-mirrors-for-debian-linux)

![Debian 11 Linux(bullseye) 可用的国内镜像源](https://www.zzxworld.com/resource/posts/202208/1661740805.577.jpg)

Debian 默认的软件源在国外，使用默认源安装软件速度感人，浪费大量不必要的等待时间。所以在安装完 Deiban 系统后的首要事情就是更换为国内的镜像源，能显著提高软件安装和系统更新速度。本文收集了 8 个能用的 Debian 国内镜像源以供选择。

> 如果不熟悉 Debian 镜像源的使用和配置，请直接翻到最后。文末提供了手动和命令式的两种镜像源配置方式。

## 可用的国内源

由阿里云提供的 Debian 镜像源：

```text
deb https://mirrors.aliyun.com/debian/ bullseye main non-free contrib
deb-src https://mirrors.aliyun.com/debian/ bullseye main non-free contrib
deb https://mirrors.aliyun.com/debian-security/ bullseye-security main
deb-src https://mirrors.aliyun.com/debian-security/ bullseye-security main
deb https://mirrors.aliyun.com/debian/ bullseye-updates main non-free contrib
deb-src https://mirrors.aliyun.com/debian/ bullseye-updates main non-free contrib
deb https://mirrors.aliyun.com/debian/ bullseye-backports main non-free contrib
deb-src https://mirrors.aliyun.com/debian/ bullseye-backports main non-free contrib
```

由腾讯提供的 Debian 镜像源：

```text
deb https://mirrors.tencent.com/debian/ bullseye main non-free contrib
deb-src https://mirrors.tencent.com/debian/ bullseye main non-free contrib
deb https://mirrors.tencent.com/debian-security/ bullseye-security main
deb-src https://mirrors.tencent.com/debian-security/ bullseye-security main
deb https://mirrors.tencent.com/debian/ bullseye-updates main non-free contrib
deb-src https://mirrors.tencent.com/debian/ bullseye-updates main non-free contrib
deb https://mirrors.tencent.com/debian/ bullseye-backports main non-free contrib
deb-src https://mirrors.tencent.com/debian/ bullseye-backports main non-free contrib
```

由北京清华大学提供的 Debian 镜像源：

```text
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye main contrib non-free
deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye main contrib non-free
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-updates main contrib non-free
deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-updates main contrib non-free
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-backports main contrib non-free
deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-backports main contrib non-free
deb https://mirrors.tuna.tsinghua.edu.cn/debian-security bullseye-security main contrib non-free
deb-src https://mirrors.tuna.tsinghua.edu.cn/debian-security bullseye-security main contrib non-free
```

由中国科学技术大学提供的 Debian 镜像源：

```text
deb http://mirrors.ustc.edu.cn/debian bullseye main contrib non-free
deb-src http://mirrors.ustc.edu.cn/debian bullseye main contrib non-free
deb http://mirrors.ustc.edu.cn/debian bullseye-updates main contrib non-free
deb-src http://mirrors.ustc.edu.cn/debian bullseye-updates main contrib non-free
deb http://mirrors.ustc.edu.cn/debian bullseye-proposed-updates main contrib non-free
deb-src http://mirrors.ustc.edu.cn/debian bullseye-proposed-updates main contrib non-free
```

由上海交通大学提供的 Debian 镜像源：

```text
deb http://mirrors.sjtu.edu.cn/debian bullseye main contrib non-free
deb-src http://mirrors.sjtu.edu.cn/debian bullseye main contrib non-free
deb http://mirrors.sjtu.edu.cn/debian bullseye-updates main contrib non-free
deb-src http://mirrors.sjtu.edu.cn/debian bullseye-updates main contrib non-free
deb http://mirrors.sjtu.edu.cn/debian bullseye-proposed-updates main contrib non-free
deb-src http://mirrors.sjtu.edu.cn/debian bullseye-proposed-updates main contrib non-free
```

由北京外国语大学提供的 Debian 镜像源：

```text
deb https://mirrors.bfsu.edu.cn/debian/ bullseye main contrib non-free
deb-src https://mirrors.bfsu.edu.cn/debian/ bullseye main contrib non-free
deb https://mirrors.bfsu.edu.cn/debian/ bullseye-updates main contrib non-free
deb-src https://mirrors.bfsu.edu.cn/debian/ bullseye-updates main contrib non-free
deb https://mirrors.bfsu.edu.cn/debian/ bullseye-backports main contrib non-free
deb-src https://mirrors.bfsu.edu.cn/debian/ bullseye-backports main contrib non-free
deb https://mirrors.bfsu.edu.cn/debian-security bullseye-security main contrib non-free
deb-src https://mirrors.bfsu.edu.cn/debian-security bullseye-security main contrib non-free
```

由华为提供的 Deiban 镜像源：

```text
deb https://mirrors.huaweicloud.com/debian/ bullseye main non-free contrib
deb-src https://mirrors.huaweicloud.com/debian/ bullseye main non-free contrib
deb https://mirrors.huaweicloud.com/debian-security/ bullseye-security main
deb-src https://mirrors.huaweicloud.com/debian-security/ bullseye-security main
deb https://mirrors.huaweicloud.com/debian/ bullseye-updates main non-free contrib
deb-src https://mirrors.huaweicloud.com/debian/ bullseye-updates main non-free contrib
deb https://mirrors.huaweicloud.com/debian/ bullseye-backports main non-free contrib
deb-src https://mirrors.huaweicloud.com/debian/ bullseye-backports main non-free contrib
```

由网易提供的 Debian 镜像源：

```text
deb https://mirrors.163.com/debian/ bullseye main non-free contrib
deb-src https://mirrors.163.com/debian/ bullseye main non-free contrib
deb https://mirrors.163.com/debian-security/ bullseye-security main
deb-src https://mirrors.163.com/debian-security/ bullseye-security main
deb https://mirrors.163.com/debian/ bullseye-updates main non-free contrib
deb-src https://mirrors.163.com/debian/ bullseye-updates main non-free contrib
deb https://mirrors.163.com/debian/ bullseye-backports main non-free contrib
deb-src https://mirrors.163.com/debian/ bullseye-backports main non-free contrib
```

## 手动更换镜像源

手动更换 Debian 镜像源配置主要分为以下三步：

1.  用熟悉的文本编辑器打开 `/etc/apt/sources.list` 文件（需要 `sudo` 权限），或是直接执行 `sudo apt edit-sources` 命令。
2.  替换文件内容为上面任意一个镜像站的源配置代码并保存。
3.  运行 `sudo apt-get update` 命令更新软件索引。

## 命令更换镜像源

使用命令替换镜像源更为快捷。比如在没有更换过数据源的情况下，要使用阿里云的 Debian 镜像源：

```shell
sudo sed -i 's/deb.debian.org/mirrors.aliyun.com/g' /etc/apt/sources.list
```

这样就完成了默认源到阿里云镜像源的配置。接下来同样需要执行一下 `sudo apt-get update` 命令更新软件索引。

上面这个命令的原理在镜像源的地址上。不同的镜像源通常只是域名有所区别，其他部分大致类似。所以之需要通过 `sed` 命令来修改 `/etc/apt/sources.list` 这个源配置文件中的域名地址就足够了。

但这意味着使用这个命令方式修改镜像源的配置时需要格外注意。如果输入的匹配地址或替换地址有误，有可能不会生效，或是导致镜像源异常。遇到这种情况，可以选择上面手动更换镜像源的方式来解决。