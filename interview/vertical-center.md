[原文地址](https://mp.weixin.qq.com/s/JL-9juZgbpz_Cnp6FnLVAQ)

# 垂直居中

1. line-height

*单行文字垂直居中技巧*
```
<div class="content">Lorem ipsam.</div>
.content{
  width: 400px;
  background: #ccc;
  line-height:100px;
  margin: auto;
}
```

2. line-height + inline-block

*多对象的垂直居中技巧*

```
<div class="box box2">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
  效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>

h2{
  text-align: center;
}
.box{
  width: 500px;
  border: 1px solid #f00;
  margin: auto;
  line-height: 200px;
  text-align: center;
}
.box2 .content{
  display: inline-block;
  height: auto;
  line-height:1;
  width: 400px;
  background: #ccc;
}
```

3. :before + inline-block

*多对象的CSS垂直居中技巧*

```
<h2>3.:before + inline-block</h2>
<div class="box box3">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>

h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  text-align: center;
}
.box::before{
  content:'';
  display: inline-block;
  height: 100%;
  width: 0;
  vertical-align: middle;
}
.box .content{
  width: 400px;
  background: #ccc;
  display: inline-block;
  vertical-align: middle;
}
```

4. absolute + margin 负值

*适用情景：多行文字的垂直居中技巧*

```
<h2>4.absolute + margin 負值</h2>
<div class="box box4">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>

h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  position: relative;
}
.box4 .content{
  width: 400px;
  background: #ccc;
  height: 70px;
  position: absolute;
  top:50%;
  left: 50%;
  margin-left: -200px;
  margin-top: -35px;
}
```

5. absolute + margin auto

*适用情景：多行文字的垂直居中技巧*

```
<h2>5.absolute + translate(-50%, -50%)</h2>
<div class="box box5">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  position: relative;
}
.content{
  width: 400px;
  background: #ccc;
  height: 70px;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
}
```

6. absolute + translate

*适用情景：多行文字的垂直居中技巧*

```
<h2>6.absolute + margin: auto</h2>
<div class="box box6">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  position: relative;
}
.box5 .content{
  width: 400px;
  background: #ccc;
  position: absolute;
  top:50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

7. Flex + align-items

*多行文字的垂直居中技巧*

```
<h2>7.Flex + align-items</h2>
<div class="box box7">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center; 
}
.content{
  width: 400px;
  background: #ccc;
}
```

8. flex + :before + flex-grow

*多行文字的垂直居中*

```
<h2>8.Flex + before + flex-grow</h2>
<div class="box box8">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.box:before{
  content: '';
  flex-grow: .5;
}
.content{
  width: 400px;
  background: #ccc;
}
```

9. Flex + margin

*多行文字的垂直居中技巧*

```
<h2>9.Flex + margin</h2>
<div class="box box9">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>

