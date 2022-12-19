## 1、下载最新版
`[https://github.com/Dreamacro/clash/releases](https://github.com/Dreamacro/clash/releases)`

## 2、解压缩

## 3、授予可执行权限

`
chmod +x clash`

## 4、初始化

`./clash`

初始化执行 clash 会默认在 ~/.config/clash/ 目录下生成配置文件和全球IP地址库：config.yaml 和 Country.mmdb。

## 5、配置config.yaml

没找到自动下载订阅的方式，只能采取笨方法，从clash for windows 中导出配置，粘贴到~/.config/clash/ 目录下的config.yaml

## 6、运行，可添加守护进程

这样就不用一直打开一个terminal了。

`./clash &`

7、配置系统代理

找到网络-代理设置-手动
`http 127.0.0.1:7890`
`socks 127.0.0.1:7890`

socks端口存疑，也可能是7891。

8、网页管理（震惊）

`http://clash.razord.top/#/proxies`

不知道是否安全