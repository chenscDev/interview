# HTML

DOCTYPE是做什么用的?
文档声明描述DTD

# CSS基础

### 实现垂直居中的几种方式?;
### 左边固定宽度右边自适应?
### 分别在左右两侧显示div的几种方式?
### Css九宫格实现?
### 写一个循环播放的动画?

## 盒模型的理解?

### 两种:一种是标准盒模型,一种是ie盒模型
```
  /* 标准模型 */
  box-sizing:content-box;
  标准模型中，盒模型的宽高只是内容（content）的宽高
  /*IE模型*/
  box-sizing:border-box;
  IE模型中盒模型的宽高是内容(content)+填充(padding)+边框(border)的总宽高。
  
```

## @BFC --- 基本概念:
``
  基本概念:其全英文拼写为 Block Formatting Context 直译为“块级格式化上下文”。 BFC的作用是决定了元素如何对其内容进行定位，以及与其他元素的关系和相互作用。其通俗理解可以理解为一个BFC块就是一个独立的单位，其互不打扰。
``
## @BFC --- 原理规则:
``
  BFC元素垂直方向的边距会发生重叠;
  BFC区域不会与float box发生重叠;
  BFC在页面上是一个独立的容器,容器里元素与容器外元素互不影响;
  计算BFC高度的时候,float元素也会参与计算.
``
## @如何创建BFC:
``
  float值不为none;
  position的默认值不为static或者relative;
  display属性与table相关;
  Overflow:hidden;
``


## 移动端适配则怎么做的,能说出来几种?
``
响应式布局: 使用媒体查询
百分比布局: 使用百分比适应屏幕
Flex布局: 使用flex自动适应屏幕尺寸
rem或 em适配:
这两个都是相对单位,由浏览器转换像素值,不同的是rem相对根节点,em相对父节点;
动态适配: 窗口宽度 * 设计稿宽度 / rem倍数
Meta标签:属性 viewport min-scale max-scale no-scaleble
``



## 移动端适配则怎么做的,能说出来几种?
``
响应式布局: 使用媒体查询
百分比布局: 使用百分比适应屏幕
Flex布局: 使用flex自动适应屏幕尺寸
rem或 em适配:
这两个都是相对单位,由浏览器转换像素值,不同的是rem相对根节点,em相对父节点;
动态适配: 窗口宽度 * 设计稿宽度 / rem倍数
Meta标签:属性 viewport min-scale max-scale no-scaleble
``
## JS基础
``
原始数据类型:Boolean,Null,Undefined,Number,String,Symbol(es6);

对象:Object.

### let、var、const的区别?
Var 存在变量提升,不赋值也不会报错,打印是undefined,作用于函数作用域;
Let es6新增,不存在变量提升,必须赋值,否则会报错, 作用于块级作用域;
Const es6新增 用于定义一个常量,使用const声明的值不可被改变,但如果声明的是一个引用类型,可以改变该对象属性;
### 数据类型检测的几种方式?
检测基本类型可以使用 typeof ,typeof检测null时类型为object;
检测引用类型可以使用 instanceof 也可以使用 constructor,因为constructor指向他的构造函数;
严格检测数组可以使用Array.isArray()来检测;
### 常用的数组操作方法?
1. reduce(); 累加器
2. push(n); 尾部添加
3. pop(); 尾部删除
4. shift(); 头部删除
5. unshift(n); 头部添加
6. reverse(); 反向排序,会改变原数组
7. sort((a,b) => return a - b); 正向排序,会改变原数组
8. indexOf(n); 返回某个元素在数组内的下标
9. forEach(); 遍历数组 没有返回值(ie6-8不兼容)
10. map(); 遍历数组 支持return返回(ie6-8不兼容)
11. slice(开始, 结束); 截取数组中的一部分返回新数组,不会修改原数组
12. splice(开始, 结束, 新值); 从数组中添加/删除项目，然后返回被删除的项目,会修改原数组
13. filter(num => return xxx ): 使用指定的函数测试所有元素，并创建一个包含所有通过测试的元素的新数组。
### 返回一个10到一百的随机数?
Math.random()时返回0-1的随机数,包括0;
公式 Math.random()*可能出现的总数+第一个出现的数
Math.random()*90+10
### 扩展运算符的使用?
将一个数组转换为参数序列;
#### 应用
代替apply进行参数传递a(...arr)
合并数组[...arr,1,2,3]
取数组最大值 Math.max(...arr);

