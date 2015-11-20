# HTML5编辑API之Range对象

## Range对象基本概念
一个Range对象代表页面上的一段连续的区域。通过Range对象，可以获取或修改网页上的任何区域。
* 通过使用 Range 对象所提供的方法实现一个鼠标选取内容，通过点击按钮打印出选中内容，当然注意在不同的浏览器下可选中的内容数量是不同的。
```
<script>
    function rageTest(){
      var html;
      showRangeDiv = document.getElementById("showRange");
      selection = document.getSelection();
      if(selection.rangeCount>0){
        html = "您选取了》" +selection.rangeCount+"《内容<br/>";
        for(var i=0;i<selection.rangeCont;i++){
          var range = selection.getRangeAt(i);
          html += "第" + (i+1) + "段内容为" + range+ "<br/>";
        }
        showRangeDiv.innerHTML = html;
      }
    }
  </script>
  <p>Selection对象与Range对象的使用</p>
  <input type="button" value="点击我" onclick="rangeTest()">
  <div id="showRange"></div>
  ```
  
## SelectNode、SelectNodeContents、deleteContents
* 包含 SelectNode、SelectNodeContents、deleteContents 方法，通过实例来了解每一个方法的使用。
```
<script>
    function deleteRangeContent(onlyContent){
      var div = document.getElementById("div");
      var rangeObj = document.createRange();
      if(onlyContent){
        rangeObj.selectNodeContents(div);
        rangeObj.deleteContents();
      }else{
        rangeObj.selectNode(div);
        rangeObj.deleteContents();
      }
    }
  </script>
  <div id="div" style="background-color:red; width:300px; height:50px">元素内容</div>
  <button onclick="deleteRangeContent(true)">删除内容</button>
  <button onclick="deleteRangeContent(false)">删除内容</button>
  ```
  
## setStart、setEnd
* setStart用于某个节点中的某个位置指定为range对象所代表区域的起点位置
* setStart用于某个节点中的某个位置指定为range对象所代表区域的终点位置
```
<srcipt>
    function deleteChar(){
        var div = document.getElementById("myDiv");
        var textNode = div.firstChild;
        var rangeObj = document.createRange();
        rangeObj.setStart(textNode,1);
        rangeObj.setStart(textNode,4);
        rangeObj.deleteContents();
    }
</script>
<div id="myDiv" style="color:red">
    这段文字是用来删除的
</div>
<button onclick="deleteChar()">删除文字</button>
```
## setStartBefort、setEndAfter
* setStartBefore()	把该范围的开始点设置为紧邻指定节点之前。
* setEndAfter()	    把该范围的结束点设置为紧邻指定节点的节点之后。
* 
* setStartAfter()	把该范围的开始点设置为紧邻指定节点的节点之后。
* setEndBefore()	把该范围的结束点设置为紧邻指定节点之前。
```
<script>
    function deleteRow(){
        var table = document.getElementById("myTable");
        if(table.rows.length >0){
            var row = table.rows[0];
            var rangeObj = document.createRange();
            rangeObj.setStartBefore(row);
            rangeObj.setEndAfter(row);
            rangeObj.deleteContents();
        }
    }
</script>
<table id="myTable" border="1" cellspacing="0" cellpadding="0">
    <tr>
        <td>内容1</td>
        <td>内容2</td>
    </tr>
        <tr>
        <td>内容3</td>
        <td>内容4</td>
    </tr>
        <tr>
        <td>内容5</td>
        <td>内容6</td>
    </tr>
</table>
<button onclick="deleteRow()">删除第一行</button>
```
## cloneRange
cloneRange用于当前的range对象进行复制，该方法返回当前range的对象。意味着可以做一个复制的功能。
```
<script>
    function cloneRange(){
        var rangeObj = document.createRange();
        rangeObj.selectNoteContents(document.getElementById("p"));
        var rangeClone = rangeObj.cloneRange();
        alert(rangeClone.toString());
    }
</script>
<p id="p">这里是随便书写的内容</p>
<button onclick="cloneRange()">克隆</button>
```
## cloneContents
用于在页面上增加一段HTML代码，并且将range对象所代表的区域中的HTML代码克隆追加到HTML代码之后。我们再页面有一段内容，我们点击那么我么就克隆岛这么一段内容在当前容器承载。
```
<script>
    function cloneContent(){
        var div = document.getElementById("div");
        var rangeObj = document.createRange();
        rangeObj.selectNodeContents(div);
        var docFrangMent = rangeObj.cloneContents();
        div.appendChild(docFrangeMent);
    }
</script>
<div id="div">
    你好吗？
    <br/>
    <button onclick="cloneContent()">克隆</button>
    <br/>
</div>
```
## extractContents
range对象所代表区域的HTML代码克隆到docFramgent对象里中。
```
<script>
    function moveContent(){
        var srcDiv = document.getElementById("srcDiv");
        var distDiv = document.getElementById("distDiv");
        var rangeObj = document.createRange();
        rangeObj.selectNodeContents(srcDiv)
        var docFragment = rangeObj.extractContents();
        disDiv.appendChild(docFragment);
        
    }
</script>
<div id="srcDiv" style="background-color:red; width:300px;height:50px">你好吗</div>
<div id="distDiv" style="background-color:orange; width:300px;height:50px"></div>
<button onclick="moveContent()">移动元素</button>
```

