## CSS ANIMATION 12
* material design 2
	* dissolve
	* cross dissolve
	* fade through
* https://material.io/design/motion/understanding-motion.html#expressing-continuity
---

## dissolve
* 다른 화면으로 장면 (fade in / fade out) 전환 
* Scene1 => Scene2
* FADE IN, FADE OUT 둘 중 하나이상 적용된다.

---
* fade in

https://codepen.io/daybrush/pen/GGPbXb
* fade out

https://codepen.io/daybrush/pen/eKbwQG

---
## dissolve
* 뜻과 동작은 다르지만 효과는 같다.
  * fade in(나타나다)
  * fade out(사라지다)

https://codepen.io/daybrush/pen/zLRYom

---

## cross dissolve
* 다른 화면으로 장면 (fade in / fade out) 전환 
* Scene1 => Scene2
* FADE IN, FADE OUT 둘 다 적용된다.

---
## cross dissolve
* Scene1 : Fade Out (사라지다)
* Scene2 : Fade In (나타나다)
* Scene1은 사라지는 효과 Scene2는 나타나는 효과를 가진 장면 전환
* 배경에 영향을 끼친다.

https://codepen.io/daybrush/pen/KBQKvZ


---

## fade through

* 크기가 다른 장면을 전환하는 방법
* cross dissolve로 전환
* https://codepen.io/daybrush/pen/rrJNvo


---
## fade through

* scene 1

```css
@keyframes fadethrough1 {
  0% {
    opacity: 1;
    height: 300px;
    top: 40px;
  }
  100% {
    opacity: 0;
    height: 380px;
    top: 0px;
  }
}
```
---

## fade through
* scene2

```css
@keyframes fadethrough2 {
  0% {
    opacity: 0;
    height: 300px;
    top: 40px;
  }
  100% {
    opacity: 1;
    height: 380px;
    top: 0px;
  }
}
```

---
## fade through 완성
* https://codepen.io/daybrush/pen/NBymme?editors=0110