### requestAnimationFrame方法?
大多数电脑显示器的刷新频率是60Hz，大概相当于每秒钟重绘60次。而setTimeout和setInterval的问题是，它们都不精确。它们的内在运行机制决定了时间间隔参数实际上只是指定了把动画代码添加到浏览器UI线程队列中以等待执行的时间。如果队列前面已经加入了其他任务，那动画代码就要等前面的任务完成后再执行。
requestAnimationFrame采用系统时间间隔，保持最佳绘制效率，不会因为间隔时间过短，造成过度绘制，增加开销；也不会因为间隔时间太长，使用动画卡顿不流畅，让各种网页动画效果能够有一个统一的刷新机制，从而节省系统资源，提高系统性能，改善视觉效果
### 写一个方法去除前后空格?
```
function trim(str) {
  return str.relaace(/^\s*|\s*$/g,’’); 
}
```

## JS中阶

### 如何理解this?

全局函数中的this指向window,匿名函数据具有全局性, 因此this通常指向window
作为一个对象的方法调用的时候指向这个对象;
使用箭头函数的this指向当前定义的对象

### 基本类型和引用类型的区别?

基本类型是简单的数据段
引用类型是多种值组成的对象

### arguments是什么?

每一个function函数都有一个arguments属性,他是一个类数组,保存着函数的参数,
类数组不可以使用数组的方法,如果想使用数组方法,可以将类数组转换为数组,

*转换方法:*

Array.form()方法从一个类似数组或可迭代对象中创建一个新的数组实例。

扩展运算符 [...arguments]

### 谈谈垃圾回收机制?

Js具有自动垃圾回收机制,也就是说执行环境会负责管理代码执行过程中使用的内存,

**垃圾回收有两种实现机制:**

**标记清除**

标记清除是最常用的回收方式,当变量进入环境时(比如说声明一个变量),标记为进入环境,离开环境时,将其标记为离开环境;垃圾回收器会在运行的时候给存储在内存中的所有变量加上标记，然后去掉环境中的变量以及被环境中变量所引用的变量（闭包），在这些完成之后仍存在标记的就是要删除的变量了，因为环境中的变量已经无法访问到这些变量了，然后垃圾回收器相会这些带有标记的变量机器所占空间。

**IE的引用计数**

在低版本IE中经常会出现内存泄露，很多时候就是因为其采用引用计数方式进行垃圾回收。引用计数的策略是跟踪记录每个值被使用的次数，当声明了一个变量并将一个引用类型赋值给该变量的时候这个值的引用次数就加1，如果该变量的值变成了另外一个，则这个值得引用次数减1，当这个值的引用次数变为0的时候，说明没有变量在使用，这个值没法被访问了，因此可以将其占用的空间回收，这样垃圾回收器会在运行的时候清理掉引用次数为0的值占用的空间。

### Call,apply和bind的区别?

Call和apply都是在特定的作用域中调用函数改变this的执行环境,第一个参数都是运行函数的作用域,不同的是第二个参数call是将参数序列化传递,而apply是传递一个类数组或数组为参数;call和apply是立即执行的;
Bind是创建一个函数实例,并将this绑定到这个函数上,bind是想用的时候再去调用

### 手写一个bind函数?
```
function bind (context) {
  var self = this;
    return function () {
    self.apply(context,arguments);
  };
};
```

### 自执行函数?

``(function(){})()``

因为js中没有私有作用域的概念,你在全局或句句作用局中定义的变量,会被其他人以同名变量不小心覆盖掉,所以我们可以使用这种方法模拟一个私有作用域,jquery是采用这种方式的,()也叫匿名包裹器,或命名空间,在他内部定义的变量不会和外边发生冲突,而外部环境则不能访问容器内部的变量。

