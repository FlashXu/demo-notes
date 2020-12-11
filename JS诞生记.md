# 1. JS 历史
* [wiki JavaScript](https://zh.wikipedia.org/wiki/JavaScript#%E5%8E%86%E5%8F%B2)
### 1.1 发明者 - Brendan Eich
1995年，网景招募了[布兰登·艾克](https://zh.wikipedia.org/wiki/%E5%B8%83%E8%98%AD%E7%99%BB%C2%B7%E8%89%BE%E5%85%8B)，目标是把Scheme语言嵌入到Netscape Navigator浏览器当中。后来网景决定发明一种与Java搭配使用的辅助脚本语言并且语法上有些类似，这个决策导致排除了采用现有的语言，例如Perl、Python、Tcl或Scheme。为了在其他竞争提案中捍卫JavaScript这个想法，公司需要有一个可以运作的原型。艾克在1995年5月仅花了十天时间就把原型设计出来了。

最初命名为**Mocha**，1995年9月在Netscape Navigator 2.0的Beta版中改名为**LiveScript**，同年12月，Netscape Navigator 2.0 Beta 3中部署时被重命名为**JavaScript**，当时网景公司与昇阳电脑公司组成的开发联盟为了让这门语言搭上Java这个编程语言“热词”，因此将其临时改名为JavaScript，日后这成为大众对这门语言有诸多误解的原因之一。
### 1.2 微软采纳
JavaScript推出后在浏览器上大获成功，微软公司在不久后就为Internet Explorer 3浏览器推出了JScript，以与处于市场领导地位的网景产品同台竞争。JScript也是一种JavaScript实现，这两个JavaScript语言版本在浏览器端共存意味着语言标准化的缺失，发展初期，JavaScript的标准并未确定，同期有网景的JavaScript，微软的JScript双峰并峙。除此之外，微软也在网页技术上加入了不少专属对象，使不少网页使用非微软平台及浏览器无法正常显示，导致在浏览器大战期间网页设计者通常会把“用Netscape可达到最佳效果”或“用IE可达到最佳效果”的标志放在主页。
### 1.3 标准化
1996年11月，网景正式向ECMA（欧洲计算机制造商协会）提交语言标准。1997年6月，ECMA以JavaScript语言为基础制定了ECMAScript标准规范ECMA-262。JavaScript成为了ECMAScript最著名的实现之一。

<hr>
# 2. JavaScript诞生记
* [JavaScript诞生记博客](http://www.ruanyifeng.com/blog/2011/06/10_design_defects_in_javascript.html)
### 2.1 网景公司的讨论
1994年，网景公司（Netscape）发布了Navigator浏览器0.9版。这是历史上第一个比较成熟的网络浏览器，轰动一时。但是，这个版本的浏览器只能用来浏览，不具备与访问者互动的能力。**网景公司急需一种网页脚本语言，使得浏览器可以与网页互动。**

网景公司当时有两个选择：一个是采用现有的语言，比如Perl、Python、Tcl、Scheme等等，允许它们直接嵌入网页；另一个是发明一种全新的语言。这两个选择各有利弊。第一个选择，有利于充分利用现有代码和程序员资源，推广起来比较容易；第二个选择，有利于开发出完全适用的语言，实现起来比较容易。

1995年Sun公司将Oak语言改名为Java，正式向市场推出。

网景公司动了心，决定与Sun公司结成联盟。它不仅允许Java程序以applet（小程序）的形式，直接在浏览器中运行；甚至还考虑直接将Java作为脚本语言嵌入网页，只是因为这样会使HTML网页过于复杂，后来才不得不放弃。

网景公司的整个管理层，都是Java语言的信徒，Sun公司完全介入网页脚本语言的决策。因此，Javascript后来就是网景和Sun两家公司一起携手推向市场的，这种语言被命名为"Java+script"并不是偶然的。

1995年5月，网景公司做出决策，未来的网页脚本语言必须"看上去与Java足够相似"，但是比Java简单，使得非专业的网页作者也能很快上手。这个决策实际上将Perl、Python、Tcl、Scheme等非面向对象编程的语言都排除在外了。Brendan Eich被指定为这种"简化版Java语言"的设计师。
### 2.2 Brendan Eich 设计思路
Javascript语言实际上是两种语言风格的混合产物----（简化的）函数式编程+（简化的）面向对象编程。这是由Brendan Eich（函数式编程）与网景公司（面向对象编程）共同决定的。
* 借鉴C语言的基本语法；

* 借鉴Java语言的数据类型和内存管理；

* 借鉴Scheme语言，将函数提升到"第一等公民"（first class）的地位；

* 借鉴Self语言，使用基于原型（prototype）的继承机制。
### 2.3 Brendan Eich的评价
"与其说我爱Javascript，不如说我恨它。它是C语言和Self语言一夜情的产物。十八世纪英国文学家约翰逊博士说得好：'它的优秀之处并非原创，它的原创之处并不优秀。'（the part that is good is not original, and the part that is original is not good.）"

<hr>
# 3. JavaScript的10个设计缺陷
* [JavaScript的10个设计缺陷博客](http://www.ruanyifeng.com/blog/2011/06/10_design_defects_in_javascript.html)
### 3.1 为什么JavaScript有设计缺陷
* 设计阶段过于仓促
* 没有先例
* 过早的标准化
### 3.2 JavaScript的10个设计缺陷
* 不适合开发大型程序
* 非常小的标准库
* null和undefined混淆
* 全局变量难以控制
* 自动插入行尾分号
* 加号运算符加剧运算复杂性
* NaN特性奇怪
* 难以区分一个对象是不是数组
* == 当两个值类型不同时，会发生自动转换
* 基本类型的包装对象造成混淆
### 3.3 如何看待Javascript的设计缺陷
* 如果遵守良好的编程规范，加上第三方函数库的帮助，Javascript的这些缺陷大部分可以回避。

 * Javascript目前是网页编程的唯一语言，只要互联网继续发展，它就必然一起发展。目前，许多新项目大大扩展了它的用途，[node.js](http://nodejs.org/)使得Javascript可以用于后端的服务器编程，[coffeeScript](http://jashkenas.github.com/coffee-script/)使你可以用python和ruby的语法，撰写Javascript。

* 只要发布新版本的语言标准（比如 [ECMAscript 5](http://www.ecma-international.org/publications/standards/Ecma-262.htm)），就可以弥补这些设计缺陷。当然，标准的发布和标准的实现是两回事，上述的很多缺陷也许会一直伴随到Javascript存在的最后一天。




