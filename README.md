# HTML-summary
HTML(包含HTML5)相关的总结

```
outerHTML与innerHTML的区别, 获取一个元素el的outerHTML和innerHTML，outerHTML返回的是带有el元素本身和字节点元素的字符串，innerHTML返回的是带有el的字节点元素的字符串
```
### 1、元素尺寸
#### 1.偏移尺寸（offsetLeft、offsetTop、offsetHeight、offsetWidth）offset偏移
```
偏移尺寸，包含元素在屏幕上占用的所有视觉空间。
元素在页面上的视觉空间由其高度和宽度决定，包括所有内边距（padding）、滚动条和边框（但不包含外边距（margin））。以下4个属性用于取得元素的偏移尺寸。
offsetTop，元素上边框外侧距离包含元素上边框内侧的像素数。(不包括元素上边框的高度)
offsetLeft，元素左边框外侧距离包含元素上边框内侧的像素数。(不包括元素左边框的宽度)
offsetHeight，元素在垂直方向上占用的像素尺寸，包括它的高度、水平滚动条高度（如果可见）和上下边框的高度。offsetHeight = 上下border + 上下padding + height
offsetWidth，元素在水平方向上占用的像素尺寸，包括它的宽度、垂直平滚动条宽度（如果可见）和左右边框的宽度。offsetWidth = 左右border + 左右padding + width

其中offsetTop和offsetLeft是相对于包含元素的，包含元素保存在offsetParent属性中。
```
### 2、客户端尺寸
```
元素的客户端尺寸，包含元素内容及其内边距所占用的空间。客户端尺寸只有两个相关属性：clientWidth和clientHeight。（不包含边框border）
clientWidth：是内容区宽度加左、右内边距宽度。clientWidth = 左右padding + width
clientHeight：是内容区高度加上、下内边距高度。clientWidth = 上下padding + height

客户端尺寸实际就是元素内部的空间，因此不包含滚动条占用的空间。这两个属性最常用于确定浏览器视口尺寸，即检测document.documentElement的clientWidth和clientHeight。这两个属性表示视口（<html>或<body>元素）的尺寸。

注意：与偏移尺寸一样，客户端尺寸也是只读的，而且每次访问都会重新计算。
```
### 3、滚动尺寸
```
滚动尺寸，提供了元素内容滚动距离的信息。有些元素，比如<html>无需任何代码就可以自动滚动，而其他元素则需要使用CSS的overflow属性令其滚动。滚动尺寸相关的属性有如下4个：
scrollHeight: 没有滚动条出现时，元素内容的总高度。
scrollLeft: 内容区左侧隐藏的像素数，设置这个属性可以改变元素的滚动位置。
scrollTop: 内容区顶部隐藏的像素数，设置这个属性可以改变元素的滚动位置。
scrollWidth: 没有滚动条出现时，元素内容的总宽度。
```
### 4、确定元素尺寸
```
浏览器在每个元素都暴露了getBoundingClientRect()方法，返回一个DOMRect对象，包含6个属性：left、top、right、bottom、height和width。这些属性给出了元素在页面中相对于视口的位置。
```
