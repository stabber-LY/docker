直接使用的docker源中的centos的centos7版本
更新yum源
使用rpm安装一下nginx-1.10.0-1.el7.ngx.x86_64.rpm
创建nginx配置文件、访问目录、vhost配置文件以及访问目录

docker build -t stabber/nginx .
docker run -it -d -p 80 --name website -v $PWD/website:/var/www/html/website stabber/nginx nginx
进入容器
[root@ansible02 dockercreate]# docker ps -a  
CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS                    PORTS                  NAMES
1a133cc81cc4        stabber/nginx       "nginx"             About a minute ago   Up About a minute         0.0.0.0:1028->80/tcp   website             
a5775c019d18        centos              "/bin/bash"         21 hours ago         Exited (0) 16 hours ago                          pensive_leakey      
[root@ansible02 dockercreate]# docker exec -it 1a133cc81cc4 /bin/bash

停止容器
docker top 3be9f815b02f
查看活动的容器
docker ps -a
