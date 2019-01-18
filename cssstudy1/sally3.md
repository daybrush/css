# CSS STUDY 8주차
* border, border-radius
* 샐리 그리기3 (날개, 다리)

---
##  border, border-radius

<div style="width: 100px; height: 100px;background: #FFD93B; border: 10px solid black;border-left-color: #f55; border-top-color: #f5f; border-right-color: #5ff; margin: 5px; display: inline-block;vertical-align:top;"></div>

<div style="width: 100px; height: 100px;background: #FFD93B; border: 10px solid black;border-left-color: #f55; border-top-color: #f5f; border-right-color: #5ff; margin: 5px; display: inline-block; border-radius: 50%;"></div>
<p></p>

<div style="width: 100px; height: 100px;background: #FFD93B; border: 10px solid black;border-left-color: #f55; border-top-color: #f5f; border-right-color: #5ff; margin: 5px; display: inline-block;vertical-align:top;border-left-width: 0px;"></div>

<div style="width: 100px; height: 100px;background: #FFD93B; border: 10px solid black;border-left-color: #f55; border-top-color: #f5f; border-right-color: #5ff; margin: 5px; display: inline-block; border-radius: 50%; border-left-width: 0px;"></div>


---
## 샐리 입 2번째 버전
<img src="https://user-images.githubusercontent.com/3433062/38558710-ec867d5a-3d0b-11e8-958a-26603f5b9e52.png">

* 반원, 둥근 직사각형 2개
https://codepen.io/daybrush/pen/geqdLm

---
## 샐리 입 2번째 버전
```
<div class="mouths">
  <div class="mouth up"></div>
  <div class="mouth down"></div>
</div>
```

---
## 날개

https://codepen.io/daybrush/pen/rdYmEK
<div class="wing" style="width: 200px; height: 120px;border-radius: 50%/30% 30% 70% 70%;background:#FFD93B;border: 5px solid black;"></div>
<p>&nbsp;</p>
<div class="wing" style="width: 200px; height: 120px;border-radius: 50%/30% 30% 70% 70%;background:#FFD93B;border: 5px solid black;  border-left: 5px solid transparent;"></div>
<p>&nbsp;</p>

```
border-radius: 50% / 30% 30% 70% 70%;
```

---
## 날개
```
.sally .wing {
  position: absolute;
  width: 200px;
  height: 120px;
  border-radius: 50% / 30% 30% 70% 70%;
  background: #FFD93B;
  border: 5px solid black;
}
```


---
## 다리
* 6주차 도형잇기 참고


<img src="https://user-images.githubusercontent.com/3433062/38557522-3f7adfd2-3d08-11e8-8396-6130f8fa7cf5.png" />
<img src="https://user-images.githubusercontent.com/3433062/38557445-0b21b1c0-3d08-11e8-88f1-5ac344456d51.png">

```
<div class="leg">
    <div class="foot"></div>
    ::after
</div>
  ```
---

## 다리
```
.sally .leg {
  background: #FF6600;
  border: 5px solid #CF4804;
  width: 45px; height: 60px;
  position: absolute;
}
.sally .leg::after {
  content: "";
  position: absolute;
  width: 100%; height: 100%;
  background: inherit;
}
.sally .leg .foot {
  position: absolute;
  width: 70px; height: 50px;
  top: 80%; right: -15px;
  border: inherit;
  background: inherit;
  border-radius: 50%;
  transform: rotate(-20deg);
}
```


---

## CSS STUDY 9주차
* 삼각형
* 말풍선
* border있는 정삼각형