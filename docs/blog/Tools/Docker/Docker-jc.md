## Docker基础知识

### tages:
     - Docker
     - Docker镜像制作

\`\`\`python
##Docker镜像制作
# 使用我的rscodes-ubuntssh:latest作为基础镜像
FROM c53eff802780

# 设置工作目录
WORKDIR /home/coder

# 暴露22端口
EXPOSE 22

# 暴露80端口
EXPOSE 80

# 暴露8080端口
EXPOSE 8080

# 设置root密码
RUN echo 'root:1234' | chpasswd

# 启动SSH服务
CMD ["/usr/sbin/sshd", "-D"]
docker run -it  -p 2222:22 cc280cd57c39 /bin/bash
##另一种
# 使用官方 Ubuntu 基础镜像
FROM ubuntu:latest\`\`\`python

# 安装 OpenSSH 服务
RUN apt-get update && apt-get install -y openssh-server

# 启动 ssh 服务并设置开机自启
RUN mkdir /var/run/sshd
RUN echo 'root:yourpassword' | chpasswd
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
CMD ["/usr/sbin/sshd", "-D"]

# 暴露 22 端口
EXPOSE 22

# 设置工作目录
WORKDIR /root

```


