# CSS 스터디 3주차
* 수직정렬


---
## 세로 가운데 정렬 방법
* button
* line-height
* top: 50%; margin-top: -height/2;
* transform
* margin: auto;
* vertical-align
* ~~display: table;~~
* display: flex;

---

### button
* button태그안의 내용은 전부 가운데 정렬돼있다.

```html
<button>HELLO<br/>HELLO2</button>
```
---
### line-height
* 쓰이고자 하는 곳이 텍스트 또는 한 줄일 경우 많이 쓰는 방법
* height와 line-height를 동일하게 설정하면 된다.

```css
.button {
    width: 100px;
    height: 40px;
    line-height: 40px;
}
```
---
### top: 50%; margin-top: -height/2;
* position: absolute; 인 엘리먼트를 가운데 정렬할 수 있는 방법
* 고전적인 방법 중 하나
* 단점: width/height를 꼬오오오옥 알아야한다.

```css
.target {
    position: absolute;
    top: 50%;
    height: 100px;
    margin-top: -50px;
}
```
---
### top: 50%; transform: translateY(-50%)
* position: absolute; 인 엘리먼트를 가운데 정렬할 수 있는 방법
* translate의 100%는 자신의 크기 기준이다.
* 여러 줄 쓸 때 좋은 방법
* height를 몰라도 사용할 수 있다.
* 단점: transform은 IE 9 이상부터 쓸 수 있다.

```css
.target {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}
```

---
### margin: auto;
* position: absolute; 인 엘리먼트를 가운데 정렬할 수 있는 방법
* width/height값이 지정돼있으면 가운데 정렬이 가능하다.
* 이미지 같은 경우는 따로 width/height 설정하지 않아도 이미지 크기가 지정되있기 때문에 가운데 정렬이 가능
* 단점: height가 지정돼있어야 한다.

```css
.target {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    margin: auto;
}
```

---
#### ex) popup-viewer

```css
img {
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  margin: auto;
  max-width: 100%;
  max-height: 100%;
}
```

---
### vertical-align: middle;

* inline-block의 특징을 이용해 만들 수 있는 꼼수
* 여러 줄 쓸 때 좋은 방법
```html
<div class="target">
    <span>HELLO</span>
</div>
```
```css
.target {
	
}
.target:before {
    content:"";
    display: inline-block;
    vertical-align: middle;
    width: 1px;
    height: 100%;
}
```

---
### table
* table 태그와 display속성은 잘 안쓰니 패스
```html
<table>
  <tr>
    <td>
    	HELLO
    </td>
  </tr>
</table>
```

---
### display: flex
* 대상이 무엇이든 flex안의 모든 엘리먼트를 가운데 정렬시켜버린다.

```css
.target {
  display: flex;
  align-items: center;
  /* align-contents: center;*/
  
  /* flex-direction: column;
  justify-content: center;*/
}
```
