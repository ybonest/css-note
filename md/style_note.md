## CSS属性
+ 默认情况下，在chrome中文最小为12px，设置`-webkit-text-size-adjust:none`


## 清除浮动
+ 为父元素设置高度
+ 在结尾处加空的兄弟div标签，并添加标签属性`clear:both`
+ 为父元素增加伪类
```
.clearfix:after{
    content:"";
    display:block;
    visibility:hidden;
    height:0;
    line-height:0;
    clear:both;
}
.clearfix{
    zoom:1
}
```
原理：IE8以上和非IE浏览器才支持，而zoom(IE专有属性)可以解决ie6，ie7浮动问题

### 水平垂直居中的几种方式
+ absolute+transform：绝对定位+转换
```
<div class="parent">
    <div class="child">Demo</div>
</div>
<style>
    .parent{
        position:relative;
    }
    .child{
        position:absolute;
        left:50%;
        top:50%;
        transform:translate(-50%,-50%);
    }
</style>
```

+ inline-block + text-align + table-cell + vertical-algin
```
<div class="parent">
    <div class="child">Demo</div>
</div>
<style>
    .parent{
        text-align:center;
        display:table-cell;
        vertical-align:middle;
    }
    .child{
        display:inline-block;
    }
</style>
```

+ flex + justify-content + align-items(弹性模型)
```
<div class="parent">
    <div class="child">Demo</div>
</div>
<style>
    .parent{
        display:flex;
        justify-content:center;
        align-items:center;
    }
</style>
```