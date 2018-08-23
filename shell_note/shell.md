# shell

[YouTube教程视频](https://www.youtube.com/watch?v=AcSkkNAsGCY&index=3&list=PLS1QulWo1RIYmaxcEqw5JhK3b-6rgdWO_)



```shell
cat /etc/shells
which bash


chmod +x hello.sh
ls -al

./hello.sh

```

进入桌面

ls

touch hello.sh

cat





熟悉shell的最好的方法就是大量尝试

运行每个命令，看看有什么结果。



花点时间思考pyhon,JavaScript，shell有什么区别？

都是脚本。

- 都是代码单元
- 都有名称
- 都接收自变量
- 但他们处于完全不同的环境中。
- 在终端使用shell命令，与在程序中调用函数非常相似
- 但是两种技术使用的目的是不同的。函数用来组织程序，而shell命令则用来运行程序。因为shell命令以文本形式输出结果，所以很容易读懂和理解做了什么，



Nginx，sed,awk这些可以问问贵哥。



12. 看命令输出什么。
    1. uptime
    2. ls



## 课程2：shell命令

这里讲记录更多的命令。

在进行之前，我们先了解文件系统的知识。

- 文件名 filename
- 内容 content



| filename        |                    |      |
| --------------- | ------------------ | ---- |
| Hello-Kitty.jpg | 保存图片           |      |
| license         | 文本               |      |
| readme.md       | markdown文档       |      |
| superuser.pem   | ssh, pem. 增强邮件 |      |
| install.sh      | 脚本文件           |      |



vmstat



- command history

  - 历史使用命令查看
    - 输入 ctrl + R
    - history
    - 方向键向上

- 4 一些常用命令

  - unzip things.zip
  - cat 
  - tab 自动补全功能
  - wc 文件，分析文件
  - diff

- 5 Manual Pages 手册页

  - cowsay
  - man cowsay 在我的系统里面没用

- 练习阅读理解手册内容

  - 回答cowsay的作者
  - 标志-T 

- 7 通过查看手册 

  - man ls 找到显示所有文件的方法
  - ls -a
  - ls -all

- 8 ls -l 包含哪些信息，有四个

  - 文件的修时间
  - 是文件还是目录

- 9 搜索命令 rm -rf 中的r, f

  - 不要轻易执行这个命令，否则会删除你整个目录的信息
  - r 代表 recursive 
  - f stand for force 

- 10 line Based Programs

  - 使用ctrl C中断
  - 使用ctrl D执行程序。
  - 标准输入输出

- 使用full Screen interactive Programm

  - 输入长文件名使用tab键
  - 翻页使用D
  - \>
  - less()
  - 可以使用正则表达式
  - 
  - 
  - 使用ctrl X退出编辑器
  - \j

  

  

  # 文件系统

  在linux服务器上

  - 使用正斜杠表示命令
  - 相对路径和绝对路径
  - ..
  - ~
  - ~/ocean/otter

  - 

    