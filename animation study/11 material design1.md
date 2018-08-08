# CSS ANIMATION STUDY 11
* material design - motion
	* Lazy Loading


---

## Lazy Loading

* https://material.io/design/motion/understanding-motion.html#usage

* 이 것을 구현해 봅시다.
---

## Lazy Loading
* https://codepen.io/daybrush/pen/mjpPXN

---
## 다른 점
* 딱딱하다?
* 랙걸렸나? 멈췄나?
* 로딩 중인지 알 수 없다.

---
## 해야 할 것
* 로딩중은 로딩중답게
	* 정적인 것은 동적으로
* 로딩중은 JS가 아닌 CSS로 
---
## 해야 할 것
* ~~loading 중인 아이템은 class에 loading이 있다.~~
* ~~loading이 끝난 아이템은 class에 loaded가 있다.~~
* loading중인 아이템 애니메이션
* loading이 끝난 아이템 애니메이션(트랜지션)
---

## HTML
* Item HTML
```html
  <li class="loading">
    <div class="img-wrapper">
      <img src="https://naver.github.io/egjs-infinitegrid/assets/image/2.jpg"/>
    </div>
    <div class="content-wrapper">
      <p class="tittle"><span>Title 1</span></p>
      <p class="description"><span>Decription</span></p>
    </div>
  </li>
```

---
## CSS
* placeholder
```
li .img-wrapper:before {
  content: "";
  position: absolute;
  width: 40px;
  height: 40px;
  opacity: 1;
  background: #eee;
  border-radius: 50%;
}
li .content-wrapper p:before {
  content: "";
  position: absolute;
  width: 150px;
  height: 10px;
  border-radius: 5px;
  background: #eee;
  top: 5px;
}
```
---
## 완성
* https://codepen.io/daybrush/pen/KBZdqR