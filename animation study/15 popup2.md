
# CSS ANIMATION STUDY 15
* popup 2
	* 전역변수
	* bubbling
	* getItem
	* openPopup(target)
---
## popup
* 전역변수
* popup: popup element
* popupItem: item을 복사하는 위치
* popupTarget: 클릭한 item
```js
const popup = document.querySelector("#popup");
const popupItem = popup.querySelector(".item");

let popupTarget = 0;

```
---
## popup
* Bubbling을 통한 Item 가져오기

```js
app.addEventListener("click", e => {
  const target = e.target;

  popupTarget = getItemParent(target);
  openPopup(popupTarget);
});

```

---
## popup
* Item 찾기
```js

function getItemParent(target) {
  if (!target || target === app ||
    target === document.body) {
    return;
  } else if (target.classList.contains("item")) {
    return target;
  }
  return getItemParent(target.parentNode);
}
```

---
## openPopup(target)

* 아이템이 커지는 효과를 내기 위해 아이템을 그대로 복사한다.
```js
function openPopup(target) {
  popupItem.innerHTML = target.innerHTML;
  ....
}
```

---
## openPopup(target)
* 아이템의 위치와 크기를 복사한다.
```js
const rect = target.getBoundingClientRect();
const left = rect.left;
const top = rect.top;
const width = rect.width;
const height = rect.height;
popup.style.left = `${left}px`;
popup.style.top = `${top}px`;
popup.style.width = `${width}px`;
popup.style.height = `${height}px`;
popupItem.style.width = popup.style.width;
```

---
## openPopup(target)
* 복사한 item width를 복사한다.
* 왜냐하면 아이템(이미지) 사이즈가 화면 사이즈보다 작으면 어색하게 보인다.
* popup이 커지면서 이미지도 같이 커지지만 이미지가 원래 크기에 도달하면 더 이상 커지지 않으면서 어색하게 움직인다.

---
## openPopup(target)
* 이미지의 최대 높이를 500으로 설정한다.
```js
const targetImage = target.querySelector("img");
let width = targetImage.naturalWidth;
const height = targetImage.naturalHeight;

width = width / height * Math.min(height, 500);
```
