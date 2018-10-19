
### 一、官方安装说明
- https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/

### 二、操作系统

 - Zesty 17.04
 - Xenial 16.04 (LTS)
 - Trusty 14.04 (LTS)

**注意：**	
 - 安装前确定系统没有装docker
 - 14.04安装前需执行以下命令 
```
sudo apt-get update
```

```
sudo apt-get install \
    linux-image-extra-$(uname -r) \
    linux-image-extra-virtual
```
### 三、安装步骤
 1. 更新apt包
```
sudo apt-get update
```
 2. 设置安装包以允许APT在HTTPS上使用存储库
```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
```
 3. 添加Docker的GPG密钥

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

 4. 验证密钥
```
sudo apt-key fingerprint 0EBFCD88
```
5. 下载相关docker包

```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```
6.再次更新apt包
```
sudo apt-get update
```
7.查看可安装的docker版本包

```
apt-cache madison docker-ce
```
![](https://img-blog.csdn.net/20181017143309143?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzM5NzMyNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
8.安装指定版本docker

```
sudo apt-get install docker-ce=17.09.0~ce-0~ubuntu-xenial
```
9.安装完毕

```
docker -version
```
![在这里插入图片描述](https://img-blog.csdn.net/20181017143213989?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzM5NzMyNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

