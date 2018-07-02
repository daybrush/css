# CSS Animation 4
* 실습
* left, top


---
## 한바퀴 도는 정사각형을 애니메이션으로 만들자

```css
/*
n: name
d: duration
e: easing
*/
animation: n d e iterationCount direction filMode;
/* easing: linear;
iterationCount: 1;
direction: normal;
*/

```
---
## 애니메이션 속성
```
animation: han 3s;
```
* 필수인 이름과 시간 2개만 입력해도 작동한다.
* 둘 중 하나만 없어도 작동이 되지 않는다.

---
## 실습
```html
<div class="rect"><div>
```
```css
.rect {
	width: 100px;
	height: 100px;
	background: #f55;
}
```

---
## 실습
```css
@keyframes tranlsate {
  0% {
    left: 0;
    top: 0;
  }
  25% {
    left: 100px;
    top: 0;
  }
  50% {
    left: 100px;
    top: 100px;
  }
  75% {
    left: 0px;
    top: 100px;
  }
}
```
---
## left, top

* https://codepen.io/daybrush/pen/oyPqvO
* .rect에 걸려있는 left와 top을 제거해보자

---

## left, top
* 75%에서 0%로 가는게 아니라 현재 적용되고 있는 스타일로 돌아간다.
* 100px에서 auto로 가기 때문에 적용이 되지 않는다.


---

## left, top 대신 transform

```css
@keyframes tranlsate {
  0% {
    transform: translate(0px, 0px);
  }
  25% {
    transform: translate(100px, 0px);
  }
  50% {
    transform: translate(100px, 100px);
  }
  75% {
    transform: translate(0px, 100px);
  }
}
```