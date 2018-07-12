# CSS 80% JS 20% 1
1. position

---
## position
* static(default)
* relative
* absolute
* fixed
* ~~sticky~~
## offsetParent

---
### static
* 기본값입니다.
* 위치를 지정할 수 없습니다.
* width, height, padding, margin은 가능
https://codepen.io/daybrush/pen/RMoXOg

---
### relative
* 현재 위치에 에서 상대적인 위치를 가질 수 있습니다.
* left, top, right, bottom을 지정할 수 있으며 기준은 현재 위치입니다.

---
### absolute
* position이 static이 아닌 가장 가까운 위치에 있는 부모노드에 대해 절대적인 위치를 설정할 수 있다.
* 부모노드가 static이면 부모의 부(부부부)모 노드가 기준이 될 수 있다.
* 부모 노드의 padding을 무시한다. (client)

---
### relative & absolute - offsetParent
* position이 static이 아닌 가장 가까운 위치에 있는 부모노드다.
* offsetTop, Left는 offsetParent에 대한 기준이다.
* position이 아무 한테도 안 걸려 있으면 body가 offsetParent이다.
* body의 offsetParent은 null이다.

---
### fixed
* 부모노드와 상관없이 스크린에 기준을 갖는다.
* 스크롤을 해도 스크린에 고정돼있다.
---
### ~~sticky~~
* 스크롤 영역을 기준으로 부모노드가 사라지기 전까지 모서리에 고정된다.
* 그룹, 스티커
* https://developer.mozilla.org/ko/docs/Web/CSS/position



---
### Understand client, offset, scroll
![understand offset, client](https://i.stack.imgur.com/5AAyW.png)