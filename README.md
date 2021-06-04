# Flex

Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。



.box{
    display: flex; 
    display: inline-flex; 行内元素也可以使用 Flex 布局。
}



Webkit内核


.box{
    display: -webkit-flex;
    display: flex;
}


注意，设为 Flex 布局以后，子元素的float、clear和vertical-align属性将失效



容器属性:

    
    .flex-direction  排列方式
    .flex-wrap  换行
    .flex-flow    flex-direction与flex-wrap结合
    .justify-content   在横向轴上的对齐方式 左/右对齐/居中/均匀间距/ 
    .align-items    在纵向轴上的对齐方式 上/下对齐/居中/均匀间距/ 
    .align-content  多行显示时在纵向轴上的对齐方式(多行显示生效)
    
    
flex-direction:


    .row 横向显示多个 从左到右
    .row-reverse 反转
    .column 纵向显示 从上到下
    .column-reverse 反转
    

flex-wrap: 


    .nowrap  不换行(默认)
    .wrap 换行, 第一行在上方
    .wrap-reverse 换行,第一行在下方


flex-flow:

    .row nowrap   横向排列不换行(默认)
    .row wrap   横向排列换行
    .row-reverse nowrap  反转横向排列不换行
    ...
    
    
justify-content:

    .flex-start   左对齐
    .flex-end 右对齐
    .center  水平居中
    .space-between 两端对齐，项目之间的间隔都相等
    .space-around 每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍



align-items:

    .flex-start: 居上对齐
    .flex-end: 巨下对齐
    .center: 垂直居中
    .baseline: 项目的第一行文字的基线对齐。
    .stretch: （默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。


align-content:

    .flex-start: 整体居上对齐显示
    .flex-end:整体巨下对齐显示
    .center: 整体垂直居中对齐
    .space-between: 与交纵向轴两端对齐，轴线之间的间隔平均分布。
    .space-around: 每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
    .stretch（默认值）：轴线占满整个交叉轴。





项目的属性

    
