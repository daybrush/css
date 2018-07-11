# CSS Animation 7
* transform

---

## transform
* 변형
* 2d, 3d 변형을 할 수 있다.
* 선형대수학을 배우면 이해가 더 잘된다.

---
## transform
* 2d와 3d는 지원범위가 다르다.
* 3d는 IE12부터 지원......

---

## transform
* translate(X, Y, Z, 3d): 이동하다.
* scale(X, Y, Z, 3d): 범위/ 크기 / 규모
* rotate(X, Y, Z, 3d): 회전하다.
	* 기본이 Z축에 대한 회전
	* X,Y,Z축이 아닌 다른 축에 대한 회전은 엄청난 계산 뿐만 아니라 복잡한 식이고 rotate가 아닌 matrix를 사용해야 한다.
* skew(X, Y) : 비뚤다. 경사지게 하다. 왜곡.
	* Z와 3d가 없는 이유는 div자체가 3d가 아닌 2d plain(평면/판)이다.
* perspective: 원근감 부여

---

## transform
* 한 개의 속성
* CSS 함수로 사용할 수 있다.
* 개별적으로 transition을 걸 수도 없다.

---
## rotate(0deg) vs rotate(360deg)
https://codepen.io/daybrush/pen/ZjzWdX
```
@keyframes rotate {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}

@keyframes rotate2 {
    0% {
        transform: scale(1) rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}
```

---
## rotate(0deg) vs rotate(360deg)
* 기대: 360도 회전한다.
* 이론: 회전하지 않는다.
* 현실: rotate, rotate2가 다르게 작동한다.
* 이유: 모르겠다.
* 설명
	* rotate(0deg)와  rotate(360deg)의 값은 같으므로 회전하지 않는다. 
	* transform 함수 조합의 연산 값이 같으면 작동하지 않는다.


---

## matrix
* 배열
* transform의 함수는 배열의 곱셈이다. (선형대수)
* translate

![](https://i.stack.imgur.com/Vb23q.png)

---
## matrix - rotate
* rotate

![](https://i.stack.imgur.com/W3hip.jpg)


---

## 복습
https://codepen.io/daybrush/pen/WKbepm

* 이동하면서 나타나고 이동하면서 사라지는 구름

