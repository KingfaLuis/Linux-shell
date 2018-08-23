# Xpath语法





代码

```xml
<?xml version="1.0" encoding="ISO-8859-1"?>

<bookstore>

<book>
  <title lang="eng">Harry Potter</title>
  <price>29.99</price>
</book>

<book>
  <title lang="eng">Learning XML</title>
  <price>39.95</price>
</book>

</bookstore>
```



|  表达式  |                                                        |
| :------: | ------------------------------------------------------ |
| nodename | 选取此节点的所有子节点                                 |
|    /     | 从根节点选取                                           |
|    //    | 从匹配选的当前节点选择文档中的节点，而不考虑他们的位置 |
|    .     | 选取当前节点                                           |
|    ..    | 选取当前节点的父节点                                   |
|    @     | 选取属性                                               |





谓语（predicates）

谓语写在方括号里面

| 路径表达式                      |      |
| ------------------------------- | ---- |
| /bookstore/book[1]              |      |
| /bookstore/book[last()]         |      |
| /bookstore/book(last()-1)       |      |
| /bookstore/book[position()<3]   |      |
| //title[@lang]                  |      |
| //title[@lang='eng']            |      |
| /bookstore/book[price>35]/title |      |
|                                 |      |



## 选取未知节点

通配符可以用来选取未知的xml元素

| 通配符 | 描述             |
| :----: | ---------------- |
|   *    | 匹配任何元素节点 |
|   @*   | 匹配任何属性节点 |
| node() | 匹配任何类型节点 |



|  路径表达式  |      |
| :----------: | ---- |
| /bookstore/* |      |
|     //*      |      |
| //title[@*]  |      |





## 选取若干路径



|            路径表达式            |                                                              |
| :------------------------------: | ------------------------------------------------------------ |
|   //book/title \| //book/price   |                                                              |
|        //title \| //price        | 选取文档中的所有的title 和 price                             |
| /bookstore/book/title \| //price | 选取属于bookstore元素的book的元素的所有title元素，以及文档中所有的price元素 |



# Xpath Axes轴

轴可定义相对于当前节点的节点集



| 轴名称             |                                            |
| ------------------ | ------------------------------------------ |
| ancestor           |                                            |
| ancestor-or-self   |                                            |
| attribute          | 选取当前节点的所有属性                     |
| child              | 选取当前节点的所有子元素                   |
| desendant          | 选取当前节点的所有后代元素                 |
| following          | 选取文档中当前节点的结束标签之后的所有节点 |
| namespace          |                                            |
| parent             |                                            |
| preceding          |                                            |
| preceding-slibling |                                            |
| self               |                                            |
|                    |                                            |





## 位置路径表达式

 ### 绝对位置路径



```
/step/step/...
```



### 相对位置路径



```
step/step/...
```



### 步（step）包括

轴axis

定义所选节点与当前节点之间的树关系

节点测试

识别某个轴内部的节点

零个或者更多谓语（predicate）

 ### 步的语法

```
轴名称：：节点测试[谓语]
```

实例

|          例子          | 结果                                   |
| :--------------------: | -------------------------------------- |
|      child::book       | 选取所有属于当前节点的子元素的book节点 |
|    attribute::lang     |                                        |
|        child::*        |                                        |
|      attribute::*      |                                        |
|     child::text()      |                                        |
|     child::node()      |                                        |
|    descendant::book    |                                        |
|     ancestor::book     |                                        |
| ancestor-or-self::book |                                        |
| child::*/child::price  |                                        |
|                        |                                        |
|                        |                                        |





## 您已经学习了 XPath，下一步应当学习什么呢？

您下一步应该学习 XSLT、XQuery、XLink 以及 XPointer。