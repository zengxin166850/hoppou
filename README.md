# hoppou
使用renren-fast测试github+dockerhub的自动构建
经尝试，只有将jar包放到dockerfile同目录下再能自动构建镜像。
- 项目中使用到的数据库，redis均为docker中部署的同网段容器
- 猜测不存在自动install打包源码的行为，
- 在没有jar的时候，build过程中，会在ADD目录的时候报如下的错误:
> ADD failed: stat /var/lib/docker/tmp/docker-builder225088559/target/renren-fast.jar: no such file or directory
- build成功之后的镜像详见
> https://cloud.docker.com/repository/docker/hoppou/hoppou/builds
