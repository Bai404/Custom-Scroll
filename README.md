# jQuery实现自定义滚动条

> jQuery事件对象

jQuery事件对象对原生事件的差异进行封装和修正，统一了事件对象的属性和方法。 jQuery.Event.originalEvent:指向原生事件
> jQuery事件对象属性

  event.type：获取事件的类型

  event.pageX 和 event.pageY：获取鼠标当前相对于页面的坐标

event.preventDefault() 方法：阻止默认行为

event.stopPropagation() 方法：阻止事件冒泡

event.which：获取在鼠标单击时，单击的是鼠标的哪个键

event.currentTarget : 在事件冒泡过程中的当前DOM元素

>元素属性

div.scrollTop "元素中的内容(文档内容)"超出"元素上边界"的那部分高度(像素数)

div.scrollLeft "元素中的内容(文档内容)"超出"元素左边界"的那部分宽度(像素数)

div.scrollHeight 获取元素的完整高度，以像素为单位

div.scrollWidth 获取元素的完整高度，以像素为单位

>jQuery提供的位置方法

scrollTop 获取匹配的元素集合中第一个元素的当前垂直滚动条的位置， 也就是"该元素中的内容"超出"该元素上边界"的那部分像素数

scrollTop(value) 设置每个匹配元素的垂直滚动条位置， 滚动条垂直位置和"元素中的内容"超出"元素上边界"的那部分像素数是相同的

position():

获取匹配元素相对父元素的偏移。返回的对象包含两个整形属性：top 和 left。使用position()方法时事实上是把该元素当绝对定位来处理，获取的是该元素相当于最近的一个拥有绝对或者相对定位的父元素的偏移位置。

>鼠标滚轮事件浏览器的差异

Firefox中滚轮事件DOMMouseScroll，其他浏览器滚轮事件是mousewheel 
$(element).on("mouseWheel","DOMMouseScroll",mouseWheelHandler)

>鼠标滚轮事件属性浏览器的差异
Firefox中使用detail属性，其他浏览器中使用wheeldelta属性 Firefox中属性取值±3(倍数)，其他浏览器中属性取值±120(倍数) Firefox负数表示向上，其他浏览器中正数表示向上

**滑块移动距离/滑块可移动距离 = 内容滚动高度/内容可滚动高度**
