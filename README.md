# HTML
花礼网仿制项目
### 使用到的技术：
HTML+CSS
### 编写项目过程中遇到的问题：
#### 1. input输入框在聚焦时出现黑色边框:
![alt 图片](readme_image/quastion_one.png)

	如何解决：使用focus伪类，在input输入框获得焦点时的outline边框线去除。
```
	input:focus{
		outline:none;
	}
```

#### 2.页面盒子高度塌陷：
	原因：元素中的子元素使用了浮动，使子元素脱离了文档流，并且父元素没有设置高度，使得父元素的高度为0，这必然会造成高度塌陷的问题。
	如何解决:给浮动的元素容器添加一个clearfix的class，并且使用:after伪元素实现之后会在元素后面添加一个看不见的块级元素（block）来清除浮动。
```
	clearfix::after{
		display:block
		content:"";
		clear:both;
	}
```