README
===========================
该文件用来测试和展示书写README的各种markdown语法。GitHub的markdown语法在标准的markdown语法基础上做了扩充，称之为`GitHub Flavored Markdown`。简称`GFM`，GFM在GitHub上有广泛应用，除了README文件外，issues和wiki均支持markdown语法。

****

|图片|名字|描述|
|:----:|:---:|:---|
|![my-logo-small]|Author|Gorpeln|
|![mail-logo-small]|E-mail|154158462@qq.com|
|![csdn-logo-small]|CSDN|http://blog.csdn.net/chen_gp_x|
|![qqgroup-logo-small]|QQ群|119783156|  

****
|1|3|4|4|5|5|6|
|:----:|:---:|:---:|:----:|:----:|:----:|:----:|
|Author|E-mail|CSDN|QQ群|公众号|简书|知乎|
|[Gorpeln]|logo|logo|logo|[公众号][QRCode-wechat]|[我的简书][jianshu]|[我的简书][zhihu]|
****

## 目录
* [横线](#横线)
* [标题](#标题)
* [文本](#文本)
    * 普通文本
    * 单行文本
    * 多行文本
    * 文字高亮
    * 换行
    * 斜体
    * 粗体
    * 删除线
* [图片](#图片)
    * 来源于网络的图片
    * GitHub仓库中的图片
* [链接](#链接) 
    * 文字超链接
        *  链接外部URL
        *  链接本仓库里的URL
    *  锚点
    * [图片链接](#图片链接)
* [列表](#列表)
    * 无序列表
    * 有序列表
    * 复选框列表
* [块引用](#块引用)
* [代码高亮](#代码高亮)
* [表格](#表格) 
* [表情](#表情)
* [diff语法](#diff语法)

### 横线
-----------
***、---、___可以显示横线效果

***
---
___



标题
------

# 一级标题  
## 二级标题  
### 三级标题  
#### 四级标题  
##### 五级标题  
###### 六级标题  


文本
------
### 普通文本
这是一段普通的文本
### 单行文本
在一行开头加入1个Tab或者4个空格。

	Hello,大家好，我是 Gorpeln Chen 。
	
### 文本块
#### 语法1
在连续几行的文本开头加入1个Tab或者4个空格。

    欢迎到访,
    很高兴见到您!
    祝您，早上好，中午好，下午好，晚安。

#### 语法2
使用一对各三个的反引号：
```
欢迎到访，
我是专注于iOS的码农。
你可以在 CSDN、github搜索【Gorpeln】找到我哦！
```
该语法也可以实现代码高亮，见[代码高亮](#代码高亮)
### 文字高亮
文字高亮功能能使行内部分文字高亮，使用一对反引号。
语法：
```
`linux` `iOS` `HTML5` `小程序` `php` `APIClound`
```
效果：`linux` `iOS` `HTML5` `小程序` `php` `APIClound`

也适合做一篇文章的tag
### 换行
直接回车不能换行，  
可以在上一行文本后面补两个空格，  
这样下一行的文本就换行了。

或者就是在两行文本直接加一个空行。

也能实现换行效果，不过这个行间距有点大。
### 斜体、粗体、删除线

|语法|效果|
|----|-----|
|`*斜体1*`|*斜体1*|
|`_斜体2_`| _斜体2_|
|`**粗体1**`|**粗体1**|
|`__粗体2__`|__粗体2__|
|`这是一个 ~~删除线~~`|这是一个 ~~删除线~~|
|`***斜粗体1***`|***斜粗体1***|
|`___斜粗体2___`|___斜粗体2___|
|`***~~斜粗体删除线1~~***`|***~~斜粗体删除线1~~***|
|`~~***斜粗体删除线2***~~`|~~***斜粗体删除线2***~~|

    斜体、粗体、删除线可混合使用

图片
------
基本格式：
```
![alt](URL title)
```
alt和title即对应HTML中的alt和title属性（都可省略）：
- alt表示图片显示失败时的替换文本
- title表示鼠标悬停在图片时的显示文本（注意这里要加引号）

URL即图片的url地址，如果引用本仓库中的图片，直接使用**相对路径**就可了，如果引用其他github仓库中的图片要注意格式，即：`仓库地址/blob/分支名/图片路径`，如：
```
https://github.com/GorpelnChen/README/blob/master/Images/myLogo.jpg
```

|#|语法|效果|
|---|---|:----:|
|1|`![baiduLogo](http://www.baidu.com/img/bdlogo.gif "百度logo")`|![baidu-logo](http://www.baidu.com/img/bdlogo.gif "百度logo")
|2|`![][myLogo_small]`|![][my-logo]
|3|`![](https://github.com/GorpelnChen/README/blob/master/Images/myLogo.jpg)`|![](https://github.com/GorpelnChen/README/blob/master/Images/myLogo.jpg)

注意例2的写法使用了**URL标识符**的形式，在[链接](#链接)一节有介绍。
>在文末有myLogo_small的定义：
```
[myLogo_small]:https://github.com/GorpelnChen/README/blob/master/Images/myLogo.jpg
```

链接
------
### 链接外部URL

|#|语法|效果|
|---|----|:-----:|
|1|`[我的CSDN](http://blog.csdn.net/chen_gp_x "Gorpeln")`|[我的CSDN](http://blog.csdn.net/chen_gp_x "Gorpeln")|
|2|`[我的知乎][zhihu]（暂无内容） `|[我的知乎][zhihu] |
|3|`[我的简书][jianshu]（暂无内容） `|[我的简书][jianshu] |

语法2由两部分组成：
- 第一部分使用两个中括号，[ ]里的标识符（本例中zhihu），可以是数字，字母等的组合，标识符上下对应就行了（**姑且称之为URL标识符**）
- 第二部分标记实际URL。

>使用URL标识符能达到复用的目的，一般把全文所有的URL标识符统一放在文章末尾，这样看起来比较干净。
>>URL标识符是我起的名字，不知道是否准确。囧...

### 链接本仓库里的URL

|语法|效果|
|----|-----|
|`[我的简介](/myProfile.md)`|[我的简介](/myProfile.md)|
|`[我的头像](/Images/myLogo.jpg)`|[我的头像](/Images/myLogo.jpg)|

### 图片链接
给图片加链接的本质是混合图片显示语法和普通的链接语法。普通的链接中[ ]内部是链接要显示的文本，而图片链接[ ]里面则是要显示的图片。  
直接混合两种语法当然可以，但是十分啰嗦，为此我们可以使用URL标识符的形式。

|#|语法|效果|
|---|----|:---:|
|1|`[![csdn-logo]][csdn]`|[![csdn-logo]][csdn]|
|2|`[![jianshu-logo]][jianshu](暂无内容)`|[![jianshu-logo]][jianshu]|
|3|`[![](/Images/zhihuLogo.png "Gorpeln")][zhihu](暂无内容)`|[![](/Images/zhihuLogo.png "Gorpeln")][zhihu]|

因为图片本身和链接本身都支持URL标识符的形式，所以图片链接也可以很简洁（见例1）。  
注意，此时鼠标悬停时显示的文字是图片的title，而非链接本身的title了。
> 本文URL标识符都放置于文末

### 锚点
其实呢，每一个标题都是一个锚点，和HTML的锚点（`#`）类似，比如我们 

|语法|效果|
|---|---|
|`[回到顶部](#readme)`|[回到顶部](#readme)|
|`[去到尾部](#end)`|[去到尾部](#end)|

不过要注意，标题中的英文字母都被转化为**小写字母**了。
> 以前GitHub对中文支持的不好，所以中文标题不能正确识别为锚点，但是现在已经没问题啦！

## 列表
### 无序列表
* 昵称：Gorpeln
- 别名：风未止
* 英文名：Gorpeln

### 多级无序列表
* 编程语言
	* 移动端开发
		* iOS
		* swift
	* PC端开发
	* 前端开发
	* 服务端开发
		* PHP
		* JAVA
    
### 有序列表
#### 一般效果
就是在数字后面加一个点，再加一个空格。不过看起来起来可能不够明显。    
面向对象的三个基本特征：

1. 封装
2. 继承
3. 多态


#### 多级有序列表
和无序列表一样，有序列表也有多级结构：  

1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
	 

### 复选框列表
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付

您可以使用这个功能来标注某个项目各项任务的完成情况。
> Tip:
>> 在GitHub的**issue**中使用该语法是可以实时点击复选框来勾选或解除勾选的，而无需修改issue原文。

## 块引用

### 常用于引用文本
#### 文本摘自 百度百科 【 Objective-C 】词条
　Objective-C，通常写作ObjC或OC和较少用的Objective C或Obj-C，是扩充C的面向对象编程语言。它主要使用于Mac OS X和GNUstep这两个使用OpenStep标准的系统，而在NeXTSTEP和OpenStep中它更是基本语言。
> GCC与Clang含Objective-C的编译器，Objective-C可以在GCC以及Clang运作的系统上编译。  
1980年代初布莱德·考克斯(Brad Cox)在其公司Stepstone发明Objective-C。他对软件设计和编程里的真实可用度问题十分关心。Objective-C最主要的描述是他1986年出版的书 Object Oriented Programming: An Evolutionary Approach. Addison Wesley. ISBN 0-201-54834-8.

### 块引用有多级结构
> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树

代码高亮
----------
在三个反引号后面加上编程语言的名字，另起一行开始写代码，最后一行再加上三个反引号。
```Java
public static void main(String[]args){} //Java
```
```c
int main(int argc, char *argv[]) //C
```
```Bash
echo "hello GitHub" #Bash
```
```javascript
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
```
```cpp
string &operator+(const string& A,const string& B) //cpp
```
表格
--------

表头1  | 表头2|
--------- | --------|
表格单元  | 表格单元 |
表格单元  | 表格单元 |

| 表头1  | 表头2|
| ---------- | -----------|
| 表格单元   | 表格单元   |
| 表格单元   | 表格单元   |

### 对齐
表格可以指定对齐方式

| 左对齐 | 居中  | 右对齐 |
| :------------ |:---------------:| -----:|
| 风未止      | some wordy text | $1600 |
| col is       | centered        |   $12 |
| gorpeln chen | are neat        |    $1 |

### 混合其他语法
表格单元中的内容可以和其他大多数GFM语法配合使用，如：  
#### 使用普通文本的删除线，斜体等效果

| 名字 | 描述 |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

#### 表格中嵌入图片（链接）
其实前面介绍图片显示、图片链接的时候为了清晰就是放在在表格中显示的。

| 图片 | 描述 |
| ---- | ---- |
|![路飞][my-logo] | 路飞|

表情
----------
Github的Markdown语法支持添加emoji表情，输入不同的符号码（两个冒号包围的字符）可以显示出不同的表情。

比如`:blush:`，可以显示:blush:。

具体每一个表情的符号码，可以查询GitHub的官方网页[http://www.emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com)。

但是这个网页每次都打开**奇慢**。。所以我整理到了本repo中，大家可以直接在此查看[emoji](./emoji.md)。

diff语法
---------
版本控制的系统中都少不了diff的功能，即展示一个文件内容的增加与删除。
GFM中可以显示的展示diff效果。使用绿色表示新增，红色表示删除。

其语法与代码高亮类似，只是在三个反引号后面写diff，
并且其内容中，以 `+ `开头表示新增，`- `开头表示删除。

效果如下：

```diff
+ 运筹帷幄之中，决胜千里之外
- 运筹帷幄之中，决胜千里之外
```
### END


--------------------------------
[csdn]:http://blog.csdn.net/chen_gp_x "Gorpeln"
[zhihu]:https://www.zhihu.com/people/gorpeln "Gorpeln"
[jianshu]:https://www.jianshu.com/users/d9e93557a550 "Gorpeln"

[my-logo]:https://github.com/GorpelnChen/README/blob/master/Images/myLogo.jpg
[baidu-logo]:http://www.baidu.com/img/bdlogo.gif "百度logo"
[csdn-logo]:/Images/csdnLogo.png "Gorpeln"
[jianshu-logo]:/Images/jianshuLogo.png "Gorpeln"
[zhihu-logo]:/Images/zhihuLogo.png "Gorpeln"

[csdn-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/csdnLogo_small.png "http://blog.csdn.net/chen_gp_x"
[jianshu-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/jianshuLogo_small.png "www.jianshu.com/users/d9e93557a550"
[zhihu-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/zhihuLogo_small.png "https://www.zhihu.com/people/gorpeln"
[my-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/myLogo_small.png "Gorpeln"
[qqgroup-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/qqgroupLogo_small.png "119783156"
[wechat-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/wechatLogo_small.png "Gorpeln"
[mail-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/mailLogo_small.png "154158462@qq.com"
[QRCode-wechat]:https://github.com/Gorpeln/README/blob/master/Images/QRCode_whchat.png "公众号"
[mail-logo-small]:https://github.com/Gorpeln/README/blob/master/Images/smallImage/mailLogo_small.png "154158462@qq.com"
[Gorpeln]: /myProfile.md "Gorpeln"

