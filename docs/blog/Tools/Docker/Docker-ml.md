## Docker容器常用命令
### tages:
     - Docker
     - Docker容器常用命令
     - Docker示例




##在Docker中，我们可以使用以下命令将容器保存为镜像：

docker commit registry-vpc.cn-shenzhen.aliyuncs.com/ruizekj/
docker commit [CONTAINER ID] [IMAGE NAME]

#映射端口并起敌不过进去入容器
docker run -it  -p 2222:22 ubuntu /bin/bash
docker run -it  -p 2222:22 cc280cd57c39 /bin/bash

#进入容器
docker exec -it 0d63e467e034 /bin/bash
docker exec -it fda199c418cc /bin/bash







#添加当前用户到 docker 用户组，可以不用 sudo 运行 docker（可选）
sudo groupadd docker
sudo usermod -aG docker $USER

#重新启动docker
sudo systemctl daemon-reload
sudo systemctl restart docker

#启动容器
docker run -it -p 18080:8080 registry-vpc.cn-shenzhen.aliyuncs.com/ruizekj/mypyhon-code-server231107:latest

docker run -d -p 8888:8888 lincaigui/mojo-jupyter:latest
sudo docker login --username=995559618@qq.com registry.cn-shenzhen.aliyuncs.com

docker run -d -p 8888:8888 registry-vpc.cn-shenzhen.aliyuncs.com/ruizekj/ruize1029:latest

登录专网拉docker  images
docker login --username=995559618@qq.com registry-vpc.cn-shenzhen.aliyuncs.com
docker pull registry-vpc.cn-shenzhen.aliyuncs.com/ruizekj/ruize1029:latest


docker操作步骤及代码
步骤1：查看本地已有的镜像
首先，我们需要查看本地已有的镜像，以确定需要备份的镜像。可以使用以下命令查看本地镜像列表：
docker images
步骤2：选择需要备份的镜像
根据步骤1中的镜像列表，选择需要备份的镜像。可以根据镜像的名称和版本号进行选择。
步骤3：备份镜像
使用以下命令备份镜像，将镜像保存为tar文件：

docker save -o <备份文件名>.tar <镜像名称>:<镜像版本>

其中，<备份文件名>为保存备份镜像的文件名，<镜像名称>为需要备份的镜像名称，<镜像版本>为需要备份的镜像版本。
步骤4：将备份的镜像文件复制到目标机器
将步骤3中备份的镜像文件复制到目标机器，可以使用scp命令或其他文件传输工具进行复制。
步骤5：导入镜像到目标机器

在目标机器上导入备份的镜像，使用以下命令：

docker load -i <备份文件名>.tar

其中，<备份文件名>为之前备份的镜像文件名。
步骤6：查看目标机器上的导入镜像

使用以下命令查看目标机器上已导入的镜像：
docker images

总结
通过以上步骤，我们可以实现Docker镜像的备份与导入操作。首先通过docker save命令将需要备份的镜像保存为tar文件，然后将备份文件复制到目标机器，最后在目标机器上使用docker load命令导入镜像。使用docker images命令可以查看本地镜像列表，确认备份和导入的结果。
希望以上步骤和代码可以帮助到你，快速掌握Docker镜像备份与导入的操作。


https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=module



快速修改运行中的docker容器端口映射的三种方式
2023年5月15日 下午8:34 • Docker

下面我们来详细讲解一下快速修改运行中的docker容器端口映射的三种方式。
方式一：使用docker命令修改端口映射

    查看运行中的docker容器
    docker ps

    使用以下命令修改端口映射，将容器内部的端口 8080 映射到宿主机的端口 8888
    docker container update --publish-add 8888:8080 容器名称或容器ID
    其中 --publish-add 表示新增一个端口映射，8888 是宿主机的端口，8080 是容器内部的端口。

    查看端口映射是否已生效
    docker container inspect 容器名称或容器ID
    在返回结果中找到 "Ports" 部分，可以看到端口映射已生效。

示例：修改 nginx 容器内部的端口 80 映射到宿主机的端口 8080

docker container update --publish-add 8080:80 nginx

方式二：使用docker-compose修改端口映射

    编辑 docker-compose.yml 文件，修改对应服务的端口映射
    services:
    web:
    ports:
    - "8888:80"
    表示将容器内部的端口 80 映射到宿主机的端口 8888。
    Python技术站热门推荐：
    PDF电子发票识别软件，一键识别电子发票并导入到Excel中！
    10大顶级数据挖掘软件！
    人工智能的十大作用！

    在 docker-compose.yml 文件所在的目录中，运行以下命令使修改生效
    docker-compose up --force-recreate --build -d
    其中 --force-recreate 表示强制重新创建容器， --build 表示在创建容器前先构建镜像。

示例：修改 docker-compose.yml 中 web 服务的端口映射，将容器内部的端口 80 映射到宿主机的端口 8888。

services:
  web:
    ports:
      - "8888:80"

方式三：使用Portainer可视化控制面板修改端口映射

1.通过浏览器访问Portainer可视化控制面板，在菜单中打开相应的docker容器详情页。

2.进入 容器设置 页面，找到 端口映射 选项，点击 添加映射。

3.将容器内部的端口 8080 映射到宿主机的端口 8888，保存设置。

4.返回 容器设置 页面，找到 容器重启 选项，点击 重启。

5.查看修改是否生效，重新进入容器详情页，查看 端口映射 是否正确。

示例：使用Portainer可视化控制面板将 nginx 容器内部的端口 80 映射到宿主机的端口 8888。

以上是三种修改运行中的docker容器端口映射的方式，根据实际情况选择适合自己的方式进行修改即可






