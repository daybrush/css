# CSS 스터디 10주차

* 비어있는 정삼각형
* 별1
* 말풍선1


---
## 비어있는 정삼각형

https://codepen.io/daybrush/pen/xjKXda?editors=0110
```
.triangle {
	position: absolute;
	left: 0;
	right: 0;
	top: 0px;
	bottom: 20px;
	margin: auto;
	width: 100px;
	height: 10px;
	border-radius: 5px;
	background: #f5f;
}

```
---
## 비어있는 정삼각형
```
.triangle:before, .triangle:after {
	content: "";
	position: absolute;
	width: 100%;
	height: 100%;
	border-radius: inherit;
	background: inherit;
}
.triangle:before {
	transform-origin: 5px 50%;
	transform: rotate(60deg);
}
.triangle:after {
	transform-origin: calc(100% - 5px) 50%;
	transform: rotate(-60deg);
}
```

---
## 별1

<p align="center">
<img src="https://user-images.githubusercontent.com/3433062/38872604-9fb46f4a-428e-11e8-9bb6-a0987854733a.png">
</p>

https://codepen.io/daybrush/pen/xjKXpQ


https://codepen.io/daybrush/pen/WJezKg

---
## 별1

삼각형 10개


<img src="https://user-images.githubusercontent.com/3433062/38872720-e912646c-428e-11e8-87e4-b01a96c6a66e.png"/>

<img src="https://user-images.githubusercontent.com/3433062/38872721-e93d7dc8-428e-11e8-9b0a-3ca331c55bb3.png"/>


---
## 말풍선 실습
* 삼각형 + 사각형 = 말풍선!
* https://codepen.io/daybrush/pen/gzYQGR

---
## 말풍선
```
.balloon {
  position: relative;
  width: 200px;
  height: 200px;
  border-radius: 10px;
  border: 10px solid black;
  background: #fff;
}
.balloon:before {
  position: absolute;
  content: "";
  left: 100%;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
  border-left: 10px solid black;
  margin-left: 10px;
  top: 20px;
}
```

---

## 다음
* box-shadow
* 달그리기
* box-shadow를 이용한 말풍선
* skew를 이용한 비어 있는 별