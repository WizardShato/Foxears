# meta常用标签

meta元素共有三个可选属性（http-equiv、name和scheme）和一个必选属性（content），content定义与 http-equiv 或 name 属性相关的元信息

可选属性

| 属性 | 值 | 描述 |
| :---: | :---: | :---: |
| http-equiv | content-type / expire / refresh / set-cookie | 把content属性关联到HTTP头部。 |
| name | author / description / keywords / generator / revised / others | 把 content 属性关联到一个名称。 |
| sceme | some\_text | 定义用于翻译content属性值得格式 |

必选属性

| content | some\_text | 定义于http-equiv或name属性相关的元信息 |
| :---: | :---: | :---: |


name属性

```
<!-- 页面作者 -->
<meta name="author" content="author name" />
<!-- 页面描述 -->
<meta name="description" content="meta元素共有三个可选属性(不超过150字符)" />
<!-- 页面关键词 -->
<meta name="keywords" content="meta标签总结,meta标签" />
<!-- 页面生成器 -->
<meta name="generator" content="hexo" />
<!-- 页面修改信息 -->
<meta name="revised" content="story,2015/07/22" />
<!-- 版权信息 -->
<meta name="copyright" content="All Rights Reserved" />
<!-- 页面爬虫设置 -->
<meta name="robots" content="index,follow" />
<!-- robots的content取值 -->
<!-- all：文件将被检索，且页面上的链接可以被查询 -->
<!-- none：文件将不被检索，且页面上的链接不可以被查询 -->
<!-- index：文件将被检索 -->
<!-- follow：页面上的链接可以被查询 -->
<!-- noindex：文件将不被检索，但页面上的链接可以被查询 -->
<!-- nofollow：文件将被检索，但页面上的链接不可以被查询 -->
```

http-equiv

```
<!-- 字符编码 -->
<meta http-equiv="content-type" content="text/html;charset=UTF-8" />
<!-- 页面到期时间 -->
<meta http-equiv="expire" content="Wed,22Jul201511:11:11GMT" />
<!-- 页面重刷新，0秒后刷新并跳转 -->
<meta http-equiv="refresh" content="0;URL=''" />
<!-- cookie设置 -->
<meta http-equiv="set-cookie" content="cookie value=xxx;expires=Wed,22-Jul-201511:11:11GMT；path=/" />
<!-- 脚本类型 -->
<meta http-equiv="Content-Script-Type"Content="text/javascript">
<!-- 禁止从本地缓存中读取页面 -->
<meta http-equiv="Pragma"content="no-cache"> 
```

移动端

```
<meta name="viewport" content="width=device-width, initial-scale=1.0,maximum-scale=1.0, user-scalable=no"/>
<!-- viewport的content取值 -->
<!-- width：宽度（数值 / device-width）（200~10000，默认为980px） -->
<!-- height：高度（数值 / device-height）（223~10000） -->
<!-- initial-scale：初始缩放比例 （0~10） -->
<!-- minimum-scale：允许用户缩放到的最小比例 -->
<!-- maximum-scale：允许用户缩放到的最大比例 -->
<!-- user-scalable：是否允许用户缩放 (no/yes)  -->

<!-- uc强制竖屏 -->
<meta name="screen-orientation" content="portrait">
<!-- QQ强制竖屏 -->
<meta name="x5-orientation" content="portrait">
<!-- UC强制全屏 -->
<meta name="full-screen" content="yes">
<!-- QQ强制全屏 -->
<meta name="x5-fullscreen" content="true">
<!-- UC应用模式 -->
<meta name="browsermode" content="application">
<!-- QQ应用模式 -->
<meta name="x5-page-mode" content="app">

<!-- IOS启用 WebApp 全屏模式 -->
<meta name="apple-mobile-web-app-capable" content="yes" />
<!-- IOS全屏模式下隐藏状态栏/设置状态栏颜色 content的值为default | black | black-translucent  -->
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<!-- IOS添加到主屏后的标题 -->
<meta name="apple-mobile-web-app-title" content="标题">
<!-- IOS添加智能 App 广告条 Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=myAppStoreID, affiliate-data=myAffiliateData, app-argument=myURL">

<!-- 去除iphone 识别数字为号码 -->
<meta name="format-detection" content="telephone=no">
<!-- 不识别邮箱 -->
<meta name="format-detection" content="email=no">
<!-- 禁止跳转至地图 -->
<meta name="format-detection" content="adress=no">
<!-- 可以连写-->
<meta name="format-detection" content="telephone=no,email=no,adress=no">
```



