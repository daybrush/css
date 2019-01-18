---
# CSS 스터디 5주차
* transform 1
* transform-origin
* 두 개의 도형을 이어봅시다.


---
## transform 1
* translate
* rotate

---
## translate
* translateX(10px)
* translate(10px)
	* 오른쪽으로 10px 갑니다.
* translateX(10%)
	* 자신의 너비의 10%만큼 오른쪽으로 이동합니다.
* translateY(10px)
	* 아래쪽으로 10px 갑니다.
*  translate(10px, 10px)
	*  오른쪽, 아래쪽으로 10px 갑니다.

---
## rotate
* 회전
* rotate(45deg)
* 45도로 회전합니다.
---
## transform
* transform: translate(40px) rotate(40deg)
* transform: rotate(40deg) translate(40px)
---
## transform-origin
* 원점의 위치를 바꾼다.
* default: 50% 50%;


https://codepen.io/daybrush/pen/wmxjNG

---
## 두 개의 도형을 이어봅시다.
```
<div class="cloud">
  <div class="cloud">
    <div class="cloud"></div>
  </div>
</div>
```
https://codepen.io/daybrush/pen/NYBMER

---
## 두 개의 도형을 이어봅시다.
```
.cloud:after {
  content: "";
  position: absolute;
  background: inherit;
  border-radius: inherit;
  width: 100%;
  height: 100%;
}
```