### 封装一个函数,参数是定时器的时间,.then执行回调函数?

```
Function callBack(time) {
  Return new paromise(resolve=>settimeout(resolve,time))
}
```
### forEach和map如何终止循环?
forEach和 map 无法在遍历结束前终止循环,如果要提前终止，除非抛出异常

## JS高阶

### js运行机制,对同步和异步的理解?

JS的所有任务可以分为两种,

**一种是同步任务,一种是异步任务**

*同步任务是主线程上的任务*
*异步任务是任务队列里的任务*

所有的回调函数都是异步任务,都会被推入异步队列;
当主线程所有任务完成后,检测异步队列里的任务,采用先入先出的原则,依次执行,如果是定时器的任务则等到时间再去执行,定时器必须满足两个条件一主线程空闲,二到达时间,时间的最小值是4ms如果不指定时间,则自动++;老版本是10ms,因此无法保证移动在到达时间后一定执行回调函数;主线程在任务队列中读取任务的过程是被不断循环的,所以也叫事件循环

## 对原型链的理解?

### 原型是什么？

每一个函数中都有一个prototype原型对象，用于表示类型之间的关系。

### 原型链是什么？

JavaScript万物都是对象，对象和对象之间也有关系，并不是孤立存在的。对象之间的继承关系，在JavaScript中是通过prototype对象指向父类对象，直到指向Object对象为止，这样就形成了一个原型指向的链条，专业术语称之为原型链。

### 手写一个原型继承?
```
function extend (Child,Person) {
  var f = function () {};
  f.prototype = Person.prototype;
  Child.prototype = new f();
  Child.prototype.constructor = Child;
  Child.usber = Person.prototype;
};
```
### 创建一个对象的几种方式?
```
// 字面量
Var o1 = {};

// 构造函数
Var o2 = new Object();

/// Create方法
Var o3 = Object.create({});
```

### 对闭包的理解?

闭包是指有权访问作用域内部的变量的函数,创建闭包的常见方式就是在函数内部创建一个函数并返回它,因为闭包可以访问内部属性导致该属性一直处于引用状态不会被销毁,所以闭包容易造成内存泄漏,解决方法是在用完之后将其设置为null;

### 对作用域的理解?

**在es5时作用域分为两种:**

全局作用域和局部作用域,而es6增加了块级作用域,使用let声明的变量只在当前代码块内生效;

*全局作用域代表window,*

*局部作用域以函数划分,*

外部无法访问作用域内部的属性和方法,内部则可以向上访问,通过作用域可以有效地防止变量被污染;

### 什么是内存泄漏?

当一个变量无法被销毁时就会产生内存泄漏,解决方法就是将其设置为null手动解除占用

### Ajax的实现机制?

　Ajax的原理简单来说通过XmlHttpRequest对象来向服务器发异步请求，从服务器获得数据，然后用javascript来操作DOM而更新页面。


同源:http协议;端口;域名;

前后端通信:

1. a: Ajax--同源下的通讯;
2. b:WebSocket--不受同源限制;
3. c:CORS--支持跨域通信,也支持同源通信.

创建Ajax:

1. XMLHttpRequest对象的工作流程;
2. 兼容性处理;
3. 事件的触发条件;
4. 事件的触发顺序.

### 如何解决跨域?
使用Jsonp,因为src属性不受跨域限制,所以在前端可以动态生成一个script标签通过src访问跨域的地址并在query参数里添加一个回调函数,后台讲数据作为参数返回;

