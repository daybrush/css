# CSS ANIMATION STUDY 10
* Twinkle


---
## 반짝이는 효과
* width 사용
* scaleX
* tranlsate(또는 left)
를 간단하게 사용

---
## 반짝이는 효과
* raindrop효과와 비슷하다.

https://codepen.io/daybrush/pen/bjpJZN


---
## 반짝이는 효과
* 이게 뭐나요?
	* 반짝이입니다.
* 이상하면 4방향으로 추가해보세요.


https://codepen.io/daybrush/pen/yqOdNx


---
## 반짝이는 효과
```css
@keyframes twinkle {
  0% {
    width: 0px;
    transform: translate(0px) scaleX(1);
  }
  100% {
    width: 100px;
    transform: translate(50px) scaleX(0) ;
  }
}
```

---
## 반짝이는 효과
* transform은 한 속성이기 때문에 중복이 됩니다.
* 중복이 안되긴 위해서는 자식 Element를 만들어서 중복이 안되게 해야합니다.

---

## 반짝이는 태양 그리기
* raindrop과 twinkle을 적절히 섞어서 반짝이는 태양 그리기

---

## 반짝이는 태양
https://codepen.io/daybrush/pen/KBzjyr