# CSS 스터디 14주차

* 코니 그리기 - 머리2
* 코니 그리기 - 몸



## 코니 그리기 - 뺨

<div style="background: #FCBFCA;
	width: 40px;
	height: 20px;
	border-radius: 50%;
"></div>
<br/>


```css
.cheek {
	background: #FCBFCA;
	width: 40px;
	height: 20px;
	border-radius: 50%;
}
```

---
## 코니 그리기 - 뺨2

<div style="background: #FCBFCA;
	border-radius: 50%;
  width: 20px;
  height: 4px;
  box-shadow: 0px 0px 5px 5px #FCBFCA;
	border-radius: 50%;
"></div>
<br/>


```css
.cheek {
	background: #FCBFCA;
	width: 10px;
	height: 2px;
	box-shadow: 0px 0px 5px 5px #FCBFCA;
	border-radius: 50%;
}
```

---
## 코니 그리기 - 입

<div style="
  width: 32px;
  height: 22px;
  left: 30%;
  top: 65%;
  border-radius: 50% / 0 0 100% 100%;
  background: #D73E34;
  border: 3px solid black;
"></div>


```
.cony .mouth {
  position: absolute;;
  width: 32px;
  height: 22px;
  left: 30%;
  top: 65%;
  border-radius: 50% / 0 0 100% 100%;
  background: #D73E34;
  border: 3px solid black;
  overflow: hidden;
}
```

---
## 코니 그리기 - 몸
```
  <div class="body">
    <div class="arm left"></div>
    <div class="arm right"></div>
    <div class="leg left">
      <div class="foot"></div>
    </div>
    <div class="leg right">
      <div class="foot"></div>
    </div>
  </div>
  ```
  
---
  
## 코니 그리기 - 팔
<div style="
  top: 0px;
  width: 100px;
  height: 50px;
  border: 3px solid black;
  background: #fff;
  border-radius: 100% 0% 0% 100% / 50%;
  transform-origin: 100% 50%;"></div>
  
```

.arm {
  position: absolute;
  top: 0px;
  width: 100px;
  height: 50px;
  border: 3px solid black;
  background: #fff;
  border-radius: 100% 0% 0% 100% / 50%;
  transform-origin: 100% 50%;
}
```

---

## 코니 그리기 - 다리
```
.leg {
  position: absolute;
  background: #fff;
  width: 50%;
  top: 130px;
  height: 100px;
  border: 3px solid black;
}
```

---
## 코니 그리기 - 발
<div style="
  width: 80px;
  height: 60px;
  background: #fff;
  border: 3px solid black;
  right: -10px;
  bottom: -30px;
  transform: rotate(-20deg);
  border-radius: 50%;
"></div>

```
.foot {
  position: absolute;
  width: 80px;
  height: 60px;
  background: #fff;
  border: 3px solid black;
  right: -10px;
  bottom: -30px;
  transform: rotate(-20deg);
  border-radius: 50%;
}
```
---
## 코니 그리기 - 다리 잇기
```
.leg:after {
  position: absolute;
  width: 100%;
  height: 100%;
  content: "";
  background: inherit;
}
```
---
## 코니 그리기 - 몸 잇기
```
.body:after {
  content: "";
  width: 100%;
  height: 100%;
  background: inherit;
  position: absolute;
  left: 0;
  top: 0;
  z-index: 1;
}
```