```
*******JSONP跨域:
  * [util 工具类]
  * @type {Object}
  */
 var util = {};

 /**
  * [function 返回数组的指定项]
  * @param  {[type]} array [description]
  * @param  {[type]} item  [description]
  * @return {[type]}       [description]
  */
 util.indexOf = function (array, item) {
     for (var i = 0; i < array.length; i++) {
         if (array[i] === item) {
             return i;
         }
     }
     return -1;
 };

 /**
  * [function 判断是否为函数]
  * @param  {[type]} source [description]
  * @return {[type]}        [description]
  */
 util.isFunction = function (source) {
     return '[object Function]' === Object.prototype.toString.call(source);
 };

 /**
  * [isIE 判断是不是ie]
  * @return {Boolean} [如果是ie返回版本号，不是则返回false]
  */
 util.isIE = function () {
     var myNav = navigator.userAgent.toLowerCase();
     return (myNav.indexOf('msie') != -1) ? parseInt(myNav.split('msie')[1]) : false;
 };

 /**
  * [function 对象浅复制]
  * @param  {[type]} dst [description]
  * @param  {[type]} obj [description]
  * @return {[type]}     [description]
  */
 util.extend = function (dst, obj) {
     for (var i in obj) {
         if (obj.hasOwnProperty(i)) {
             dst[i] = obj[i];
         }
     }
 };

 /**
  * [function 获取一个随机的5位字符串]
  * @param  {[type]} prefix [description]
  * @return {[type]}        [description]
  */
 util.getName = function (prefix) {
     return prefix + Math.random().toString(36).replace(/[^a-z]+/g, '').substr(0, 5);
 };

 /**
  * [function 在页面中注入js脚本]
  * @param  {[type]} url     [description]
  * @param  {[type]} charset [description]
  * @return {[type]}         [description]
  */
 util.createScript = function (url, charset) {
     var script = document.createElement('script');
     script.setAttribute('type', 'text/javascript');
     charset && script.setAttribute('charset', charset);
     script.setAttribute('src', url);
     script.async = true;
     return script;
 };

 /**
  * [function jsonp]
  * @param  {[type]} url      [description]
  * @param  {[type]} onsucess [description]
  * @param  {[type]} onerror  [description]
  * @param  {[type]} charset  [description]
  * @return {[type]}          [description]
  */
 util.jsonp = function (url, onsuccess, onerror, charset) {
     var callbackName = util.getName('tt_player');
     window[callbackName] = function () {
         if (onsuccess && util.isFunction(onsuccess)) {
             onsuccess(arguments[0]);
         }
     };
     var script = util.createScript(url + '&callback=' + callbackName, charset);
     script.onload = script.onreadystatechange = function () {
         if (!script.readyState || /loaded|complete/.test(script.readyState)) {
             script.onload = script.onreadystatechange = null;
             // 移除该script的 DOM 对象
             if (script.parentNode) {
                 script.parentNode.removeChild(script);
             }
             // 删除函数或变量
             window[callbackName] = null;
         }
     };
     script.onerror = function () {
         if (onerror && util.isFunction(onerror)) {
             onerror();
         }
     };
     document.getElementsByTagName('head')[0].appendChild(script);
 };

/**
 * [json 实现ajax的json]
 * @param  {[type]} options [description]
 * @return {[type]}         [description]
 */
 util.json = function (options) {
     var opt = {
         url: '',
         type: 'get',
         data: {},
         success: function () {},
         error: function () {},
     };
     util.extend(opt, options);
     if (opt.url) {
         var xhr = XMLHttpRequest
            ? new XMLHttpRequest()
            : new ActiveXObject('Microsoft.XMLHTTP');
         var data = opt.data,
             url = opt.url,
             type = opt.type.toUpperCase(),
             dataArr = [];
         for (var k in data) {
             dataArr.push(k + '=' + data[k]);
         }
         if (type === 'GET') {
             url = url + '?' + dataArr.join('&');
             xhr.open(type, url.replace(/\?$/g, ''), true);
             xhr.send();
         }
         if (type === 'POST') {
             xhr.open(type, url, true);
             xmlhttp.setRequestHeader('Content-type', 'application/x-www-form-urlencoded');
             xhr.send(dataArr.join('&'));
         }
         xhr.onload = function () {
             if (xhr.status === 200 || xhr.status === 304) {
                 var res;
                 if (opt.success && opt.success instanceof Function) {
                     res = xhr.responseText;
                     if (typeof res ==== 'string') {
                         res = JSON.parse(res);
                         opt.success.call(xhr, res);
                     }
                 }
             } else {
                 if (opt.error && opt.error instanceof Function) {
                     opt.error.call(xhr, res);
                 }
             }
         };
     }
 };

 /**
  * [function crc32加密]
  * @param  {[type]} str [description]
  * @return {[type]}     [description]
  */
 util.crc32 = function (url) {
     var a = document.createElement('a');
     a.href = url;
     var T = (function () {
         var c = 0,
             table = new Array(256);
         for (var n = 0; n != 256; ++n) {
             c = n;
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             c = ((c & 1) ? (-306674912 ^ (c >>> 1)) : (c >>> 1));
             table[n] = c;
         }
         return typeof Int32Array !=== 'undefined' ? new Int32Array(table) : table;
     })();
     var crc32_str = function (str) {
         var C = -1;
         for (var i = 0, L = str.length, c, d; i < L;) {
             c = str.charCodeAt(i++);
             if (c < 0x80) {
                 C = (C >>> 8) ^ T[(C ^ c) & 0xFF];
             } else if (c < 0x800) {
                 C = (C >>> 8) ^ T[(C ^ (192 | ((c >> 6) & 31))) & 0xFF];
                 C = (C >>> 8) ^ T[(C ^ (128 | (c & 63))) & 0xFF];
             } else if (c >= 0xD800 && c < 0xE000) {
                 c = (c & 1023) + 64;
                 d = str.charCodeAt(i++) & 1023;
                 C = (C >>> 8) ^ T[(C ^ (240 | ((c >> 8) & 7))) & 0xFF];
                 C = (C >>> 8) ^ T[(C ^ (128 | ((c >> 2) & 63))) & 0xFF];
                 C = (C >>> 8) ^ T[(C ^ (128 | ((d >> 6) & 15) | ((c & 3) << 4))) & 0xFF];
                 C = (C >>> 8) ^ T[(C ^ (128 | (d & 63))) & 0xFF];
             } else {
                 C = (C >>> 8) ^ T[(C ^ (224 | ((c >> 12) & 15))) & 0xFF];
                 C = (C >>> 8) ^ T[(C ^ (128 | ((c >> 6) & 63))) & 0xFF];
                 C = (C >>> 8) ^ T[(C ^ (128 | (c & 63))) & 0xFF];
             }
         }
         return C ^ -1;
     };
     var r = a.pathname + '?r=' + Math.random().toString(10).substring(2);
     if (r[0] != '/') {
         r = '/' + r;
     }
     var s = crc32_str(r) >>> 0;
     var is_web = location.protocol.indexOf('http') > -1;
     return (is_web ? [location.protocol, a.hostname] : ['http:', a.hostname]).join('//') + r + '&s=' + s;
 };

 export default util;
   /**
       * 跨域通信的几种方法
       */

      // jsonp工作原理，参考jsonp.js


      // 利用hash，场景是当前页面 A 通过iframe或frame嵌入了跨域的页面 B
      // 在A中伪代码如下：
      var B = document.getElementsByTagName('iframe');
      B.src = B.src + '#' + 'data';
      // 在B中的伪代码如下
      window.onhashchange = function () {
          var data = window.location.hash;
      };

      // postMessage
      // 窗口A(http:A.com)向跨域的窗口B(http:B.com)发送信息
      Bwindow.postMessage('data', 'http://B.com');
      // 在窗口B中监听
      Awindow.addEventListener('message', function (event) {
          console.log(event.origin);
          console.log(event.source);
          console.log(event.data);
      }, false);

      // Websocket【参考资料】http://www.ruanyifeng.com/blog/2017/05/websocket.html

      var ws = new WebSocket('wss://echo.websocket.org');

      ws.onopen = function (evt) {
          console.log('Connection open ...');
          ws.send('Hello WebSockets!');
      };

      ws.onmessage = function (evt) {
          console.log('Received Message: ', evt.data);
          ws.close();
      };

      ws.onclose = function (evt) {
          console.log('Connection closed.');
      };

      // CORS【参考资料】http://www.ruanyifeng.com/blog/2016/04/cors.html
      // url（必选），options（可选）
      fetch('/some/url/', {
          method: 'get',
      }).then(function (response) {

      }).catch(function (err) {
        // 出错了，等价于 then 的第二个参数，但这样更好用更直观
      });   /**
       * 跨域通信的几种方法
       */

      // jsonp工作原理，参考jsonp.js


      // 利用hash，场景是当前页面 A 通过iframe或frame嵌入了跨域的页面 B
      // 在A中伪代码如下：
      var B = document.getElementsByTagName('iframe');
      B.src = B.src + '#' + 'data';
      // 在B中的伪代码如下
      window.onhashchange = function () {
          var data = window.location.hash;
      };

      // postMessage
      // 窗口A(http:A.com)向跨域的窗口B(http:B.com)发送信息
      Bwindow.postMessage('data', 'http://B.com');
      // 在窗口B中监听
      Awindow.addEventListener('message', function (event) {
          console.log(event.origin);
          console.log(event.source);
          console.log(event.data);
      }, false);

      // Websocket【参考资料】http://www.ruanyifeng.com/blog/2017/05/websocket.html

      var ws = new WebSocket('wss://echo.websocket.org');

      ws.onopen = function (evt) {
          console.log('Connection open ...');
          ws.send('Hello WebSockets!');
      };

      ws.onmessage = function (evt) {
          console.log('Received Message: ', evt.data);
          ws.close();
      };

      ws.onclose = function (evt) {
          console.log('Connection closed.');
      };

      // CORS【参考资料】http://www.ruanyifeng.com/blog/2016/04/cors.html
      // url（必选），options（可选）
      fetch('/some/url/', {
          method: 'get',
      }).then(function (response) {

      }).catch(function (err) {
        // 出错了，等价于 then 的第二个参数，但这样更好用更直观
      });
```

