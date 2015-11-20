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
#### url类型
* url类型的input元素是一种专门用来输入url地址的文本框。提交时如果该文本框中的内容不是url地址格式的文字，则不允许提交。
* 非url提交时Firefox、Chrome 提示错误，Opera自动将url框中值转化为url格式，ie9和safari不支持，正常提交

#### email类型
* email类型的input元素是一种专门用来输入email的文本框。提交时如果该文本框中的内容不是email地址格式的文字则不允许提交，但是它并不检查email地址是否存在，提交时该文本框可以为空，除非加上了 required 属性。
* email类型的文本框具有一个 multiple 属性——它允许在该文本框中输入一串以逗号分割的email地址。当然并不强制要求用户输入该email地址列表。
* Firefox、Chrome、Opera 非email提交时提示错误，支持required，ie9和safari不支持，正常提交

#### date类型
* date类型的input元素是深受开发者喜爱的一种元素我们也经常看到网页中要求我们输入的各种各样的日期，例如生日、购买日期、订票日期等。date类型的input元素以日历的形式方便用户输入。当该文本框获取焦点时，显示日历，可以在日历总选择日期进行输入。
* Opera点击弹出一个日历下拉框，但不允许手动输入。Chrome、Safari表现一致，但Safari在提交时没有验证，在输入框右侧有上下两个按钮，点击加减天，Firefox、ie9不支持

#### time类型
* time类型的input元素是一种专门用来输入时间的文本框，并且在提交时会对输入时间的有效性进行检查。它的外观取决于浏览器。
* Opera类似系统的时间设置框。Chrome、Safari表现一致，但Safari在提交时没有验证，在输入框右侧有上下两个按钮，点击加减分钟，Firefox、ie9不支持

#### datetime类型
* datetime类型的input元素是一种专门用来输入UTC日期和时间的文本框，并且在提交时会对输入的日期和时间进行有效性检查。
* Opera支持的最好，很类似date和time的组合。Chrome、Safari表现一致，但Safari在提交时没有验证，在输入框右侧有上下两个按钮，点击加减分钟，Firefox、ie9不支持

#### datetime-local类型
* datetime-local类型的input元素是一种专门用来输入本地日期和时间的文本框，并且在提交时会对输入的日期和时间进行有效检查。
* Opera中和datetime表现上的区别就是末尾少了个UTC。Chrome、Safari表现一致，但Safari在提交时没有验证，Firefox、ie9不支持

#### month类型
* month类型的input元素是一种专门用来输年月份的文本框，并且在提交时会对输入的月份进行有效检查。
* Opera中和date类似，只是只能选择到月份。Chrome、Safari表现一致，但Safari在提交时没有验证，Firefox、ie9不支持

### week类型
* week类型的input元素是一种专门用来输周号的文本框，并且在提交时会对输入的周号进行有效检查。
* Opera提供下拉选择，不允许手动输入。Chrome、Safari表现一致，但Safari在提交时没有验证，Firefox、ie9不支持

#### number类型
* number类型的input元素是一种专门用来输数字的文本框，并且在提交时会对输入的内容是否为数字。它们具有 min、max 与 step 属性。 带有数值控制按钮，以控制其数值，使之不超过最大值于最小值，同时在点击该数值控制按钮时，其中的数值会按step属性进行增减，当然也可以直接在其中输入数字。
* Opera、Chrome、Safari表现一致，但Safari在提交时没有验证，Firefox、ie9不支持

#### range类型
* range类型的input元素是一种只允许输入一段范围内数值的文本框，它具有min属性与max属性，可以设定最小值与最大值（默认为0与100），它还具有step属性，可以制定每次拖动的维度，用滑动条的方式进行值的制定。
* Opera中滑条带刻度、Chrome、Safari不带，Firefox、ie9不支持

#### search类型
* search类型的input元素是一种专门用来输入搜索关键词的文本框的文本框。search类型与text类型仅仅在外观上有却别。在Safari浏览器中，它的外观为操作系统默认的圆角矩形文本框，但这个外观可以用css央视表进行改写。在其他浏览器中，TA的外观暂与text类型的文本框外观相同，但可以用css样式表进行改写。（-webkit-appearance:textfield）
* Safari和Chrome在输入框有内容时会默认在输入框右边出现一个×

#### tel类型
* tel类型的input元素被设计为用来输入电话号码的专用文本框。它没有特殊的校验规则，不强制输入数字（因为许多电话号码通常带有其他文字），譬如86-010-86670831.但是开发者可以通过 pattern属性来制定对于输入的电话号码格式的验证。
* Safari和ie不支持

#### color类型
* color类型的input元素用来选取颜色，它提供了一个颜色选取器。
* Safari和ie不支持

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

#### AutoComplete
帮助输入所用的自动完成功能，是一个既节省输入时间又十分方便的功能。在HTML5之前，因为谁都可以看见输入的值，所以在安全方面存在缺陷，只要使用AtuoComplete属性，安全性方面也可以得到很好的控制。

