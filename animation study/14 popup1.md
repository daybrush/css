
# CSS ANIMATION STUDY 14
* popup 1
	* markup
	* css

---
## popup
* 이미지 목록은 InfiniteGrid JustifiedLayout을 사용했습니다.

* openPopup(target)
* closePopup(target)
* 두 함수로 나뉘었고 target은 아이템 자신이다.
---
## popup
* https://codepen.io/daybrush/pen/ERzvrQ?editors=0110
* transition이 빠진 popup 예제다.
* item에서 자연스럽게 커지는 popup을 만든다!
---
## popup
* popup markup
* item-wrapper: 아이템이 복사되는 영역
* item: 복사된 아이템
* popup-info, title, description: popup 정보
```html
<div id="popup" class="close">
  <div class="item-wrapper">
    <div class="item"></div>
  </div>
  <div class="popup-info">
    <div class="title">egjs Title</div>
    <div class="description">Lorem.</div>
  </div>
</div>
```
---
## popup
* 클래스
* open: 보여줄 때 추가하는 클래스
* close: display: none 하는 클래스 가장 마지막에 호출된다.

* openPopup => remove close class => add open class => done
* closePopup => remove open class => done => add close class
---
## popup 
* position:fixed인 popup을 만든다.
* 모든 transition의 duration은 0.5로 통일
```css
#popup {
  position: fixed;
  overflow: hidden;
  background: #fff;
  transition: all ease 0.5s;
}
```
---
## popup
* item-wrapper는 색깔 transition만 설정
* 기존 item의 info는 가려지게 한다.
```css
#popup .item-wrapper {
  transition: background-color ease 0.5s;
  padding: 0;
  font-size: 0;
  background-color: rgba(0, 0, 0, 0);
}
#popup.open .item-wrapper {
  background-color: #000;
}
#popup .item .info {
  transition: all ease 0.5s;
  opacity: 1;
}
#popup.open .item .info {
  opacity: 0;
}
```

---
## popup
* open이 추가되면서 close가 제거되면 popup은 보여지게 된다.
* open이 제거되면 popup이 사라지는 transition이 발생하며
* close가 추가되면 popup은 완전히 사라진다.
```css
#popup.open {
  overflow: auto;
}
#popup.close {
  display: none;
  overflow: hidden;
}
```

---
## popup
* 딜레이를 살짝 주면서 popup이 어느정도 나타나면 정보도 나타난다.
* 하지만 close할 때는 딜레이 없이 사라진다.
```css
#popup .popup-info {
  opacity: 0;
  transition: opacity ease 0.3s;
}
#popup.open .popup-info {
  transition-delay: 0.2s;
  opacity: 1;
}
```

