# docker

1. 容器上传docker hub

```
 docker commit -a "JeremyHua1931" -m "ubantu20.04 with oh-my-zsh" c235a05b3bd3  jeremyhua1931/ubantu20.04:v1
 docker login
 docker push jeremyhua1931/ubantu20.04:v1
```

2. 镜像上传到docker hub

```
docker pull josephkamel/f2md:1.0
docker tag josephkamel/f2md:1.0  jeremyhua1931/f2md:v1
docker login
docker push jeremyhua1931/f2md:v1
```

## docker install

```
# 参考链接：https://yeasy.gitbook.io/docker_practice/install/ubuntu

# 卸载旧版本docker
sudo apt-get remove docker \
               docker-engine \
               docker.io

# 使用apt安装docker
 sudo apt-get update

 sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

# 建议使用国内源安装
# 国内源
$ curl -fsSL https://mirrors.aliyun.com/docker-ce/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
# 官方源
# $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# 想sources.list中添加Docker软件源
$ echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://mirrors.aliyun.com/docker-ce/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
# 官方源
# $ echo \
#   "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
#   $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# 更新 apt 软件包缓存，并安装 docker-ce
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io
```

```
# 使用脚本自动安装Docker
curl -fsSL get.docker.com -o get-docker.sh
sudo sh get-docker.sh --mirror Aliyun
# $ sudo sh get-docker.sh --mirror AzureChinaCloud

# 若想安装测试版的 Docker, 请从 test.docker.com 获取脚本
# $ curl -fsSL test.docker.com -o get-docker.sh
```

```
# 启动 Docker
sudo systemctl enable docker
sudo systemctl start docker
```

```
# 建立 docker 组
sudo groupadd docker

# 将当前用户加入 docker 组
sudo usermod -aG docker $USER
```

```
# 测试 Docker 是否安装正确
docker run --rm hello-world

Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
b8dfde127a29: Pull complete
Digest: sha256:308866a43596e83578c7dfa15e27a73011bdd402185a84c5cd7f32a88b501a24
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```

## 
