# wenhaotest

## 测试环境部署
https://cloud-staging.d.xiaomi.net/#/services

### Windows

依赖: winScp、SecureCRT，自行下载安装

### Mac
notice：Mac 自带的终端是不支持lrzsz的，需要使用iterm2，并做一些配置，参考 http://blog.csdn.net/jack85986370/article/details/51382077
或者直接使用SecureCRT Mac版

### 一、构建代码，准备上传
	npm run build
	压缩dist.zip
### 二、连接机器
	// 连接通道机
	ssh relay.xiaomi.com
	// 输入shell进入bash
	shell
	// 进行hd登录 密码找 @海洋 或 @文浩
	ssh work@c3-hadoop-staging-cloud01.bj
	// 项目path
	cd /home/work/cloud-manager/paas-ui

### 三、上传部署代码
	//使用rz命令 上传构建好的dist.zip 
	rz
	// 解压dist.zip  覆盖dist
	unzip -o dist.zip
	// 把dist里的所有文件 copy到paas-ui下
	cp -rf dist/* ./

## 线上环境部署
https://cloud-platform.d.xiaomi.net/#/services

### 一、构建代码，准备上传
	npm run build
	压缩dist.zip
### 二、连接机器
	// 连接通道机
	ssh relay.xiaomi.com
	// 输入主机名，回车即可登录  有两台主机。 权限开通须通知@海洋 找@刘亚运 开通
	c3-hadoop-cloud01.bj
	c3-hadoop-cloud02.bj
	// 项目path
	cd /home/work/cloud-manager/paas-ui

### 三、上传部署代码
	//使用rz命令 上传构建好的dist.zip 
	rz
	// 解压dist.zip  覆盖dist
	unzip -o dist.zip
	// 把dist里的所有文件 copy到paas-ui下
	cp -rf dist/* ./

