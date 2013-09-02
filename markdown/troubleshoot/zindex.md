## 5. z-index 不就是PS的圖層嗎？

---

##症狀：
- z-index 都要 999999 了，為什麼不是最上層？
- 為什麼總是上下疊不出想要的？

---

##解釋元素疊疊樂的規則之前
我們得要先有疊東西的地基

---

##Stacking context
元素疊放順序的情境、環境

可以以下的方法建立：

- html文件的源頭 `<html>`
- position: 非 static，並且 z-index != auto 
- *opacity < 1*


---

##就像是午餐盒一樣
飯菜疊放的環境－<span class="fragment highlight-blue">飯盒！</span>

![](images/speech/lunch.jpg)

---

##Stacking Order
排序不只是看z-index

- 非 static posiiton, 正 z-index
- *未設定 position*
- 非 static posiiton, 未設定z-index
- 非 static position, 負 z-index
- stacking context 之背景與邊界

---

<a class="jsbin-embed" href="http://jsbin.com/AkEYuNa/1/embed?html,css,output">JS Bin</a>

---

##完整 z-index 規則

1. the background and borders of the element forming the stacking context
2. the child stacking contexts with negative stack levels (most negative first)
3. the in-flow, non-inline-level, non-positioned descendants
4. the non-positioned floats
5. the in-flow, inline-level, non-positioned descendants, including inline tables and inline blocks
6. the child stacking contexts with stack level 0 and the positioned descendants with stack level 0
7. the child stacking contexts with positive stack levels (least positive first)

---

##你可以在餐盒裡放小碟子

在 Stacking context 裡頭在創造一個 Stacking context

![](images/speech/lunch.jpg)

---

##日式飯盒

小碟子無法突破自己所在飯盒的宿命

![](images/speech/lunchbox2.jpg)

---

<a class="jsbin-embed" href="http://jsbin.com/ACEWoDe/8/embed?html,css,output">JS Bin</a>

---

##你要怎麼跟設計師說

<ul>
	<li class="fragment">要用z-index前，設個position吧！</li>
	<li class="fragment">想一下自己所在的飯盒（Stacking context）</li>
	<li class="fragment">你是不是用了opactiy?!</li>
	<li class="fragment" style="line-height:3em"><h3>你好棒！</h3></li>
</ul>