# CSS Animation 2
* transition

---
## animation과 transition의 차이?
| |animation|transition|
|---|---|---|
|성능|비슷하겠지....|비슷하겠지....|
|사용성|어렵다|쉽다|
|복잡성|복잡|간단|
|키프레임|O|X|

---
## transition 속성
* transition-delay
* transition-duration
* transition-property
* transition-timing-function

많이 쓰는 방법
transition: all ease 0.2s; ㅋㅋㅋ

---
## transition-delay
* transition을 적용하기 전 딜레이
---
## transition-duration
* transition을 적용할 시간

트랜지션은 transition속성이 추가되면 작동되는게 아니라 transition에 설정해놓은 속성을 바꿀시 작동된다.

---
## transition-property
transition을 적용할 속성들

* all(default)
* 속성들

---
## transition-timing-function
animation-timing-function과 똑같이 duration만큼 적용될 타이밍 펑션

* linear: ~~직선~~ 일정한 속도
* ease-in: 점점 빨라진다
* ease-out: 점점 느려진다
* ease : 빨라지다 느려짐
* ease-in-out: 빨라지다 느려짐 (ease보다 자연스러운 느낌적인 느낌)


---
## transition 과 animation
* 연산이 불가능한 포맷은 적용이 안된다.
* 예) auto, ~~none, block~~ visiblity, scroll같은 문자
* color는 #000000가 내부적으로 rgba(0, 0, 0, 1)로 변환해준다.
