### Max-DNMP 
---
>  D(Docker)N(Nginx)M(MySQL)P(PHP),该项目使用docker-compose组成,其中PHP因为其官方镜像没有加入mysql连接池,所以采用DOCKERFILE进行拓展.
> 没其他的废话,上代码
---

#### Basic Usage

1. Install Docker

   www.baidu.com

2. Install docker-compose

   www.baidu.com

3. 修改配置文件

   1. 在***./docker-compose.yml***文件中将自己的项目文件所在位置修改至Nginx和php配置项中
   2. php拓展处理,配置文件在***./php/php71/Dockerfile***

4. 启动

   1. 在项目根目录下运行

      ```shell
      docker-compose up -d
      ```

   2. 访问**localhost**

      1. 默认的配置中Nginx链接的是宿主机器80端口
         			MySQL链接的3306端口# docker-compose
# docker-compose