### CMD和AMD的区别,你用到过哪几种模块化加载?

AMD异步加载模块,依赖前置
CMD通用模块定义,按需加载
Commonjs 服务器端模块的规范, nodeJS采用此规范,webpack官方使用此规范,但也支持amd和cmd
UMD 通用模块规范,支持cmd和commonjs及全局模块

## ES6的模块

* Promise原理?
* http状态码?
1. 401未授权
1. 404页面不存在，
1. 500服务器错误，
1. 301重定向，
1. 302临时重定向，
1. 200 ok
1. 304协商缓存

**浏览器缓存分为强制缓存和协商缓存，优先读取强制缓存。**

**强制缓存** 分为expires和cache-control，而expires是一个特定的时间，是比较旧的标准和cache-control通常是一个具体的时间长度，比较新，优先级也比较高。

**协商缓存** 包括etag和last-modified，last-modified的设置标准是资源的上次修改时间，而etag是为了应对资源修改时间可能很频繁的情况出现的，是基于资源的内容计算出来的值，因此优先级也较高。

*协商缓存与强制缓存的区别在于强制缓存不需要访问服务器，返回结果是200，协商缓存需要访问服务器，命中协商缓存的话，返回结果是304。*

### Async和await?

Async相当于generator的语法糖,async相当于*号,而await相当于yeild,每一个async返回一个promise对象,可以使用.then方法添加回调,当函数执行时,一旦遇到await就会先返回,等到异步操作完成,再接着执行函数体内后面的语句,async的返回值会作为.then的参数传入,ansyc可以看做是多个异步操作组成的promise对象,await就是nebulathen命令的语法糖

