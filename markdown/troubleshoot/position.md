##4. 定位傻傻搞不清楚

---

##症狀：

- 有 `position:absolute` 還套 `float: left`
- 有 `position:absolute` 還套 `display:inline`
- 有 `float:left` 還套 `display:inline-block`
- 我的 `top`, `right`, `bottom`, `left` 到底是相對於誰位移啊？
- 為什麼排出來的版都跟我想的不一樣！


---

#CSS Position 3大法

---

#3 Positioning Schemes

<ul>
 <h3>Normal Flow</h3>
 <p>`display`: `block` | `inline` | `inline-block` | `table`, `position`: `static` | `relative`,  `float`: `none`;</p>
 
 <h3>Floats</h3>
 <p>`float`: `left` | `right`, ( `position`: `relative` )</p>
 
 <h3>Absolute Positioning</h3>
 <p>`position`: `absolute` | `fixed`</p>
</ul>

Check it on [W3C CSS2.1 9.3](http://www.w3.org/TR/CSS2/visuren.html#positioning-scheme)

---

##Normal Flow

![](images/speech/normalflow.png?borderless)

從左到右；從上到下

---

##Float

文繞圖

![](images/speech/float.png?borderless)

<small>先根據 Normal Flow 定位以後，再位移到所在行的左邊或是右邊</small>

---

### Float position 時可以使用 position: relative!

---

##Absolute Positioning

![](images/speech/abposition.png?borderless)

Word 的文字方塊

相對於position != static的父元素  

---

##各門派之間的微妙關係

###absolute positioning
	float: none;
	display: block;



###float != none
	display: block;	


---

##其實也不完全是這樣

![](images/speech/relative-pf.png)

---

##Position Relative VS Absolute

###新手設計師都以為他們是好碰友！

	.parent{
		position: relative;
	}
	
	.child{
		position: absolute;
	}

---

#巴特
##BUT

---

##Normal Flow 與 Absolute Positioning

position: relative VS position: absolute

---

##父子大不相同
<p class="fragment">~~隔壁老王生的~~</p>

---

###雖然都是 top, right, bottom, left 好夥伴

![](images/speech/relative.png?borderless)

position: relative

---

###雖然都是 top, right, bottom, left 好夥伴

![](images/speech/absolute.png?borderless)

position: absolute

---

##最後 Box model 再來參一腳

`margin` | `padding` | `border`

![](images/speech/boxmodel.png?borderless)


---


##你要怎麼跟設計師說

<ul>
	<li class="fragment">斯斯有三種，排版也有三種</li>
	<li class="fragment">各司其職，雙修之前請想清楚</li>
	<li class="fragment">`relative`跟`absolute`概念不一樣！</li>
	<li class="fragment">沒事可以背個**上右下左**</li>
	<li class="fragment" style="line-height:3em"><h3>你好棒！</h3></li>
</ul>