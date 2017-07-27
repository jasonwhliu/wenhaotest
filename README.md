# wenhaotest

## 测试环境部署

### windows

依赖: winScp、SecureCRT，自行下载安装

### mac
notice：Mac 自带的终端是不支持lrzsz的，需要使用iterm2，并做一些配置，参考 http://blog.csdn.net/jack85986370/article/details/51382077
或者直接使用SecureCRT Mac版

### 一、构建代码，准备上传
	npm run build
	压缩dist.zip
### 二、连接机器

	ssh relay.xiaomi.com
	shell
	ssh work@c3-hadoop-staging-cloud01.bj
	// 密码找 @海洋 @文浩
	cd /home/work/cloud-manager/paas-ui

### 三、上传部署代码
	//使用rz命令 上传压缩好的dist.zip 
	rz
	// 覆盖解压dist.zip
	unzip -o dist.zip
	// 把dist里的所有文件 copy到paas-ui下
	cp -rf dist/* ./