## JS算法

### 冒泡排序?

时间复杂度: 
最差 O(n2)
平均O(n2)
空间复杂度 O(1) 稳定
```
function sort(arr){
  for(var i = 0;i<arr.length;i++){
    for (var j = i+1; j < arr.length;j++) {
	  var before = arr[i];
	  if (before > arr[j]) {
	    var after = arr[j];
		arr[i] = after;
		arr[j] = before;
	  }
	}
  };
  console.log(arr);
}
```
### 快速排序?
最差 O(n2)
平均O(n*log2n)
空间复杂度 O(n) 不稳定
```
function quickSort(arr) {
  if (arr.length <= 1) { return arr; }
    var left = [];
    var right = [];
    var ind =  Math.floor(arr.length/2);
    var num = arr.splice(ind,1)[0];
    console.log(num)
    for (let item of arr) {
      console.log(item)
	  if (item < num) {
		left.push(item)
	  } else {
		right.push(item);
	  };
	};
  return [...quickSort(left),num,...quickSort(right)];
};
```

### Js的sort方法排序(普通数组,数组对象)

```
arr.sort((a,b)=>{
  return a-b
});
// Sort按照字母排序
arr.sort((a,b)=>{
  return a.name.localeCompare(b.name)
})
```

### 合并对象？
```
function concat(obj1,obj2){
  for (let item in obj2) {
    if (obj2.hasOwnProperty(item)) {
      obj1[item] = obj2[item];
    }
  };
  console.log(obj1);
};
concat(a,b)
```
### 取字符串出现最多的字符?
```
function qu(arr) {
  let newArr = [];
  let obj = {};
    for (let item of arr) {
	  if (!obj[item]){
		obj[item] = 1;
	  } else {
		obj[item]++;
	  };
	};
	for (let i in obj) {
	  let o = {
	    name: i,
		value: obj[i]
	  };
	newArr.push(o);
  };
  console.log(newArr);
  return newArr.sort((a,b)=>{
	return b.value-a.value
  })[0];
};
```
# 框架

