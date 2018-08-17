# Fpay demo docker 构建脚本

原有fpay demo打包和测试步骤实在太繁琐让人不爽，于是有了本项目。

注意：构建脚本使用了 https://github.com/jordanfung/fpay_demo ，而非官方repo。



使用说明：

> cd $WORKDIR
>
> git clone https://github.com/jordanfung/fpay_demo_docker
>
> cd pay_demo_docker/ubuntu1604
>
> docker build -t fp1604 .

生成名为**fp1604**的image，里面包含了编译好的fpay_demo二进制文件、源码、以及所需要的一切依赖。



用下面命令启动一个docker container

> docker run -it fp1604



二进制目录： /fpay_demo/build/FPDemo/bin

test目录：/fpay_demo/test



测试环境：

- Ubuntu 18.04 Bionic x86_64, kernel 4.15.0-30-generic
- Docker version 18.06.0-ce, build 0ffa825



测试结果：

|    目录    |          OS          |        备注         |
| :--------: | :------------------: | :-----------------: |
| ubuntu1604 | Ubuntu 16.04 Xential | 构建成功✔︎ 启动成功✔︎ |
| Ubuntu1804 | Ubuntu 18.04 Bionic  | 构建成功✔︎启动失败✘  |

TODO:

- 使用 docker-compose 编排 redis/root server/miner server 测试服务
- 单独打包test客户端

