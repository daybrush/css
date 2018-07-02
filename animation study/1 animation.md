# CSS Animation 1
* animation
* transition

---
## animation과 transition의 차이?
| |animation|transition|
|---|---|---|
|성능|비슷하겠지....|비슷하겠지....|
|사용성|어렵다|쉽다|
|키프레임|O|X|
|속성 해제|animation이 빠지면 <br/>keyframes에있던 속성도 다 해제된다.|변화 X

---

## animation 속성

* animation-name: 이름
* animation-duration: 플레이 시간
* animation-iteration-count: 반복 횟수
* animation-direction: 진행 방향
* animation-timing-function: 타이밍펑션
* animation-fill-mode: 시작 또는 끝에 일어날 행동
* animation-delay: 딜레이
* animation-play-state: 플레이 상태

---
## name
**이름**
keyframes 이름을 나타낸다. keyframes를 먼저 등록해야 animation을 쓸 수 있다.


---
## direction
**진행 방향**
* normal(default): 정방향
* reverse: 역방향
* alternate: 왕복
* alternate-reverse: 역방향으로 왕복

alternate가 붙은 것은 iteration-count가 1보다 커야 효과를 볼 수 있음

https://www.w3schools.com/cssref/playit.asp?filename=playcss_animation-direction

---
## iteration-count
**반복 횟수**

* 0 ~ n
* infinite

숫자는 **실수**이다. 1.5는 1번과  반(0.5)만 재생이 된다.

https://www.w3schools.com/cssref/playit.asp?filename=playcss_animation-iteration-count&preval=1

---
## duration
**플레이 시간**
플레이 시간은 keyframes가 0%부터 100%까지 진행하는 시간을 말한다.

**::총 플레이 시간이 아니다**

---
## timing-function
**재생되는 속도 매쥑**

* linear: ~~직선~~ 일정한 속도
* ease-in: 점점 빨라진다
* ease-out: 점점 느려진다
* ease : 빨라지다 느려짐
* ease-in-out: 빨라지다 느려짐 (ease보다 자연스러운 느낌적인 느낌)

---
## timing-function
bezier curve 공식을 이용한 프리셋이 제공되며 cubic-bezier css함수를 써서 바꿀 수 있다.
* 전체에 대해 함수가 적용된게 아니라 키프레임 사이마다 적용된다.
* 전시간과 다음시간에 대해 함수가 적용된게 아니라 전키프레임과 다음키프레임의 값에 대해 함수가 적용된다.

http://cubic-bezier.com


https://www.w3schools.com/cssref/css3_pr_animation-timing-function.asp

---
## fill-mode
**시작 또는 끝에 일어날 행동**
시작은 애니메이션이 시작되는 전을 나타내며 끝은 애니메이션이 끝났을 때를 말한다.

* none: 시작하기 전엔 현재 가지고 있는 스타일을 유지하고 끝난 후에도 시작하기 전에 가지고 있던 스타일로 돌아간다.
* backwards: 시작하기 전(delay)에 막 시작하는 모습을 유지한다.
* forwards: 끝난 직후 모습을 유지한다.
* both: backwards와 forwards 둘 다 적용한다
 
https://www.w3schools.com/cssref/css3_pr_animation-fill-mode.asp.

보통 forwards 또는 both를 많이 쓴다.



