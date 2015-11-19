# HTML 5
## 推出的理由及目标
HTML5的出现，是要把Web上存在的各种问题一并解决：
* Web浏览器之间兼容性很低
* 文档结构不够明显
* Web应用程序的功能受到了限制

## 语法的改变
* 内容类型，保持html后缀不变。
* DOCTYPE声明，html。
* 可以省略标记的元素
* 具有boolean的值得属性
* 省略引号

## 新增的元素
section、 article、 aside、 header、 hgroup、 footer、 nav、 figure
#### article
article 元素代表文档、页面或者应用程序中独立的、完整的、可以独自卑外部引用的内容。它可以使一篇博客或者报刊中的文章，一篇论坛帖子、一段用户评论或者独立的插件，或其他任何独立的内容。
* article元素是可以嵌套使用的。
* article元素可以用来表示插件。

#### section
section元素对于对网站或者应用程序中页面上的内容进行分块。一个seciton元素通常由内容及其标题组成。但section元素并非一个普通的容器元素；当一个容器需要被直接定义样式或者脚本定义行为时，推荐使用div而非section元素。
* 不要将section元素作为设置样式的页面容器
* 如果article元素、aside元素、nav元素更符合使用条件，那不要使用section元素。
* 没有标题内容不要使用section元素。

#### nav
nav元素是一个可以用作页面导航的链接组，其中的导航元素链接到其他页面或当期页面的其他部分。并不是所有的链接组都要被放进nav元素，只需要将主要的、基本的连接组放进nav元素即可。nav元素应用场景：
* 传统导航条
* 侧边栏导航
* 页面导航
* 翻页操作

#### aside
aside元素用来表示当前页面或文字的附属信息部分，它可以包含当前页面或主要内容相关的引用、侧边栏、广告、导航条，以及其他类似的有区别于主要内容的部分。

## 新增的其他元素
video、 audio、 embed、 mark、 progress、 meter、 time、 ruby、 rt、 canvas、 command、 details、 datalist、 datagrid、 keygen、 output、 menu

## 新增的input元素的类型
email、 url、 number、 range、 DatePickers

## 废除的元素
* 能使用CSS代替的元素：basefont、big、center、font、s、tt、u 等
* 不再使用frame框架
* 只有部分浏览器支持的元素
* 其他被废除的元素

## 全局属性
* contentEditable 属性 
* designMode 属性  
* hidden 属性
* spellcheck 属性
* tabindex 属性

