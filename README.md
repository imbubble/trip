# trip

移动端经验速递

## 概要

本文档针对移动前端开发，包括 `Hybrid` 里面的web页面，非 `Native` 应用。

## 适用

所有经验适用于：`iOS6.0+`, `Android4.0+`

## 目录

* [兼容性](#compatibility)
	* [CSS伪类:active](#active)
* [经验](#experience)
	* [禁止保存或拷贝图像](#touch-callout)
	* [取消touch高亮](#tap-highlight-color)
* 待续...

<a name="compatibility"></a>
## 兼容性

<a name="active"></a>
### CSS伪类:active

如果你想使用元素的伪类来实现激活状态，那么你需要知道以下问题：

1. iOS（非PC）上任何元素的伪类 `:active` 都无效；
2. Android上，`Android Browser` 和 `Chrome` 都支持伪类 `:active` ，其它第三方浏览器基本上都不支持；


<a name="experience"></a>
## 经验

<a name="touch-callout"></a>
### 禁止保存或拷贝图像

通常当你在手机或者pad上长按图像 `img` ，会弹出选项 `存储图像` 或者 `拷贝图像`，如果你不想让用户这么操作，那么你可以通过以下方法来禁止：

	img {
		-webkit-touch-callout: none;
	}

需要注意的是，该方法只在 `iOS` 上有效。

<a name="tap-highlight-color"></a>
### 取消touch高亮

在移动设备上，所有设置了伪类 `:active` 的元素，默认都会在激活状态时，显示高亮框，如果不想要这个高亮，那么你可以通过以下方法来禁止：

	.xxx {
		-webkit-tap-highlight-color: rgba(0, 0, 0, 0);
	}