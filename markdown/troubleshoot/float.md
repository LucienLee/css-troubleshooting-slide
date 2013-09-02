##1. 被講到爛掉的`float`問題

---

##症狀:

- 為什麼我沒有背景？
- 我的排版亂掉了混在一起了！
- 兩欄式的版排不出來…
- 下拉式選單怪怪的…

---

#主流
##clearfix

	.clearfix:after {
		content: "";
		display: table;
		clear: both;
	}
	
	.clearfix {
		*zoom: 1;
	}	

---

##clear: both/left/right

最後加一個清除浮動用的元素

---

##overflow: hidden/auto

告訴父元素要完全包住子元素

---

##如果你有特殊需求

<a class="jsbin-embed" href="http://jsbin.com/OrAB/6/embed?html,output">JS Bin</a>

---

##Future

min-height: contain-floats
![contain-float](images/speech/contain-float.png)

---

##你要怎麼跟設計師說
  
<ul>
	<li class="fragment">解釋離家出走的概念</li>
	<li class="fragment">記得要 clearfix</li>
	<li class="fragment" style="line-height:3em"><h3>你好棒！</h3></li>
</ul>
