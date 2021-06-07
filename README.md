# Flex

#### Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。

    .box{
        display: flex; 
        display: inline-flex; 行内元素也可以使用 Flex 布局。
    }


#### Webkit内核

    .box{
        display: -webkit-flex;
        display: flex;
    }


##### 注意，设为 Flex 布局以后，子元素的float、clear和vertical-align属性将失效



## 容器属性:

    .flex-direction  排列方式
    .flex-wrap  换行
    .flex-flow    flex-direction与flex-wrap结合
    .justify-content   在横向轴上的对齐方式 左/右对齐/居中/均匀间距/ 
    .align-items    在纵向轴上的对齐方式 上/下对齐/居中/均匀间距/ 
    .align-content  多行显示时在纵向轴上的对齐方式(多行显示生效)
    
    
### flex-direction:


    .row 横向显示多个 从左到右
    .row-reverse 反转
    .column 纵向显示 从上到下
    .column-reverse 反转
    

### flex-wrap: 


    .nowrap  不换行(默认)
    .wrap 换行, 第一行在上方
    .wrap-reverse 换行,第一行在下方


### flex-flow:

    .row nowrap   横向排列不换行(默认)
    .row wrap   横向排列换行
    .row-reverse nowrap  反转横向排列不换行
    ...
    
    
### justify-content:

    .flex-start   左对齐
    .flex-end 右对齐
    .center  水平居中
    .space-between 两端对齐，项目之间的间隔都相等
    .space-around 每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍



### align-items:

    .flex-start: 居上对齐
    .flex-end: 巨下对齐
    .center: 垂直居中
    .baseline: 项目的第一行文字的基线对齐。
    .stretch: （默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。


### align-content:

    .flex-start: 整体居上对齐显示
    .flex-end:整体巨下对齐显示
    .center: 整体垂直居中对齐
    .space-between: 与交纵向轴两端对齐，轴线之间的间隔平均分布。
    .space-around: 每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
    .stretch（默认值）：轴线占满整个交叉轴。





## 项目的属性

    .order  属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。
    .flex-grow 属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。
    .flex-shrink 属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
    .flex-basis 属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。
    .flex 是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。
    .align-self 属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。
    
    
### order
    .item{
        order: <integer>;
    }


### flex-grow
    .item{
        flex-grow: <number>; /* default 0 */
    }
##### 如果所有项目的flex-grow属性都为1，则它们将等分剩余空间（如果有的话）。如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍。



### flex-shrink
    .item{
        flex-shrink: <number> /* default 1 */
    }
##### 如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小。如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小。

##### 负值对该属性无效。



### flex-basis
    .item{
        flex-basis: <length> | auto; /* default auto */
    }
##### 它可以设为跟width或height属性一样的值（比如350px），则项目将占据固定空间。



### flex
    .item{  
        flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
    }
##### 该属性有两个快捷值：`auto`  `(1 1 auto)` 和` none` `(0 0 auto)`。
##### 建议优先使用这个属性，而不是单独写三个分离的属性，因为浏览器会推算相关值。



### align-self
    item{
        align-self: auto | flex-start | flex_end | center | baseline | stretch
    }
##### 该属性可能取6个值，除了auto，其他都与align-items属性完全一致。
