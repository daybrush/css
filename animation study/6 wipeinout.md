# CSS Animation 6
* left, top(or translate)
* wipe in
* wipe out


---

## wipe in
* 화면 전환기법
* 기존의 장면에 다음 장면을 밀어 넣으면서 화면을 전환

---
## wipe in

https://codepen.io/daybrush/pen/xzmvpe

```css
@keyframes wipeIn {
  0% {
    left: -100%;
  }
  100% {
    left: 0%;
  }
}
```

---
## wipe out
* 화면 전환 기법
* wipe in과 반대
* 기존의 장면을 밀어 내면 다음 장면이 보이면서 화면을 전환
---

## wipe out
https://codepen.io/daybrush/pen/BVvXPR
```css
@keyframes wipeOut {
  0% {
    left: 0%;
  }
  100% {
    left: 100%;
  }
}
```
---
## wipe in / out
* wipe in은 기존 장면은 그대로 있고 다음 장면이 온다.
* wipe out은 다음 장면은 그대로 있고 기존 장면이 나간다.

---
## wipe out 실습
https://youtu.be/VwK6f9SqtfQ?t=10s

https://codepen.io/daybrush/pen/RJEXYR

---

## 실습
### html

```html
<div class="container">
  <div class="cards">
    <div class="card card1"></div>
    <div class="card card2"></div>
    <div class="card card3"></div>
    <div class="card card4"></div>
    <div class="card card5"></div>
  </div>
</div>
```


---
### css
```css
.card {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: -1;
  background: #f55;
  border-radius: 8px;
  transform: scale(0.7);
  transition: transform ease 1s;
}
.card1, .wipeout+.card {
  z-index: 1;
  transform: scale(1);
}
.card.wipeout {
  animation: wipeout 1s 1 ease-in-out forwards;
  z-index: 3;
}
```
---
### js
```js
document.querySelectorAll(".card").forEach(card => {
   card.addEventListener("click", e => {
     card.classList.add("wipeout");
   })
});
```
---
### keyframes
* 자연스럽게 오른쪽 상단으로 슬라이드하면서 wipe out하는 모습
```css
@keyframes wipeout {
  100% {
    top: -120%;
    left: 70%;
    transform: rotate(20deg);
  }
}
```