h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: flex;
}
.content{
  width: 400px;
  background: #ccc;
  margin: auto;
}
```


10. Flex + align-self

*多行文字的垂直居中技巧*

```
<h2>10.Flex + align-self</h2>
<div class="box box10">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: flex;
  justify-content: center;
}
.content{
  width: 400px;
  background: #ccc;
  align-self: center
}
```


11. Flex + align-content


*适用情景：多行文字的垂直居中技巧*

```
<h2>11.Flex + align-content</h2>
<div class="box box11">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-content: center;
}
.content{
  width: 400px;
  background: #ccc;
}
.box11:before,
.box11:after{
  content: '';
  display: block;
  width:100%;
}
```
12. Grid + template

*多行文字的垂直居中技巧*

```
<h2>12.Grid + template</h2>
<div class="box box12">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: grid;
  grid-template-rows: 1fr auto 1fr;
  grid-template-columns: 1fr auto 1fr;
  grid-template-areas: 
    '. . .'
    '. amos .'
    '. . .';
}
.content{
  width: 400px;
  background: #ccc;
  grid-area: amos;
}
```


13. Grid + align-items

*多行文字的垂直居中技巧*

```
<h2>13.Grid + align-items</h2>
<div class="box box13">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: grid;
  justify-content: center;
  align-items: center; 
}
.content{
  width: 400px;
  background: #ccc;
}
```

14. Grid + align-content

*杜航文字的垂直居中技巧*

CSS Grid的align-content跟Flex的align-content有点差异，CSS Grid对于空间的解释会跟Flex有一些些的落差，所以导致align-content在Flex中仅能针对多行元素起作用，但在Grid中就没这个问题，所以我们可以很开心的使用align-content来对子元素做垂直居中，丝毫不费力气

```
<h2>14.Grid + align-content</h2>
<div class="box box14">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: grid;
  justify-content: center;
  align-content: center; 
}
.content{
  width: 400px;
  background: #ccc;
}
```

15. Grid + align-self

*适用情景：多行文字的垂直居中技巧*

align-self 应该大家都不陌生，基本上就是对grid Y轴的个别对齐方式，只要对单一子层元素设置为align-self:center就能达成垂直居中的目的了

```
<h2>15.Grid + align-self</h2>
<div class="box box15">
  <div class="content">
    立马来看Amos实际完成的    
    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    
    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: grid;
  justify-content: center;
}
.content{
  width: 400px;
  background: #ccc;
  align-self: center;
}
```


16. Grid + place-items

*适用情景：多行文字的垂直居中技巧*

place-items这属性不知道有多少人用过，此属性是align-items与justify-items的缩写，简单的说就是水平与垂直的对齐方式，想当然的，设定center就能居中

```
<h2>16.Grid + place-items</h2>
<div class="box box16">
  <div class="content">
    立马来看Amos实际完成的    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: grid;
  height: 150px;
  margin: 0 auto;
  place-items: center;
}
.content{
  width: 400px;
  background: #ccc;
}
```

17. Grid + place-content


*适用情景：多行文字的垂直居中技巧*

place-content这属性有多少人用过，此属性是align-content与justify-content的缩写，简单的说就是水平与垂直的对齐方式，想当然的，设置center就能居中了

```
<h2>17.Grid + place-content</h2>
<div class="box box17">
  <div class="content">
    立马来看Amos实际完成的    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: grid;
  height: 150px;
  margin: 0 auto;
  place-content: center;
}
.content{
  width: 400px;
  background: #ccc;
}
``` 


18. Grid + margin


*适用情景：多行文字的垂直居中技巧*

继续用Grid来居中，由于Grid元素对空间解读的特殊性，我们只要在父层元素设定display:grid，接着在需要垂直居中的元素上设置margin:auto即可自动居中。怎么这描述似曾相识。

```
<h2>18.Grid + margin</h2>
<div class="box box18">
  <div class="content">
    立马来看Amos实际完成的    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  display: grid;
}
.content{
  width: 400px;
  background: #ccc;
  margin:auto;
}
```


19. Display：table-cell

*适用情景：多行文字的垂直居中技巧*

这一招我想有点年纪的开发者应该都有看过，当然像我这么嫩的开发者当然是第一次看到啦，这一招的原理在于使用 CSS display属性将div设置成表格的单元格，这样就能利用支持存储单元格对齐的vertical-align属性来将信息垂直居中

```
<h2>19.display: table-cell</h2>
<div class="box box19">
  <div class="content">
    立马来看Amos实际完成的    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
    text-align: center;
    display: table-cell;
  vertical-align: middle;
}
.content{
  width: 400px;
  background: #ccc;
  margin: auto;
}
```


20. calc

*适用情景：多行文字的垂直居中技巧*

Cale是计算机英文单词calculator的缩写，这个由微软提出的css 方法，真的是网页开发者的一个福音。我们竟然可以在网页中直接做计算，这真是太猛了，从此我们再也不用在那边绞尽脑汁的数学计算了，或是想办法用js来动态计算，我们可以很轻松的利用calc()这个方法，来将百分比及时且动态的计算出实际要的是什么高度，真可谓是划时代的一个方法啊，但这个方法需要注意的是大量使用的话，网页性能会是比较差的，所以请谨慎使用。

```
<h2>20.calc</h2>
<div class="box box20">
  <div class="content">
    立马来看Amos实际完成的    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
}
.content{
  width: 400px;
  background: #ccc;
  position: relative;
  top:calc((100% - 70px) / 2);
  margin:auto;
  height: 70px;
}
```


21. Relative + translateY

*适用情景：多行文字的垂直居中技巧*

这个技巧是利用了top:50%的招式，让你的元素上方能产生固定百分比的距离，接着让要居中的元素本身使用tanslateY的百分比来达成垂直居中的需求，translate是一个很棒的属性，由于translate的百分比单位是利用元素自身的尺寸作为100%，这样让我们要利用元素自身宽高做事变得方便很多。

```
<h2>21.relative + translateY(-50%)</h2>
<div class="box box21">
  <div class="content">
    立马来看Amos实际完成的    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
}
.content{
  width: 400px;
  background: #ccc;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
  margin: auto;
}
```


22. padding

*适用情景：多行文字的垂直居中技巧*

```
<h2>22.padding</h2>
<div class="box box22">
  <div class="content">
    立马来看Amos实际完成的    <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
      CSS3精美相册效果    </a>
    效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  border: 1px solid #f00;
  margin: auto;
  height: auto;
  padding: 50px 0;
}
.content{
  width: 400px;
  background: #ccc;
  margin: auto;
}
```


23. Write-mode


*适用情景：多行文字的垂直剧种技巧*

这个方式应该是比较少见到的有人使用的了，这个想法是被老友Paul所激发的，write-mode这个css属性的功能基本上跟垂直居中是八竿子打不着，它的用途是改变文字书写的方向从横变竖，且支持度从很早期的IE5就有支持了，但当时Amos很少使用，一来是网页多是横书较多，另外当时除了IE浏览器意外，其他浏览器的支持度都不是很好，也就很少使用了。

使用write-mode将一整个文字容器变成直书，接着将此容器利用text-align:center来达到垂直居中的目的，白话一点的解说就是，你把原本横排的文字变成竖排，所以原本横排用到的水平对齐方式，就变成了控制直排的中间了，原理就是这么简单。但要特别注意的是浏览器对此语法的支持度来说，需要拆开写法才行，不然某些浏览器的语法不同，可能会让你的网页在某些浏览器上看起来无效，这会是最需要注意到的

```
<h2>23.writing-mode</h2>立马来看Amos实际完成的
<div class="box box23">
  <div class="content">
    <div class="txt">
      立马来看Amos实际完成的      <a href="http://csscoke.com/2015/07/31/nth-child_rwd_album/">
        CSS3精美相册效果      </a>
      效果吧！別忘了拖拉一下窗口看看 RWD 效果喔！      這個置中的想法來自於 Paul     </div>
  </div>
</div>
h2{
  text-align: center;
}
.box{
  width: 500px;
  height: 250px;
  border: 1px solid #f00;
  margin: auto;
  writing-mode: tb-lr; /* for ie11 */
  writing-mode: vertical-lr;
  text-align: center;
  margin:0 auto;
}
.content{
  width: 400px;
  background: #ccc;
  display: inline-block; /* for ie & edge */
  width: 100%;
  writing-mode: lr-tb;
  margin: auto; 
  text-align: left;
}
.box .txt{
  width: 80%;
  margin: auto;
}
```
