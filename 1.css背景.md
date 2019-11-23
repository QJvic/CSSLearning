# css背景

## 背景颜色

例子:
```css
background-color: red;
```

## 背景图片

background-image。优点是便于控制位置。

语法：

```css
background-image: none|url
```

例：

```css
/**注意不要落下url（）**/
background-image: url(images/logo.pnh);
```

### 背景平铺

语法:

```css
background-repeat: repeat|no-repeat|repeat-x|repeat-y
```

默认情况下背景是平铺的。

**页面元素既可以添加背景图片也可以添加背景颜色，背景图片会压住背景颜色。**

### 背景图片位置

background-position修改图片在背景中的位置

语法：

```css
background-position: x y;
```

x坐标和y坐标，可以使用方位名词也可以使用精确单位。

方位名词：top|center|bottom|left|right|center。

精确单位：百分数|由浮点数子和单位标识符组成的长度值。

1. 参数是方位名词
   - 如果指定的两个值都是方位名词，则两个值的前后顺序无关，比如 left top 和 top left效果一致；
   - 如果只指定了一个方位名词，另一个值省略，则第二个值默认居中对齐。

2. 参数是精确位置
   - 如果参数是精确单位，那么第一个肯定是x坐标，第二个一定是y坐标；
   - 如果只指定了一个参数，那么一定是x坐标，y坐标默认居中。

3. 参数是混合单位
   - 如果两种参数混合使用，那么第一个是x坐标，第二个 是y坐标。

### 背景图像固定（背景附着）

background-attachment属性设置背景图像是否固定或者随着页面的其余部门滚动，可以制作视差滚动的效果。

语法

```css
background-attachment: scroll | fixed
```

scroll：随着页面滚动。 默认

fixed：固定

## 背景复合写法

为了简化背景属性的代码，我们可以将这些属性合并简写到同一个属性background中。

一般习惯约定顺序为：

background: 背景颜色 背景图片地址 背景平铺 背景图像滚动  背景图片位置；

例：

```css
body {
    background: black url(images/bg.jpg) no-repeat scroll center center;
}
```

## 背景颜色半透明

语法：

```css
background: rgba(0,0,0,0.3);
```

