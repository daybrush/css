# CSS Animation 9
* Raindrop Effect


---
## 물방울이 떨어지는 효과
* 원형으로 커지면서 나타나면서 사라지는 효과

---
## 물방울 효과 순서
* 원형이다.
* 점점 커진다. (scale)
* 잔상이 있다. (border-width)
* 점점 흐려진다. (opacity)
* 이러한 효과가 3겹으로 이루어져있다.(animation-delay)

---
## 물방울 효과
https://codepen.io/daybrush/pen/vRrbXG

https://codepen.io/daybrush/pen/djMrER

---
## 물방울 효과
* 사용 property
	* transform: scale
	* border-width
	* opacity
	* animation-delay
---
## 물방울 효과

```css
.raindrop {
  animation: raindrop 1.5s both infinite;
}
.raindrop2 {
  animation-delay: 0.4s;
}
.raindrop3 {
  animation-delay: 0.8s;
}
```
---
## 물방울 효과
```
@keyframes raindrop {
  from {
    transform: scale(0);
    border-width: 120px;
    opacity: 1;
  }
  to {
    transform: scale(1);
    border-width: 0px;
    opacity: 0.2;
  }
}
```
---
## 물방울 효과 - 완성

https://codepen.io/daybrush/pen/bjpZyQ