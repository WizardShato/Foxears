# Gitbook

1.在使用GitBook 之前, 我们需要先安装一些必须的工具，Node.js、GitBook、GitBook Editor、Git版本控制器。

2.GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书。通过Node.js命令安装GitBook

安装gitbook CLI

> 想在系统上的任何地方的gitbook命令，需要安装“gitbook CLI”，执行以下命令
>
> //安装命令  
> npm install -g gitbook-cli  
> //卸载命令  
> npm uninstall -g gitbook

NMP安装Gitbook

> npm install gitbook -g

检验下是否安装成功

> gitbook -V //显示版本号



## GitBookEditor {#articleHeader5}

> GitBook官方客户端编辑器，支持Win、Linux、Mac系统。请点击下载GitBookEditor。使用该编辑器可以快速的创建、编辑GitBook。安装具有以下步骤：
>
> * 解压下载包 gitbook-editor-4.2.1-windows-ia32.zip
>
> * 运行GitBook Editor Setup.exe进行默认安装

# 基本使用 {#articleHeader6}

> GitBook 大致分为两种使用方式，即离线和在线。最简单的使用方式是使用GitBook Editor编辑GitBook ，然后使用相关命令编译成功HTML。当然还有以下几种方式
>
> * 使用命令创建基本GitBook
>
> * 使用网页在线编辑器创建、编辑GitBook。
>
> * 使用itBookEditor客户端创建、编辑GitBook。

## gitBookEditor {#articleHeader7}

> 使用客户端方式，支持在线和本地两种方式创建、编辑GitBook，再执行相关命令编译成HTML，这种方式比较方便，推荐使用。以本地创建书籍为例

1、gitBookEditor客户端基本使用

![](https://segmentfault.com/img/bVyKz5)

![](https://segmentfault.com/img/bVyKz9)

2、使用命令对已经创建的Book进行编译

> 找到需要编译的书籍所在目录，执行gitbook serve 命令,在本电脑的默认路径为C:UsersQGYGitBookLibraryImportgitbooksimpletutorial，如图所示

![](https://segmentfault.com/img/bVyKAb)

# 高级扩展 {#articleHeader8}

> 掌握了“基本使用”，但有时候想要gitBook更美观，或者更符合我们自己的需求，则通过book.json配置进行自定义、以及安装一些常用的插件等。

## Book.json配置 {#articleHeader9}

> GitBook 在编译书籍的时候会读取书籍源码顶层目录中的 book.js 或者 book.json，这里以 book.json 为例，参考 GitBook 文档 可以知道，book.json 支持如下配置

```
{

    //样式风格配置格式
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
     },

    //插件安装配置格式

    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
     }    
}
```

## 自定义插件扩展 {#articleHeader10}

> 插件是扩展GitBook功能最好的方法。使得GitBook功能更加强大，例如，把数学公式显示支持，跟踪回访使用谷歌解析，…以toggle-chapters插件为例toggle-chapters 插件的效果是默认只在目录导航中显示章的标题，而不会显示小节的标题，点击每一章或者每一节会显示当前章或节的子目录，如果有的话，但是同时会收起其它之前展开的章节。所以，个人认为不是非常实用，因为这样子用户不能快速跳转到没有展开的章节！

一、搜索、安装插件方式

1、编辑器方式（没成功）

![](https://segmentfault.com/img/bVyKAo)

2、通过GitHub方式

> www.plugins.gitbook.com

3、node.js命令方式

* 默认安装在以下路径

```
C:\Users\QGY\AppData\Roaming\npm\node_modules
```

* 把插件文件夹复制到

```
npm install gitbook-plugin-toggle-chapters--save-dev
```

二、通过Book.json配置插件

```
"plugins": ["toggle-chapters"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
     }
```



原文地址：[https://segmentfault.com/a/1190000005859901](https://segmentfault.com/a/1190000005859901)

