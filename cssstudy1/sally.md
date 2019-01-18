---
# CSS 스터디 6주차
* 샐리를 그려봅시다.


---

## 샐리 얼굴을 그려봅시다.
<img width="405" alt="2018-03-28 2 30 20" src="https://user-images.githubusercontent.com/3433062/37985354-7be7c97e-3233-11e8-8536-af8c35400de0.png">

https://codepen.io/daybrush/pen/RMjdRP

---
## 샐리 얼굴을 그려봅시다

* 얼굴 배경: #F9D95C
* 눈, 테두리 : black
* 입: #EE6F2D
* 입 테두리: #C05123
---
## 샐리 얼굴을 그려봅시다
* 얼굴, 눈, 입을 잘 배치해 봅시다.

--- 
## 샐리 얼굴을 그려봅시다
* 입
	* transform-origin
	* transform
	* 두 개의 도형을 이어봅시다.

---

## 샐리 입
```html
    <div class="mouth mouth-up">
        <div class="mouth mouth-down">
        </div>
        ::after
    </div>
```

---

## 샐리 입
* transform-origin
 ```css
.sally .mouth {
  position: absolute;
  width: 140px;
  height: 50px;
  border-radius: 25px;
  border: 6px solid #CF4804;
  background: #FF6600;
  right: 0%;
  transform-origin: calc(100%-25px) 50%;
}
```
* calc(100% - 25px) = 115px


----
## 샐리 입
* transform
```
.sally .mouth-up {
  transform: rotate(20deg);
}
.sally .mouth-down {
  transform: rotate(-40deg);
  right: -6px;
  top: -6px;
}
```
* 두 개의 도형을 이어봅시다.
```
.sally .mouth-up:after {
  content: "";
  position: absolute;
  background: inherit;
  border-radius: inherit;
  width: 100%;
  height: 100%;
}
```