## VUE经典面试题

### 双向数据绑定原理?

vue.js 是采用数据劫持结合发布者-订阅者模式的方式，通过Object.defineProperty()来劫持各个属性的setter，getter，在数据变动时发布消息给订阅者，触发相应的监听回调。

### 组件之间的通信?

父组件往子组件传值props
子组件往父组件传值，通过$emit事件,父组件接收子组件用$on
不同组件之间传值，通过eventBus（小项目少页面用eventBus，大项目多页面使用 vuex）

①定义一个新的vue实例专门用于传递数据，并用$emit导出

②定义传递的方法名和传输内容，点击事件或钩子函数触发eventBus.emit事件

③用$on接收传递过来的数据

### Vue的生命周期?

创建前/后： 
beforeCreated 数据和dom都没有生成。

Created data有了，dom还没有生成。

载入前/后：
beforeMount 已经初始化但是此时是虚拟dom

mounted，vue实例挂载完成。

更新前/后：当data变化时，会触发beforeUpdate和updated方法。

销毁前/后：在执行destroy方法后，对data的改变不会再触发周期函数，说明此时vue实例已经解除了事件监听以及和dom的绑定，但是dom结构依然存在

### 为什么要用vuex,vuex是做什么的?

vuex主要是是做数据交互，父子组件传值可以很容易办到，但是兄弟组件间传值（兄弟组件下又有父子组件），或者大型spa单页面框架项目，页面多并且一层嵌套一层的传值，异常麻烦，用vuex来维护共有的状态或数据会显得得心应手。
#### v-model是什么的语法糖,如何在组件之间使用v-model?
v-model是v-bind和v-on的语法糖,在组件中使用分为两步使用v-model传递父级数据进去,自己组件使用props接收,使用v-bind:value绑定在input上, 在有新值的时候触发v-on:input将通过$emit新值作为参数返回

###  Vue.nextTick?
Vue.nextTick(callback)，当数据发生变化，更新后执行回调。Vue.$nextTick(callback)，当dom发生变化，更新后执行的回调。
### vue ruter钩子函数

```
// 全局钩子
berforEach: (to, from, next) => {
// ...
}
afterEach: (to, from, next) => {
// ...
}
// 路由独享钩子
beforeEnter: (to, from, next) => {
// ...
}
// 组件钩子
beforeRouteEnter: (to, from, next) => {
// ...
}
berforeRouterUpdate: (to, from, next) => {
// ...
}
berforeRouterLeave: (to, from, next) => {
// ...
}
```

### v-key的意义?
虚拟DOM有一个Diff算法, 简单的说就是为了提高遍历性能

## 项目问题

