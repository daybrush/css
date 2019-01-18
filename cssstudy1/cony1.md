# CSS 스터디 13주차

* 코니 그리기 - 머리1


---
## 코니 그리기 - 머리 마크업
* head
	* ear left
	* ear right
	* eye left
	* eye right
	* cheek left
	* cheek right
	* nose
	* mouth
	* tongue

https://codepen.io/daybrush/pen/jxBRbp

---
## 코니귀 그리기 - 복습
* box-shadow


---
## box-shadow 코니귀

![](/Users/user/Desktop/스크린샷%202018-04-25%20오전%202.28.57.png)

<div style="width: 35px;
	height: 100px;
	background: #FCBFCA;
	border-radius: 50% / 100% 100% 0 0;
	border:3px solid #333;
        border-bottom: 0;
	top: 200px;
	box-shadow:#fff 0px 0px 0px 6px inset;"></div>
    
---
## box-shadow 코니귀
```css
.ear {
	position: absolute;
	width: 35px;
	height: 100px;
	background: #FCBFCA;
	border-radius: 50% / 100% 100% 0 0;
	border:3px solid #333;
        border-bottom: 0;
	top: 200px;
	box-shadow:#fff 0px 0px 0px 6px inset;
}
```

---
## 코니 그리기 - 머리
```
<div class="cony">
  <div class="head">
    <div class="ear left"></div>
    <div class="ear right"></div>
    <div class="face">
      <div class="eye left"></div>
      <div class="eye right"></div>
      <div class="cheek left"></div>
      <div class="cheek right"></div>
      <div class="nose"></div>
      <div class="mouth">
        <div class="tongue"></div>
      </div>
    </div>
  </div>
</div>
```
---


## 코니 그리기 - 머리 & 귀 잇기

* 2개 이상의 도형 잇기 복습하기


---

## 코니 그리기 - 색깔

테두리 : #333333(검정색)
귀, 혀, 볼 : #FCBFCA(분훙색)
입: #D73E34(빨간색)

