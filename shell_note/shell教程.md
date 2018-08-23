---
typora-copy-images-to: img
typora-root-url: img
---

# shell教程



地址：https://www.imooc.com/video/7946



shell和其他编程语言在条件测试上的表现非常不同。

按照文件类型进行判断。

- 条件测试
  - if的判断依据
  - test命令和空格的使用
  - 18819389806

4. 两个整数
5. 字符串的判断

### test命令和空格的使用

语法： test expr

```
test "$password" = "join"
[expr]

## 例子
password="kingfa"  ##赋值语句，=前后没有空格
test "$password" = "kingfa" ##条件测试命令
[ "$password" = "join" ] ##条件测试命令，注意其间必须有空格



```



1. 字符串比较
2. 文件测试
3. 数字比较
4. 复合表达式



1. 字符串比较

2. 文件测试

3. 数字比较

   语法：test int1 option int2

   或者 [ int1 potion int2 ]

   |      |      |      |
   | :--: | ---- | ---- |
   | -eq  |      |      |
   | -ne  |      |      |
   | -lt  |      |      |
   | -le  |      |      |
   | -gt  |      |      |
   | -ge  |      |      |

   

4. 复合表达式

   组合使用几个表达式

   |                |      |
   | :------------: | ---- |
   |     ！expr     |      |
   | expr1 -a expr2 |      |
   | expr1 -o expr2 |      |

   ```shell
   #! /bin/bash
   
   if [ -f $@ -a -x /usr/bin/vi ]
   then
   	cp $@ $@.bak
   	vi $@
   fi
   ```

   注意复合表达式需要走程序

   shell的条件操作符"&&" 和 "||" 可以用来替代 命令 "-a" "-o"



# 控制流



编程思想：

1. 熟悉linux基本命令，规范，语法以及shell知识，
2. 遇到实际问题，运用所学知识。
3. 背诵，背得滚瓜烂熟。

如何别程序：

1. 抄写老师的程序并能正确
2. 为程序补全注释
3. 删掉注释，读懂代码
4. 看注释写代码

## 单分支语句if

if开头

fi结尾



- 如何判断登陆的用户是否是root

  - whoami
  - env
  - env | grep USER
  - env | grep USER | cut 

- 写脚本

  ```shell
  #! /bin/bash
  test= $()
  if ["$test" == root]
  then
  	echo "it is root"
  fi
  
      
  ```

  

## 单分支if语句

例子：判断分区使用率



df -h

```shell

```



## 多分枝语句

判断输入的是否是一个目录

https://zhidao.baidu.com/question/1434651600913602739.html

```shell
#！ /bin/bash
if [ -d $FILE ]
then
     echo "$FILE 是一个目录"
else
	echo "no no no"
fi


#！ /bin/bash

read -t 30
if [ -d $file]
```



## 双分支语句

Apache服务器是否启动。

Apache linux



```shell
#! /bin/bash

test=$[]
if [ -n "$test" ]
then
	echo "that is ok"
else 
	echo 
```

![1535020459935](/1535020459935.png)





### for 循环

语法：

```shell
for variable [in list]
    do
        语句
    done
```



![1535021353120](/1535021353120.png)





### while 

不定循环，也称作条件循环。

语法：

while test-commands

do

​	commands

done





例子：

计算加法：从1加到100.

```shell
#! /bin/bash

bumber=1
sum=0
while [ $number le 100 ]
	do 
		sum=$(( $sum + $number ))
		number=$(($number + 1))
	done
echo "The summary is $sum"

```



### until

语句：思想是知道条件不为真。





# 总结shell编程

shell主要用来简化管理员操作，实现办公自动化

shell编程更多的考虑程序的功能实现，而不是效率



语法上对比C，python，就容易理解了。至此可以说自己了解shell了。

