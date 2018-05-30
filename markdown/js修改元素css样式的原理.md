
##### 1.我们以下面的代码为例
##### 

```
<!DOCTYPE html>
<html>
<head>
		<meta charset="UTF-8">
		<title>cssText文本格式化与属性操作</title>
		<style>
			#one{
				width: 200px;
				height: 100px;
				border: 1px solid green;
			}
		</style>
	</head>
	<body>
		<div id="one">
			我是填充的内容
		</div>
		<script>
			var one=document.getElementById("one");
			one.onclick=function(){
			one.style.width="300px"; 
			}
		</script>
	</body>
</html>

```
在js代码理给one添加单击事件，让其宽度变为300px，实际上是通过给one添加了一个行内样式，即
```
<div class="one" style="width:300px"></div>
```
这样才使得one在单击时宽度由200px变为300px。

我们都知道，行内样式的优先级比css里面高，所以才会使one元素在单击时，让其宽度变为300px，而不是通过js代码去修改css里面的样式，下面我们验证一下这个说法，我们都知道在css中，在某个样式后面加上 **!important**，会把其优先级设置为最高，即是行内样式的优先级也低于它

```
#one{
		width: 200px !important;
		height: 100px;
		border: 1px solid green;
			}
```
当我们给one元素的width后面加上了 ！important后，我们再通过js单击one去改变其宽度时，发现并不起作用，这也从侧面证明了js改变元素样式是通过设置其行内样式，而不是css样式。

但是，我们可以通过 **cssText**属性来修改css样式，即便有**!important**,代码如下

```
<script>
	var one=document.getElementById("one");
	one.onclick=function(){
	    one.style.cssText="width:300px;";
	}
</script>
```

---



利用cssText属性，修改元素的css样式，写法和css样式相同，这样就可以通过js修改元素的css样式了。

 朱东帅/2018/05/30




