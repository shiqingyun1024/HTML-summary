# HTML-summary
HTML(包含HTML5)相关的总结

```
outerHTML与innerHTML的区别, 获取一个元素el的outerHTML和innerHTML，outerHTML返回的是带有el元素本身和字节点元素的字符串，innerHTML返回的是带有el的字节点元素的字符串
```
### 1、元素尺寸
#### 1.偏移尺寸（offsetLeft、offsetTop、offsetHeight、offsetWidth）
```
偏移尺寸，包含元素在屏幕上占用的所有视觉空间。
元素在页面上的视觉空间由其高度和宽度决定，包括所有内边距（padding）、滚动条和边框（但不包含外边距（margin））。以下4个属性用于取得元素的偏移尺寸。
offsetTop，元素上边框外侧距离包含元素上边框内侧的像素数。(不包括元素上边框的高度)
offsetLeft，元素左边框外侧距离包含元素上边框内侧的像素数。(不包括元素左边框的宽度)
offsetHeight，元素在垂直方向上占用的像素尺寸，包括它的高度、水平滚动条高度（如果可见）和上下边框的高度。
offsetWidth，元素在水平方向上占用的像素尺寸，包括它的宽度、垂直平滚动条宽度（如果可见）和左右边框的宽度。

其中offsetTop和offsetLeft是相对于包含元素的，包含元素保存在offsetParent属性中。
```
