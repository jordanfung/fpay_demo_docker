# Fpay demo docker 构建脚本

原有fpay demo打包和测试步骤实在太繁琐让人不爽，于是有了本项目。



注意：构建脚本使用了 https://github.com/jordanfung/fpay_demo ，而非官方repo。



测试环境：

- Ubuntu 18.04 Bionic x86_64, kernel 4.15.0-30-generic
- Docker version 18.06.0-ce, build 0ffa825



测试结果：

|    目录    |          OS          |        备注         |
| :--------: | :------------------: | :-----------------: |
| ubuntu1604 | Ubuntu 16.04 Xential | 构建成功✔︎ 启动成功✔︎ |
| Ubuntu1804 | Ubuntu 18.04 Bionic  | 构建成功✔︎启动失败✘  |

