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

#### header
header元素是一种具有引导和导航作用的结构元素，通常用来放置整个页面或者页面内的一个内容块的标题，但是也可以包含其他内容，例如数据表格、搜索表单或者相关logo图片。

#### footer
footer元素可以作为上层父级内容区块或是一个根区块的脚注。footer通常包括其相关区块的脚注信息，如作者、相关阅读链接以及版权信息等。

#### hgroup
hgroup元素是将标题及其子标题进行分组的元素。hgroup元素通常会将h1~h6元素进行分组，譬如一个内容块的标题及其子元素算一组。

#### address
address元素用来在文档中呈现联系信息，包括文档作者或者文档维护者的名字、他们的网站链接、电子邮箱、真实地址、电话号码等。address应该不只用来呈现电子邮箱或真实地址，还用来展示跟文档相关联系人的所有联系信息。

## 新增的其他元素
video、 audio、 embed、 mark、 progress、 meter、 time、 ruby、 rt、 canvas、 command、 details、 datalist、 datagrid、 keygen、 output、 menu

## 新增的input元素的类型
email、 url、 number、 range、 DatePickers

## 废除的元素
* 能使用CSS代替的元素：basefont、big、center、font、s、tt、u 等
* 不再使用frame框架
* 只有部分浏览器支持的元素
* 其他被废除的元素

## 表单新增属性
Form、Formaction、Formmethod、Formenctype、Formtarget、Autofocus、Required、Labels
#### form
* 在HTML4中，表单内的从属元素必须书写再表单内部。
* 在HTML5中，可以把他们书写再页面任何地方，然后为该元素指定一个form属性，属性值为该表单的id，这样就可以声明改元素从属于指定表单了。

#### formaction
* 在HTML4中，一个表单内的所有元素智能通过表单的action属性被统一提交到另一个页面。
* 在HTML5中可以为所有的提交按钮，增加不同的formaction属性，使单击不同的按钮可以将表单提交到不同的页面。

#### formmethod属性
* 在HTML4中，一个表单内只能有一个action属性用来对表单内所有元素统一指定提交页面，所以每个表单内页只有一个method属性来统一指定提交方法。
* 在HTML5中，可以使用formmethod属性来对每一个表单元素分别指定不同的提交方法。

#### formenctype
* 在HTML4中，表单元素具有一个enctype属性，该属性用于指定在表单发送到服务器之前应该如何对表单内的数据进行编码。
* 在HTML5中，可以使用formenctype属性对表单元素分别指定不同的编码方式。

#### formtarget
* 在HTML4中，表单元素具有一个target属性，改属性用于指定在何处打开表单提交后所需要加载的页面。
* 在HTML5中，可以对多个提交按钮分别使用formtarget属性来指定提交后在何处打开所需要加载的页面。

#### autofocrs
* 为文本框、选择框或按钮控件加上autofocus属性，当画面打开时，改控件自动获得光标焦点。

#### required
* HTML5中新增的required属性可以应用在大多数输入元素上，在提交时，如果元素中内容为空，则不允许提交，同时在浏览器中显示信息提示文字。

#### labels
在HTML5中，为所有可使用标签的表单元素、button、select元素等，定义一个labels属性，属性值为一个NodeList对象，代表改元素所绑定的标签元素所构成的集合。

#### control
在HTML5中，可以在标签内部放置一个表单元素，并通过该标签的control属性来访问该表单元素。

#### placeholder
placeholder是指当文本框处于未输入状态时显示的输入提示。当文本框处于未输入状态切未获取光标焦点时，模糊显示输入提示文字。

#### list
在HTML5中，为单行文本框增加了一个list属性，该属性的值为某个datalist元素的id。datalist元素也是HTML5中新增的元素，该元素类似于选择框，但是当用户想要设定的值不在选择列表之内，允许自行输入。datalist元素本身并不显示，而是当文本框获取焦点时以提示输入的显示方式。




####

## 全局属性
* contentEditable 属性 
* designMode 属性  
* hidden 属性
* spellcheck 属性
* tabindex 属性

