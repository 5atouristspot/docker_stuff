# docker_stuff

该步可忽略，只是为了记录常规情况下如何离线安装docker

```bash
# 下载依赖和安装包
wget https://apt.dockerproject.org/repo/pool/main/d/docker-engine/docker-engine_17.05.0~ce-0~ubuntu-trusty_amd64.deb
wget http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libltdl7_2.4.6-0.1_amd64.deb
wget http://archive.ubuntu.com/ubuntu/pool/universe/libg/libgcrypt20/libgcrypt20_1.6.1-2ubuntu1_amd64.deb
wget http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/libsystemd-journal0_204-5ubuntu20_amd64.deb

# 安装
dpkg -i *.deb

#测试
docker -h
dockerd -h
```
