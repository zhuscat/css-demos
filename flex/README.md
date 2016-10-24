### 布局类型
1. 传统的布局类型：基于盒装模型，依赖 `display` 属性， `poisiton` 属性和 `float` 属性。
2. Flex 布局。
3. 最近看到了一个 grid 布局，只是看到标题，没有去了解。

### 知识点

设置 Flex 布局之后，子元素 `float`, `clear`, `vertical-align` 失效。

水平主轴(main axis), 垂直交叉轴(cross axis)。

主轴开始位置叫做 `main start`。

结束位置叫做 `main end`。

交叉轴开始位置叫做 `cross start`。

结束位置叫做 `cross end`。

单个项目占据主轴空间叫做 `main size`。占据交叉轴空间叫做 `cross size`。

### Flex 布局的几个属性(设置在容器上)

```
flex-direction
flex-wrap
flex-flow
justify-content
align-items
align-content
```

这里要注意一下 `align-content`，当只有一行的时候，`align-content` 无效。

align-items 与 align-content 的区别：参考 https://github.com/banricho/webLog/issues/10

### 设置在项目上

```
order
flex-grow
flex-shrink
flex-basis
flex
align-self
```

#### order

定义排列顺序

#### flex-grow

项目的放大比例：默认为0，如果存在剩余空间，也不放大

#### flex-shrink

项目的缩小比例：默认为1，即如果空间不足，则缩小项目

#### flex-basis

分配多余空间之前，项目占据主轴空间。浏览器根据这个属性，计算主轴是否有多余空间。默认值是 auto，即项目本来的大小。

#### flex

一个复合属性: 由 `flex-grow`，`flex-shrink`，`flex-basis` 组成。默认为 `0 1 auto`，后两个属性可选。

两个快捷值：`auto`(`1 1 auto`) `none`(`0 0 auto`)

#### align-self

允许单个项目跟其他项目有不同的对齐方式，默认为 `auto`，表示集成父元素的 `align-items` 属性。如果没有父元素，则为 `stretch`。
