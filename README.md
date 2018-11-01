# docker_stuff

>常规情况下 ubnutu14.04 如何离线安装docker

```
## 下载依赖和安装包
wget https://apt.dockerproject.org/repo/pool/main/d/docker-engine/docker-engine_17.05.0~ce-0~ubuntu-trusty_amd64.deb
wget http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libltdl7_2.4.6-0.1_amd64.deb
wget http://archive.ubuntu.com/ubuntu/pool/universe/libg/libgcrypt20/libgcrypt20_1.6.1-2ubuntu1_amd64.deb
wget http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/libsystemd-journal0_204-5ubuntu20_amd64.deb

## 安装
dpkg -i *.deb

#测试
docker -h
dockerd -h
```


>16.04下安装 docker
```
apt-get remove docker docker-engine docker-ce docker.io

apt-get update

apt-get install -y apt-transport-https ca-certificates curl software-properties-common

apt-get -f install -y

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

apt-key fingerprint 0EBFCD88

add-apt-repository \
"deb [arch=amd64] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) \
stable"

apt-get update

apt-cache madison docker-ce

apt-get install -y docker-ce

apt-cache madison docker-ce


```
