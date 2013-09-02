## 2. `inline-block` 小淘氣

---

##要把東西排一起

比起 `float` 我更愛 `inline-block`！
<p class="fragment">而且他會超潮的Response Layout</p>
<p class="fragment">（如果在合適的情況底下）</p>

---

<a class="jsbin-embed" href="http://jsbin.com/inline/3/embed?css,output">JS Bin</a>

---

##症狀

- 他明明塞的下，為什麼自己斷行了？
- 為什麼我的東西不是連在一起的？
- 為什麼我做不出群組按鈕？

![](images/speech/btn-group.png?borderless)

---

##原因是有空白（white-space）

根據[W3C 9.1 White space](http://www.w3.org/TR/html401/struct/text.html#h-9.1)所定義：

- ASCII space
- ASCII tab
- ASCII form feed
- Zero-width space
- **Line breaks** are also white space characters

---


	<div class="parent">
		<div class="child">I'm a child!</div>
		<div class="child">I'm a child!</div>
		<div class="child">I'm a child!</div>
	</div>



---

##從 Mockup 下手  

---

##直接擠在一行

	
	<div class="parent">
		<div class="child">I'm a child!</div><div class="child">I'm a child!</div><div class="child">I'm a child!</div>
	</div>


---

##把空格丟到 html 內文裡

	<div class="parent">
		<div class="child">
		I'm a child!</div><div class="child">
		I'm a child!</div><div class="child">
		I'm a child!</div>
	</div>



or


	<div class="parent">
		<div class="child">I'm a child!</div
		><div class="child">I'm a child!</div
		><div class="child">I'm a child!</div>
	</div>


---

##註解掉

	<div class="parent">
		<div class="child">I'm a child!</div><!--
		--><div class="child">I'm a child!</div><!--
		--><div class="child">I'm a child!</div>
	</div>


---

##從 CSS 下手

---

##letter-spacing

<a class="jsbin-embed" href="http://jsbin.com/inline-fix/10/embed?css,output">JS Bin</a>

---

##margin

<a class="jsbin-embed" href="http://jsbin.com/inline-fix/8/embed?css,output">JS Bin</a>

---

##font-size

<a class="jsbin-embed" href="http://jsbin.com/inline-fix/9/embed?css,output">JS Bin</a>

Chrome 已經拿掉最小字體大小12px限制了。

---

##你要怎麼跟設計師說

<ul>
	<li class="fragment">就像是 InDesign 不小心多了空格破版一樣！</li>
	<li class="fragment">記得要把空格隱藏起來！</li>
	<li class="fragment" style="line-height:3em"><h3>你好棒！</h3></li>
</ul>