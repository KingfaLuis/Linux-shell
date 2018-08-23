# Ubuntu16.04安装Scrapy命令



## 背景

命令行下有三种安装Scrapy的方式：

```
apt-get:千万不要用，因为你会下载到一个上古时期的Scrapy版本，产生一系列与你参考教程的代码不兼容的问题
easy_install:我没有安装成功
pip:Scrapy官网上推荐的下载方式，我们使用这种方法
1234
```

## 安装

首先python、lxml、OpenSSL这些工具Ubuntu是自带的，不用管它们。

其次安装pip，在命令行中执行以下命令：

```
sudo apt-get install python-pip1
```

然后安装两个安装Scrapy需要的依赖库，在命令行中分别执行以下三条命令：

```
sudo apt-get install python-dev
sudo apt-get install libevent-dev
sudo apt-get install libssl-dev  # 在阿里云上配置的时候发现还得确定有这个123
```

最后安装Scrapy，在命令行中执行以下命令：

```
sudo pip install scrapy1
```

然后我们的最新版Scrapy就安装好了，可以执行下列命令查看版本号：

```
scrapy version
```

------

ipython是一个不错的交互工具，调试Python代码很方便

# 安装ipython

```
$ sudo apt-get install ipython3
$ sudo pip install ipython12
```

# 安装Qt console 工具

```
$ sudo pip install jupyter1
```

# 使用Ipython

## 进入 ipython

```
$ ipython1
```

## 使用TAB代码提示

![这里写图片描述](https://img-blog.csdn.net/20171109154701140?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGFuaGFpeHVhbnZ2/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)