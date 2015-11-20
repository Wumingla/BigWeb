## 音频播放

### Audio(音频）
HTML5提供了播放音频文件的标准

### control（控制器）
control属性供添加播放、暂停和音量控件。

### 标签：
* \<audio\>   定义声音
* \<source\>  规定多媒体资源，可以为多个

### PS:
```
<audio src="raw/xxx.mp3" controls="controls">您的浏览器不支持</audio>
```
* 自定义播放按钮
```
<script>
  var a = document.getElementById("audio");
  function clickA(){
    if(a.paused){
      a.play();
    }else{
      a.pause();
    }
  }
</script>
<audio id="audio" src="raw/xxx.mp3" >您的浏览器不支持</audio>
<button onclick="clickA()">播放/暂停</button>
```
## 编解码工具
不是所有浏览器都支持视频格式都是统一的，比如Chrome支持MP4，Safari和FFox支持的是OGG。

### 软件
* FFmpeg
* 官方网站：www.ffmpeg.org

### 使用软件
* 下载到本地
* 打开终端 cd /ffmpeg进入项目存放地址
* 终端输入 ./ffmpeg启动程序
* cd /进入需要编译文件的存放地址  
* 终端输入 ffmpeg项目存放地址/ffmpeg   -i  xx.mp4（例如:需要转译的文件名)  -acodec libvorbis xx.ogg(转译成的格式）

## 视频播放

### Video（视频）
HTML5提供了展示视频的标准

### control（控制器）
control属性供添加播放、暂停和音量控件

### 标签
* \<video\> 定义声音
* \<source\> 规定多媒体资源，可以使多个

### 属性
* width：宽
* height：高

### PS：
```
<video controls="controls" >
  <source src="raw/xxx.mp4">
  <source src="raw/xxx.ogg">
  您的浏览器不支持
</video>
```
* 自定义控件
```
<button onclick="clickV()">播放/暂停</button>
<button onclick="clickB()">放大</button>
<button onclick="clickS()">缩小</button>
<video id="video">
  <source src="raw/xxx.mp4">
  <source src="raw/xxx.ogg">
  您的浏览器不支持
</video>
<script>
  var v = document.getElementById("video");
  function clickV(){
    if(v.paused){
      v.play();
    }else{
      v.pause();
    }
  }
  function clickB(){
    v.width = 800;
    v.height = 800;
  }
  function clickS()}
    v.width = 300;
    v. height = 300;
  }
```

