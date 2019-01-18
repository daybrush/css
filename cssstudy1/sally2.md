# CSS STUDY 7주차

* 샐리 그리기 2


---

## Sally 
* 머리
* 몸
* 날개
* 다리


---
## 머리
```html
<div class="sally">
  <div class="head">
    <div class="eyes">
      <div class="eye left"></div>
      <div class="eye right"></div>
    </div>
    <div class="mouth mouth-up">
        <div class="mouth mouth-down"></div>
    </div>
  </div>
</div>
```

---
## 머리
```css
.sally {
  position: absolute;
  margin: auto;
  left: 0;
  right: 0;
  top: 0;
  width: 350px;
  height: 350px;
}
.sally .head {
  position: absolute;
  border-radius: 50%;
  background: #FFD93B;
  border: 5px solid black;
  width: 350px;
  height: 350px;
  left: 0%;
  top: 10%;
  z-index: 2;
}
```

---
## 머리 - 눈
```css
.sally .eyes {
  position: absolute;
  width: 100%;
  top: 27%;
  z-index: 3;
}
.sally .eye {
  position: absolute;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  background: black;
}
.sally .eye.left {
  left: 53%;
}
.sally .eye.right {
  right: 53%;
}
```

---
## 머리 - 입
```
.sally .mouths {
  position: absolute;
  width: 54px;
  height: 54px;
  top: 55%;
  left: 50%;
  z-index: 3;
}
.sally .mouth {
  position: absolute;
  width: 140px;
  height: 50px;
  border-radius: 25px;
  border: 6px solid #CF4804;
  background: #FF6600;
  right: 0%;
  transform-origin: 115px 50%;
}
```
---
## 머리 - 입2
```
.sally .mouth-up {
  transform: rotate(20deg);
}
.sally .mouth-up:after {
  content: "";
  position: absolute;
  background: inherit;
  border-radius: inherit;
  width: 100%;
  height: 100%;
}
.sally .mouth-down {
  transform: rotate(-40deg);
  right: -6px;
  top: -6px;
}
```
---
## 머리와 몸통을 잇기
* 6주차에서 두개의 도형을 잇기 참고


```
<div class="sally">
  <div class="head">
  	<div class="body"></div>
  	::after
  </div>
</div>
```
```
.sally .head::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: inherit;
  border-radius: inherit;
}
```