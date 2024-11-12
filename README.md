（0）找管理员在harbor.test.geely.com中添加用户

（1）确认基础镜像

基础镜像网站：

https://catalog.ngc.nvidia.com/orgs/nvidia/containers/pytorch/tags?quick-deploy=false

docker-hub看信息

（2）按照确认好的基础镜像准备好dockerfile（和对应的requirement.txt）

（3）sudo docker build -t your_docker_name /path/to/dockerfile

（4）sudo docker images, 找到iamge id

（5）sudo docker login harbor.test.geely.com，输入username（域账号）和password

（6）sudo docker tag <Image ID> harbor.test.geely.com/di-public/<docker_name>:<version>

（7）sudo docker push harbor.test.geely.com/di-public/<docker_name>:<version>

（8）笔记本打开harbor.test.geely.com, 域账号密码登录, 项目 => di-public => 找到镜像， 点拉取镜像，拷贝拉取命令（docker pull）

（9）打开AML平台，创建开发机，选择镜像URL，把拉取命令中的docker pull删掉，下面填写域账号和密码

（10）执行其他正常操作，完成开发机创建，测试环境，保存镜像
