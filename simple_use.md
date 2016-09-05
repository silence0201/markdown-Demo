MarkDown语法测试
======================
该文件用来测试基本的markdown语法.`markdown`是一种很常见的排版方式,`github`的`README`文件是在markdowm语句基础上进行扩展的`Github Flavored Markdown`.`markdown`应用十分广泛,一些博客以及wiki都是支持`markdown`进行编辑的  
***
###　　　　　　　　　　　　  Author : Silence  
###　　　　　　　　　　　  Data : 2016年09月05日        
     
======================  
  

##目录
1. [横线](#1.横线)
2. [标题](#2.标题)
3. [文本](#3.文本)
	* 普通文本
	* 单行文本
	* 多行文本
	* 文字高亮
	* 代码格式化
	* 换行
	* 斜体
	* 粗体
	* 删除线
4. [图片](#4.图片)
	* 来源网络的图片
	* 来源本地图片
5. [链接](#5.链接)
	* 文字链接
		* 外部URL
		* 本地URL
	* 锚点
	* 图片链接
6. [列表](#6.列表)
	* 有序列表
	* 无序列表
	* 复选框列表
7. [块引用](#7.块引用)
8. [代码高亮](#8.代码高亮)
9. [表格](#9.表格)

##1.横线


***/---/___可以显示横线效果
***   
---   
___   

##2.标题

#一级标题
##二级标题
###三级标题
####四级标题
#####五级标题
######六级标题   

##3.文本

###普通文本
这是一段普通文本

###单行文本
	我是一行单行文本,需要在一行开头加入一个Tab或者四个空格,测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试

####多行文本
	多行文本需要在单行文本的模式下进行分行   
	多行文本测试

###文字高亮
文字高亮功能能使行内部分文字高亮,需要使用一对反引号  
```
`Linux` `Objective-C`
```
效果为:`Linux` `Objective-C`
适合做一些文章的tag

###代码格式化
```
+ (instancetype)SI_buttonCustomButtonFrame:(CGRect)frame
                           normalImageName:(NSString *)imageName
                               actionBlock:(ButtonActionBlock)block{
    MyButton *button = [MyButton buttonWithType:UIButtonTypeCustom] ;
    button.frame = frame ;
    [button setImage:[UIImage imageNamed:imageName] forState:UIControlStateNormal] ;
    button.actionBlock = block ;
    return button ;
}
```

###换行
直接回车不能换行  
可以在上一行文本后面补两个空格  
这样下一行的文本就能换行了

或者在两行文本中直接加一个回车

也能实现对象的效果,不过这样的行距比较大

###斜体/粗体/删除线
| 语法 | 效果 |  
|-----|------ |
|`*斜体1*`|*斜体*|
|'_斜体2_'|_斜体2_|
|`**粗体1**`|**粗体1**|
|`__粗体2__`|__粗体__|
|`~~删除线~~`|~~删除线~~|
|`***斜粗体1***`|***斜粗体***|
|`___斜粗体2`|***斜粗体***|
|`***~~斜粗删除体~~***`|***~~斜粗删除体~~***|  

斜体/粗体/删除线可以混合使用

##4.图片

基本格式  
```
![alt](URL title)
```  

属性含义如下:
> 1. alt表示图片显示失败时,替换的文本  
> 2. title表示图片悬停在图片的时候显示的文本  
> 3. URL表示图片url的地址,如果会本地仓库内的地址,可以直接使用**相对路径**

###来自网络的图片
`![2016090556137p101 3.jpg](http://7xwbzi.com1.z0.glb.clouddn.com/20160905561.jpg)`

![2016090556137p101 3.jpg](http://7xwbzi.com1.z0.glb.clouddn.com/20160905561.jpg)

###来自本地的图片
`![pp](./pp.jpg)`   
![pp](./pp.jpg)  
如果引用github的地址注意格式为:`仓库地址/raw/分支名/图片路径`


##5.链接

基本格式   
 
* 内联式:  
```
[title](URL tip)
```
> 1. title 显示的文本
> 2. URL 超链接的地址
> 3. tip 悬停显示的提示


* 外链式   
```
  [title][name]  
  [name]:URL tip  
```
> 1. title 显示的文本
> 2. name 外链的标记名称
> 3. URL 超链接的地址
> 4. tip 悬停显示的提示

###文字链接
* 外部URL
  1. [我的博客](http://www.playcode.cc '我的博客')
  2. [百度][baidu]  
  
* 本地URL
  1. [About](./About.md)
  2. [Pic](./pp.jpg)
    
    
###锚点
每一个标题都是一个锚点,和Html的锚点类似  
不过要注意，标题中的英文字母都被转化为**小写字母**了

###图片链接
给图片加链接本质是混合图片显示语法和普通的链接语法.  
普通的链接中[ ]内部是链接要显示的文本,而图片链接[ ]里面则是要显示的图片   
1. 内联式 
[![2016090523637p102 2.jpg](http://7xwbzi.com1.z0.glb.clouddn.com/2016090523637p1.jpg)](http://www.playcode.cc 'text')
2. 外链式  
[![2016090528227p106.png](http://7xwbzi.com1.z0.glb.clouddn.com/2016090528227p106.png)][baidu]  

##6.列表

###有序列表
* #####一般效果  
就是在数字后面加一个点,再加一个空格.  
面向对象的三大特征  
  1. 封装
  2. 继承
  3. 多态  
 
* #####自动排序
  面向对象的七大原则
  1. 开放封闭原则
  * 李氏替换原则
  * 依赖倒转原则
  * 接口耦离原则
  * 组合/聚合复用原则
  * 迪米特原则
  * 单一职责原则
* #####多级有序列表
   1. 第一层
      1. 第二层 
         1. 第三层
      2. 第二层
         1. 第三层
  
###无序列表
* #####单层次
  * 你好
  * 世界

* #####多层次
  * 编程语言
     - 脚本语言
       * python
       
  
  
###复选框列表
 - [x] 需求分析
 - [x] 系统设计
 - [ ] 编码
 - [ ] 测试
   
   
##7.块引用

###简单使用
这是主要内容  
> 这是引用内容

###多层结构
> 数据结构
>> 树
>>>二叉树
>>>>平衡二叉树
>>>>满二叉树


##8.代码高亮


在三个反引号后面加上编程语言的名称,最后另起一行开始写代码,最后一行再加上三个反引号  
  
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

##9.表格

###表格1

表头1 | 表头2   
------|-----  
表格单元 | 表格单元  
表格单元 | 表格单元  

###表格2
| 表头1 | 表头2 |
|------|-------|
| 表格单元 | 表格单元 |  
| 表格单元 | 表格单元 |   

###指定对其方式
表格可以指定对齐方式 
 
| 左对齐 | 居中 | 右对齐 |  
|:------|:-----:|-----:|  
|col is |somen wordd yesd | $1234 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

###表格中嵌套图片

| 图片 | 描述 |
|------|-------|
|![2016090517430p102 3.jpg](http://7xwbzi.com1.z0.glb.clouddn.com/2016090517430.jpg) | [百度][baidu] |

----------------------------
[baidu]:https://www.baidu.com  '百度' 
