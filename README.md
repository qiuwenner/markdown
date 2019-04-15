## Markdown语法

Markdown是一种轻量级标记语言，它允许人们使用易读易写的纯文本格式编写文档。通过简单的标记语法，它可以使普通文本内容具有一定的格式。  
- 优点：  
1、因为是纯文本，所以只要支持Markdown的地方都能获得一样的编辑效果，可以让作者摆脱排版的困扰，专心写作。  
2、操作简单。一些简单的语法，就能实现各种格式和需求。  
3、编写的文档可以导出 HTML 、Word、图像、PDF、Epub 等多种格式的文档。
- 缺点：  
1、需要记一些语法（很简单，基本是几分钟就可以学会）。  
2、有些平台不支持Markdown编辑模式  

一些支持markdown语法的平台，Github、简书、CSDN、有道云笔记等。

### 编辑器
推荐使用vs code、Typora来进行编写，具有及时预览和支持跨平台的特点，十分的方便。附上下载链接：
- [visual studio code 下载](https://code.visualstudio.com/)
- [Typora 下载](https://typora.io/)

### 1. 标题
通过 # 号的个数来分辨标题的类型，一般有六级标题（#号与文字之间有个空格space）：  
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```
效果：
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

### 2. 字体样式

- #### 加粗  

需要加粗的文本两段分别用两个 * 号或两个 _ 包起来
```
**这是加粗文本1**
__这是加粗文本2__
```
效果：  
**这是加粗文本1**  
__这是加粗文本2__

- #### 斜体

需要斜体的文本两段分别用一个 * 号或一个 _ 包起来
```
*这是斜体文本1*
_这是斜体文本2_
```
效果：  
*这是斜体文本1*  
_这是斜体文本2_

- #### 加粗斜体

需要加粗斜体的文本两段分别用三个 * 号或三个 _ 包起来
```
***这是加粗斜体文本1***
___这是加粗斜体文本2___
```
效果：  
***这是加粗斜体文本1***  
___这是加粗斜体文本2___

- #### 删除线  

需要删除线的文本两段分别用两个 ~~ 包起来
```
~~这是需要删除线文本~~
```
效果：  
~~这是需要删除线文本~~  

- #### 引用  

在段落开头使用 > 符号可以实现缩进，另外引用是可以嵌套的，一个、两个、...、n个以此类推退：
```
>这是需要引用文本 1
>>这是需要引用文本 2
>>>这是需要引用文本 3
```
效果：  
>这是需要引用文本 1
>>这是需要引用文本 2
>>>这是需要引用文本  3

### 段落  
Markdown 段落没有特殊的格式，直接编写文字就好，段落的换行是使用两个或以上空格\<space\>加上回车。
```
第一段内容<space><space>
第二段内容
```
效果：  
第一段内容  
第二段内容

### 列表 
- #### 无序列表  

用 - + * 任何一种符号加上一个空格\<space\>都可以实现  
```
- 列表内容1
+ 列表内容2
* 列表内容3
```
效果：
- 列表内容1
+ 列表内容2
* 列表内容3

- #### 有序列表  

数字加上符号点 . ，再加上一个空格\<space\>
```
1. 列表内容1
2. 列表内容2
3. 列表内容3
```
效果：  
1. 列表内容1
2. 列表内容2
3. 列表内容3

- #### 列表嵌套  
上一级和下一级之间敲三个 空格\<space\> 即可
```
1. 第一项   
   - 第一项的嵌套内容1
   - 第一项的嵌套内容2
2. 第二项   
   - 第二项的嵌套内容1
   - 第二项的嵌套内容2
```
效果：  
1. 第一项   
   - 第一项的嵌套内容1
      - 第一项的嵌套的嵌套内容1
      - 第一项的嵌套的嵌套内容2
   - 第一项的嵌套内容2
2. 第二项   
   - 第二项的嵌套内容1
   - 第二项的嵌套内容2

### 表格
Markdown 制作表格使用 | 来分隔不同的单元格，第二行分割表头和内容，并设置内容和标题栏的对齐格式。使用一个或多个 - 加上一个冒号 : 来表示。
文字默认居左  
-: 设置内容和标题栏居右对齐。  
:- 设置内容和标题栏居左对齐。  
:-: 设置内容和标题栏居中对齐。  
```
(分别是：左对齐、居中、右对齐)
姓名|明显特征|排行名次
--|:--:|--:
苏明哲|要面子|老大
苏明成|啃老|老二
苏明玉|强势独立|老三
```
效果：
姓名|明显特征|排行名次
--|:--:|--:
苏明哲|要面子|老大
苏明成|啃老|老二
苏明玉|强势独立|老三

### 代码块
单行代码：代码之间分别用一个反引号 \` 包起来  
效果：  
`代码内容`  
代码块：分别用三个反引号 \` 包裹一段代码，并指定一种语言（也可以不指定），且两边的反引号单独占一行  
效果：  
``` lua
local str = "markdown is very useful"
print(str)
```


### 链接
网页跳转，Markdown本身语法不支持链接在新页面中打开，而一些平台可能做了处理，语法：
```
[alt名字](超链接地址 "超链接title")
alt名字是显示在页面上的名字
title是链接的标题，当鼠标移到链接上时显示的内容。title可以不加
```
示例：
```
[Markdown教程](https://www.jianshu.com/p/154eea07ae2c "Markdown教程")
[Git与Github教程](https://www.jianshu.com/p/a0859b8ddfd9)
```
效果：  
[Markdown教程](https://www.jianshu.com/p/154eea07ae2c "Markdown教程")  
[Git与Github教程](https://www.jianshu.com/p/a0859b8ddfd9)

### 图片
语法：
```
![alt名字](图片路径 "图片title")
alt就是显示在图片下面的文字，相当于对图片内容的解释。
title是图片的标题，当鼠标移到图片上时显示的内容。title可以不加
```
示例：
```
![markdown图标](http://www.runoob.com/wp-content/uploads/2019/03/iconfinder_markdown_298823.png "markdown图标")
```
效果：
![markdown图标](http://www.runoob.com/wp-content/uploads/2019/03/iconfinder_markdown_298823.png "markdown图标")