#### pattern
在HTML5中，对input元素使用pattern属性，并且将属性值设为某个格式的正则表达式，在提交时会针对这些进行检查，检查内容是否符合给定格式。当输入的内容不符合给定格式时，则不允许提交，同时在浏览器中显示信息提示文字，提示输入的内容必须符合给定格式。

#### SelectionDirection
这个对input元素与textarea元素，HTML5增加了SelectionDirection属性。当用户在这两个元素中用鼠标选取部分文字时，可以使用该属性来获取选取方向。当用户正向选取文字时，改属性值为"forward"，当用户反向选取文字时，改属性值为"backward"。当用户没有选取任何文字，该属性值为"forward"。

#### indeterminate
对于复选框checkbox元素来说，过去只是选取与非选取这两种状态。在HTML5中，可以在JavaScript脚本代码中对该元素使用indeterminate属性，以说明复选框处于“尚未明确是否选取”状态。
```
<input type="checkbox" indeterminate id="cb">属性测试
<script>
  var cb = document.getElementById("cb");
  cb.indeterminate = true;
</script>
```
#### image提交按钮的height属性与width属性
针对类型为image的input元素，HTML5新增了两个属性，height、width分别用来指定图片按钮的高度和宽度。

## 全局属性
* contentEditable 属性 ~内容是否可被编辑
* designMode 属性      ~全局内容是否可被编辑
* hidden 属性          ~隐藏
* spellcheck 属性      ~检测拼写是否正确
* tabindex 属性        ~切换顺序

## 增强的页面元素
#### figure 与 figcaption
一种组合元素，带有可选标题。用来表示网页上一块独立的内容，将其移除不会对其他内容产生影响。figure所表现得内容可以使图片、统计图、或者代码事例。figcaption元素表示figure元素的标题，从属于figure元素的内部。一个figure元素最多只允许放置一个figcaption元素，但是允许放置多个其他元素。
```
<figure>
    <figcation>标题/整体的描述</figcation>
    <img src="xxx.png">
    <img src"aaa.png">
</figure>
```
#### details 与 summary
details元素是用来标识改元素内部的子元素可以被展开收缩形式的元素。内部不仅限制于放置文字，还可以放置表单、插件或者是统计图的详细数据。summary元素从属于details元素，当用鼠标单击summary元素的文字内容时，details所有的从属元素会被展开，或者收缩。如果没有填写summary元素，浏览器会默认提供文字。
```
<script>
    function detail_onclick(detail){
      var p = document.getElementById("p");
      if(detail.open){
        p.style.visibility="hidden";
      }else{
        p.style.visibility="visible";
      }
    }
  </script>
      
<details id="detail" onclick="detail_onclick(this)">
  <summary>更多详情</summary>
  <p id="p" style="visiblility:hidden">我是详情</p>
</details>
```
#### mark
表示页面中需要突出显示或者高亮显示，对于当前具有参考作用的文字。有一个着重或者说是高亮的效果。背景有颜色。
```
<p>这是一段文字用来测试<mark>mark元素</mark></p>
```

#### progress
progress元素代表任务的完成进度，这个进度可以使不确定的，表示进度正在执行，或者不清楚当前工作量有没有完成。也可以使用数值来表示完成进度的一个情况。
```
<script>
    function btn(){
      var i = 0;
      function thread_one(){
      if(i<=100){
        i ++;
        updateprogress(i);
      }
      setInterval(thread_one,100);
    }
    function updateprogress(newValue){
        var progressBar = document.getElementById("p");
        progressBar.value = newValue;
        progressBar.getElementsByTagName("span")[0].textContent = newValue;
    }
<section>
    <h2>pregress元素的使用</h2>
    <p>完成的百分比<progress id="p" background-color="red"  max="100"><span>0</span>%</progress></p>
    <input type="button" onclick="" value="点击">
</section>
```
#### meter
meter元素表示规定范围内的数值量。
````
<meter value="40" min="0" max="100" low="10" high="90" optimum="80"></meter>
````
#### ol
在HTML5中为ol添加了start 和 reversed 属性。start 表示从哪里开始，reversed 表示倒叙。
```
<ol start="5" reversed>
    <li>列表1</li>
    <li>列表2</li>
    <li>列表3</li>
    <li>列表4</li>
    <li>列表5</li>
</ol>
```
#### dl
在HTML5中对dl进行重新定义，表示多个名字的列表项，每项下面都带有一条或多条的dt元素用来表示术语。dt元素后面紧跟着一个或多个dd元素。在一个元素内不能允许有相同名字的dt元素重复术语。
```
<dl>
    <dt>hello</dt>
    <dd>你好就是hello</dd>
    <dt>博客</dt>
    <dd>你喜欢博客</dd>
</dl>
```
#### cite
cite元素表示一篇文文章、一首歌的一个标题，该作品可以在页面中被详细应用。有斜体效果。
```
<h3>cite元素</h3>
<p>我最喜欢的电影是<cite>速度与激情</cite></p>
```
#### small
在HTML5中对small元素进行了重新的定义，由通用的改为专门用来标识小字印刷体的元素。不允许应用在页面的主体内容中，只允许被当做额外信息以依赖方式内嵌在页面中使用。并不意味着结构字号会改变，如果要改变字号还是要css样式配合来实现。





