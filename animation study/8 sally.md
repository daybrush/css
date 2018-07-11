# CSS Animation 8
* sally

---

## sally
* 샐리를 그려봅시다.
* https://codepen.io/daybrush/pen/ZjzOqq
---
## sally - 바깥쪽 날개
* 인사를 하는 애니메이션
* rotate를 사용
* transform-origin 적절하게 사용

---
## sally - 바깥쪽 날개
```css
@keyframes wing {
  from {
    transform: rotate(20deg);
  }
  to{
    transform: rotate(35deg);
  }
}

animation: wing 0.5s ease-in-out infinite alternate;
```

---
## sally - 왼쪽/오른쪽 다리
* 걷는 애니메이션
* rotate를 사용
* transform-origin 적절하게 사용
---
## sally - 왼쪽/오른쪽 다리
* 왼쪽과 오른쪽을 반대로 작용
```css
@keyframes leg-left {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(50deg);
  }
}
@keyframes leg-right {
  from {
    transform: rotate(-50deg);
  }
  to {
    transform: rotate(0deg);
  }
}
```
---
## sally - 위/아래 입

* 입 벌리고 / 닫는 (뻐끔뻐끔) 애니메이션
* rotate와 transform-origin 사용
* border-radius 사용
* transform-origin 적절하게 사용



---
## sally - 이동

* 오뚜기처럼 앞으로 뒤로 가면서 앞으로 진행
* rotate와 right, transform-origin 사용
* transform-origin 적절하게 사용