### 开发过程中遇到过哪些问题如何解决的?开发一个插件要考虑到什么?对项目的优化用到哪些手段?
1. 压缩文件减少http请求;
2. 理由浏览器缓存;
3. 使用CDN;
4. 非核心代码异步加载

### 你所了解的攻击方式?

#### 跨站点请求伪造?

必须用户主动登录了才可以,盗用用户身份,发送恶意请求 

目前防御 CSRF 攻击主要有三种策略：

1. 验证 HTTP Referer 字段；
2. 在请求地址中添加 token 并验证；
3. 在 HTTP 头中自定义属性并验证。

**Xss跨站脚本注入**

是指恶意攻击者利用网站没有对用户提交数据进行转义处理或者过滤不足的缺点，进而添加一些代码，嵌入到web页面中去。使别的用户访问都会执行相应的嵌入代码。

*防御方法就是对用户输入数据进行安全过滤;*

### 错误的捕获方式?

错误分类
代码运行错误 try catch window.onerror

资源错误 节点绑定object.onerror事件 

peroformance.getEntries()




# 介绍项目

上一个公司的主要业务是针对学校企业和个人开发在线的心理测评，主要以B端业务宽窄网和多元儿童智能测评系统为主，宽窄网分为学生端教师端企业端咨询师端；基本的模块划分为在线测评，测评报告，心理社区和成长曲线，使用到的技术是VUE+echarts；我主要负责测评报告和成长曲线模块； 多元儿童智能测评系统是面向3-12岁的孩子，采用游戏的方式对儿童进行智力，潜能等方面的测评，该系统分为PC和移动两版，使用技术为vue+eharts，使用rem完成屏幕适配；我主要负责登陆，注册信息的功能实现，以及潜能模块记忆力，空间推理，逻辑思维等测评游戏的制作；还有小程序辅仁青少年成长中心，主要是针对线下店用户及线上用户进行免费心理测试并生成测评报告，线下可进行完整测评，而线上则只能做一部分；我负责根据需求对整个小程序进行独立开发；目前已经迭代两个版本；

# 小程序的坑？

设置数据用`this.setData`而不能使用`this.data.xxx=xxx；`
小程序对canvas的支持不完善，且他是原生组件层级最高，不能通过z-index控制层级，不要在scroll-view和swiper中使用它，因为她的位置相对当前屏幕无法通过定位跟随移动，在开发者工具里显示正常，真机显示永远在顶层

web-view部分安卓手机显示空白，原因在于直接赋值地址正常显示，而如果是在onload里取值再赋值就会有这个bug，解决方法是用一个变量判断取值完成在赋值显示web-view

在使用onShareAppMessage进行转发操作时，默认可以截取当前屏幕作为分享图片 ，但在web-view下部分安卓无法截取成功，分享图片显示空白，解决办法是添加默认背景图片

## Html5的新特性？

新增Video，audio等媒体标签，header和footer，artice和section，details等新元素，canvas画布，拖动也是新特性，所有元素都可以拖动；
拖动什么 - `ondragstart` 和 `setData()`
放到何处 - `ondragover`
进行放置 - `ondrop`
地理定位API;
还有input增加了color等类型；

**Web存储**

`sessionStorage`—客户端数据存储，只能维持在当前会话范围内。
 `sessionStorage` 方法针对一个 `session` 进行数据存储。当用户关闭浏览器窗口后，数据会被删除。

`localStorage`—客户端数据存储，能维持在多个会话范围内。
 `localStorage` 对象存储的数据没有时间限制。第二天、第二周或下一年之后，数据依然可用

`Cookie`和`sessionStrorage`和`LocalStortage`都是保存在浏览器端；

`Cookie`在`http`请求中携带，浏览器和服务器之间来回传递。而`sessionStrorage`和`localStorage`仅在本地保存；
`Cookie`容量小，仅为4kb，且多数浏览器一个网站最多只能保存20个`cookie`；可以设置过期时间；
`sessionStrorage`和`localStorage`大小可以达到5m；`sessionStrorage`为会话级别的存储，关闭当前窗口就会被销毁，`sessionStrorage`是永久储存的，除非用户主动清除缓存！	



