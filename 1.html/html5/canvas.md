## Canvas标签
＊ HTML5\<canvas\>元素用于图形的绘制，通过脚本（通常是javascript来完成）
＊ \<canvas\>���标签只是图形容器，必须通过脚步来绘制图形。
＊ 你可以通过多种方法使用canvas绘制路径、盒、圆、字符以及添加图像。
```
* 使用html代码创建canvas：（一般极少使用）
<style>
  .canvas{
    background-color:red;
  }
</style>
<canvas class="canvas" width="200px" height="200px"></canvas>
```
＊ 使用javascript脚本创建canvas：
```
var  CANVAS_WIDTH =200 , CANVAS_HEIGHT =200;
window.onload= function(){
  creatCanvas();
}
fuction createCanvas(){
  document.body.innerHTML ="<canvas id=\"mucanvas\" width=\" "+CANVAS_WIDTH+" "\ height=\" "+CANVAS_HEIGHT+" "\></canvas>";
}
```

