# First class

## HTML初体验

### HTML定义

html:超文本标记语言

超文本：链接

标记：标记也叫标签，带尖括号的文本

### 标签语法

`<strong>内容</strong>`

![image-20230508150328654](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150328654.png)

需要加粗的文字

- 标签成对出现，中间包裹内容

- <>里面放英文字母(标签名)

- 结束标签比开始标签多 /

- 拓展、

  - 双标签：成对出现的标签

  - 单标签：只有开始标签，没有结束标签

    - `br` 换行

    - `hr`水平线

### HTML基本骨架

![image-20230508150347066](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150347066.png)

- html:整个网页
- head：网页头部，用来存放给浏览器看的信息，例如CSS
  - title：网页标题

- body：网页主体，用来存放给用户看的信息，例如图片、文字

  

vscode快捷键：！(英文状态下的)配合回车键orTab键

### 标签的关系

#### 作用：

​        明确标签的书写位置，让代码格式更加整齐

- 父子关系（嵌套关系）

  ![image-20230508150407748](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150407748.png)

- 兄弟关系（并列关系）

  ![image-20230508150419690](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150419690.png)

- 代码格式

  - 父子关系：子级标签换行且缩进（Tab）

  - 兄弟关系：兄弟标签换行要对齐

    ![image-20230508150435805](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150435805.png)

### 注释

注释就是对代码的解释说明，能提高代码的可读性。

`<!--...-->`

在vscode，添加/删除注释的快捷键：`ctrl + /`

### 标题标签

一般用在新闻标题、文章标题、网页区域名称等等。

#### 标签名：

h1-h6（双标签）   

​        ![image-20230508150506403](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150506403.png)

其显示特点：

- 文字加粗
- 字号逐渐减小
- 独占一行

​      

经验：

- h1标签在一个网页中只使用一次，用来放新闻标题或者网页logo
- h2-h6没有使用次数的限制

​      

### 段落标签

一般用在新闻段落、文章段落等

#### 标签名

p（双标签）

显示特点：

- 独占一行
- 段落与段落之间存在间隙

### 换行和水平线标签

- 换行 `br`（单标签）

  ![image-20230508150528773](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150528773.png)

- 水平线 `hr`（）单标签

### 文本格式化标签

作用：为文本添加特殊格式，以突出重点。常见的文本格式：加粗、倾斜、下划线、删除线等。 

![image-20230508150546527](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150546527.png)

> 提示：strong、em、ins、del 标签自带强调含义（语义）。 

### 图像标签

作用：在网页中插入图片

```html
<img  src="图片的 URL">
```

src用于指定图像的位置和名称，是 <img> 的必须属性。 

#### 图像属性

![image-20230508150603457](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150603457.png)

#### 属性语法

* 属性名="属性值"
* 属性写在尖括号里面，标签名后面，标签名和属性之间用空格隔开，不区分先后顺序

![image-20230508150619718](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150619718.png)

### 路径

概念：路径指的是查找文件时，从**起点**到**终点**经历的**路线**。 

路径分类：

* 相对路径：从当前文件位置出发查找目标文件
* 绝对路径：从盘符出发查找目标文件
  * Windows 电脑从盘符出发
  * Mac 电脑从根目录出发

#### 相对路径

查找方式：从**当前文件位置**出发查找目标文件

特殊符号：

* **/** 表示进入某个文件夹里面          → 文件夹名/
* **. ** 表示当前文件所在文件夹           → ./
* **..** 表示当前文件的上一级文件夹 → ../   

![image-20230508150635150](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150635150.png)

#### 绝对路径

查找方式：Windows 电脑从盘符出发；Mac 电脑从根目录（/）出发

```html
<img  src="C:\images\mao.jpg">
```

> 提示
>
> 1. Windows 默认是 \ ，其他系统是 /，建议统一写为 / 
> 2. 特殊的绝对路径 → 文件的在线网址：<https://www.itheima.com/images/logo.png> "，应用场景：网页底部**友情链接**

### 超链接标签

作用：点击跳转到其他页面。 

```html
<a href="https://www.baidu.com">跳转到百度</a>
```

**href 属性值是跳转地址，是超链接的必须属性。**

超链接默认是在当前窗口跳转页面，添加 **target="_blank"** 实现**新窗口**打开页面。

拓展：开发初期，不确定跳转地址，则 href 属性值写为 **#**，表示**空链接**，页面不会跳转，在当前页面刷新一次。

```html
<a href="https://www.baidu.com/">跳转到百度</a>

<!-- 跳转到本地文件：相对路径查找 --> 
<!-- target="_blank" 新窗口跳转页面 --> 
<a href="./01-标签的写法.html" target="_blank">跳转到01-标签的写法</a>

<!-- 开发初期，不知道超链接的跳转地址，href属性值写#，表示空链接，不会跳转 -->
<a href="#">空链接</a>
```

### 音频

```html
<audio src="音频的 URL"></audio>
```

常用属性

![image-20230508150705362](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150705362.png)

> 拓展：书写 HTML5 属性时，如果属性名和属性值相同，可以简写为一个单词。 

```html
<!-- 在 HTML5 里面，如果属性名和属性值完全一样，可以简写为一个单词 -->
<audio src="./media/music.mp3" controls loop autoplay></audio>
```

### 视频

```html
<video src="视频的 URL"></video>
```

常用属性

![image-20230508150719007](https://gitee.com/liuhb-clanguage/picture/raw/master/png/image-20230508150719007.png)

```html
<!-- 在浏览器中，想要自动播放，必须有 muted 属性 -->
<video src="./media/vue.mp4" controls loop muted autoplay></video>
```

