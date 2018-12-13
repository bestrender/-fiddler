# H5打开摄像头

```
<input  type="file"  accept="image/*" multiple="multiple" capture="camera" /> 
```
capture表示，可以捕获到系统默认的设备，比如：camera照相机；camcorder摄像机；microphone录音。accept表示，直接打开系统文件目录。

```
<label>照相机</label>
<input type="file" id='image' accept="image/*" capture='camera'>
<br>
<label>摄像机</label>
<input type="file" id='video' accept="video/*" capture='camcorder'>
```
其实html5的input:file标签还支持一个multiple属性，表示可以支持多选

```
<input type="file" id="file" multiple>
```
在各个机型都可以点击 file 调用相册 和 摄像头拍照 
1. 在老版本的安卓中，必须加上capture，否则只能调用相册 
2. 在IOS中 加了capture，就只能调用摄像头不能调用相册


解决办法: 
判断ios，如果是ios就去掉capture属性.

```
var file = document.querySelector('input');
if (getIos()) {
    file.removeAttribute("capture");
}
function getIos() {
    var ua=navigator.userAgent.toLowerCase();
    if (ua.match(/iPhone\sOS/i) == "iphone os") {
        return true;
    } else {
        return false;
    }
}
```
这样不管安卓还是IOS都可以选择调用手机摄像头还是手机相册啦