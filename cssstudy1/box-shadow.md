# CSS 스터디 12주차

* box-shadow 실습

---

## box-shadow 실습
* box-shadow 초승달
* box-shadow 말풍선
* box-shadow 코니귀
* box-shadow 브라운귀


---

## box-shadow 초승달

<div style=" width: 200px;
  height: 200px;
  border-radius: 50%;
  box-shadow: inset -30px -30px black;"></div>


https://codepen.io/daybrush/pen/yjOEYq

---
## box-shadow 초승달

```css
.moon {
  position: absolute;
  width: 200px;
  height: 200px;
  border-radius: 50%;
  box-shadow: inset -30px -30px black;
}
```

---
## box-shadow 말풍선

![](/Users/user/Desktop/스크린샷%202018-04-25%20오전%201.57.25.png)

https://codepen.io/daybrush/pen/KRzeQr


---
## box-shadow 말풍선

```css
.balloon {
  position: relative;
  width: 160px;
  height: 80px;
  border-radius: 10px;
  border: 5px solid black;
}
.balloon:after {
  content: "";
  position: absolute;
  left: 40%;
  top:  100%;
  width: 40px;
  height: 40px;
  border-radius: 0% 0% 0% 100%;
  box-shadow: inset 20px 5px black;
}
```

---
## box-shadow 코니귀

![](/Users/user/Desktop/스크린샷%202018-04-25%20오전%202.28.57.png)

---
## box-shadow 코니귀
```css
.ear {
	content:"";
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

### box-shadow 브라운귀


https://codepen.io/daybrush/pen/XqdPJe


---

### box-shadow 브라운귀


```
.ear {
	position: absolute;
	width: 55px;
	height: 50px;
	background: #512911;
	border-radius: 50%;
	top: 2px;
	box-shadow:#744932 0px 0px 0px 8px inset;
	-webkit-box-shadow: #744932 0px 0px 0px 8px inset;
	border:3px solid #333;
}
```