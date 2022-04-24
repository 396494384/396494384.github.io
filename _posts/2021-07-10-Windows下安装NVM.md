---
layout: post
title: "windows下安装nvm"
date: 2021-07-10
excerpt: "node版本管理工具nvm的安装和使用"
tags: [nvm, node]
comments: true
---

在windows下安装node版本管理工具nvm的步骤和使用方法。  

- ### 卸载node
  如果你已经安装了node，那么你需要先卸载node，如果你没有安装那直接跳过这一步到下一步。
- ### 下载安装nvm
  下载[nvm-windows](https://github.com/coreybutler/nvm-windows/releases)最新安装包，直接安装即可。  
 
  nvm-noinstall.zip： 这个是绿色免安装版本，但是使用之前需要配置  
  nvm-setup.zip：这是一个安装包，下载之后点击安装，无需配置就可以使用，方便。  
  Source code(zip)：zip压缩的源码  
  Sourc code(tar.gz)：tar.gz的源码，一般用于Linux系统    
  下载nvm-setup安装包：    
![下载nvm-setup](https://img-blog.csdnimg.cn/623d26a9b233405289a20da513a37887.png)
  点击下载即可。  

- ### 安装
  安装nvm-setup.zip  
  安装过程比较简单，注意选择的安装目录不能有空格符。    
  安装完成后在命令窗口输入nvm v 查看安装版本，能正确显示版本号，便说明已经成功安装。  
- ### 使用
  1. nvm list 命令 - 显示版本列表
```
nvm list // 显示已安装的版本（同 nvm list installed）
nvm list installed // 显示已安装的版本
nvm list available // 显示所有可以下载的版本
```
  2. nvm install 命令 - 安装指定版本node
```
nvm install 10.16.2 // 安装10.16.2版本node
nvm install latest // 安装最新版本node
```
  3. nvm use 命令 - 切换node版本
```
nvm use 10.16.2 // 使用10.16.2版本node
```
  4. nvm uninstall 命令 - 卸载指定版本node
```
nvm uninstall 10.16.2 // 卸载10.16.2版本node
```
  5. 其他命令  
```
//显示node是运行在32位还是64位系统上
nvm arch 

//开启/关闭nodejs版本管理
nvm on/off

//设置下载代理。不加可选参数url，显示当前代理。将url设置为none则移除代理
nvm proxy [url]

//设置node镜像
nvm node_mirror [url]

//设置存储不同版本node的目录。如果未设置，默认使用当前目录
nvm root [path]
```

- ### 在使用nvm中注意事项
  1. 在用命令工具使用nvm时，最好是选择以管理员身份运行命令工具  