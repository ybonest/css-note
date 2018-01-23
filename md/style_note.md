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