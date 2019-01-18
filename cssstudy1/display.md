# CSS 스터디 2주차
1. display
2. 세로 가운데 정렬 방법

---
## display
* none
* block
* inline-block
* inline
* ~~table~~
* ~~table-cell~~
* ~~table-row~~
* flex
* ...
---

### display
* none
* block
* inline-block
* inline
* table
* flex
---

### none
* 해당 element를 안보이게 한다.
* 렌더링을 하지 않는다.
* 그래서 display: none 상태의 엘리먼트를 보여줄 때 transition이 동시 적용이 되지 않는다.
* 강제로 렌더링을 발생시켜 변경을 한다.
	* 동기 : element.offsetWidth, offsetHeight, offsetLeft, ...
	* 비동기 : setTimeout, requestAnimFrame
---
### block
* div의 기본 display 속성
* 한 줄에 나열되지 않고 element하나에 한 줄을 차지한다.

---
### inline
* span, a, img 등 기본 display 속성
* text입력과 관련된 태그들의 기본 속성
* 위치 조절이 불가
* margin-left, right만 설정 가능
* pading설정은 가능
---
### inline-block
* inline의 특징인 한 줄 입력과 block의 특징인 마진속성과 크기속성을 설정할 수 있다.
 * https://codepen.io/daybrush/pen/pLoKwm
---
### inline 과 inline-block
```html
<div>1</div>
<div>2</div>
<div>3</div>
<div>4</div>
```
```css
div {
    display: inline-block;
    width: 25%;
}
```
* div사이에 여백이 있는듯이 보인다. 이 여백은 스페이스(&nbsp ;)다.
* 여백을 없애려면 태그를 이어붙이기 또는 ```font-size: 0px;```를 한다.


---

### flex
 flexbox(유연한 레이아웃) / 1차원 레이아웃 모델 
 https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Flexbox%EC%9D%98_%EA%B8%B0%EB%B3%B8_%EA%B0%9C%EB%85%90
* flex
* flex-flow
  * flex-wrap
  * flex-direction
* justify-content
* align-items
* align-content
* align-self
* https://www.w3schools.com/css/css3_flexbox.asp
---

#### flex
* flex item에서 차지하는 비율
* width가 설정된 아이템을 제외한 나머지 크기에 대해 비율을 설정
* https://developer.mozilla.org/en-US/docs/Web/CSS/flex
* https://www.w3schools.com/cssref/css3_pr_flex.asp

----
#### flex-flow
* flex-wrap과 flex-direction을 동시에 설정하는 속성
---
#### flex-wrap
* 아이템을 감싸는 방법
* flex를 쓰게 되면 기본으로 한 열/행 나열이 된다.
* nowrap(default) : 아이템들이 컨테이너보다 크게 되면 자동으로 크기 조절이 된다.
* wrap : 아이템의 크기가 보존된다.
* wrap-reverse: wrap이면서 아이템의 진행방향이 반대다.
---
#### flex-direction
* 아이템들의 진행방향
* row(default): 가로 정방향으로 진행
* row-reverse : 가로 역방향으로 진행
* column : 세로 방향으로 진행
* column-reverse : 세로 역방향으로 진행
 ---

#### justify-content
* 아이템들의 정렬 방법(flex-direction)
* flex-start(default) : 왼쪽 정렬
* center : 가운데 정렬
* flex-end : 오른쪽 정렬
* space-around : 아이템들의 마진까지 동일
* space-between
	* 양쪽 아이템은 가장 끝에 배치
	* 양쪽 아이템 왼쪽 아이템은 왼쪽 마진, 오른쪽 아이템은 오른쪽 마진이 없음
---
#### align-items(flex-wrap: nowrap)
* 아이템들의 정렬 방법(flex-direction와 다른방향)
	* flex-direction이 row면 정렬 방향이 column
	* flex-direction이 column이면 정렬 방향이 row
* flex-start(default) : 왼쪽 정렬
* center : 가운데 정렬
* flex-end : 오른쪽 정렬
* stretch: 크기가 따로 설정돼있지 않는 경우 컨테이너 크기만큼 늘어난다.
* baseline: 잘 모르겠다.
---
#### align-content(flex-wrap: wrap)
* 아이템들의 정렬 방법(여러 줄인 경우)
* stretch(default): 컨테이너를 기준으로 크기가 자동으로 맞춰진다.
* flex-start: 왼쪽 정렬
* center : 가운데 정렬
* flex-end : 오른쪽 정렬
* space-around : 아이템들의 마진까지 동일
* space-between
	* 양쪽 아이템은 가장 끝에 배치
	* 양쪽 아이템 왼쪽 아이템은 왼쪽 마진, 오른쪽 아이템은 오른쪽 마진이 없음
---
### etc
* align-self: vertical-align같은 녀석