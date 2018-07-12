# CSS 80% JS 20% 2
1. DOM


---

## Document Object Model

https://www.w3schools.com/js/js_htmldom.asp

<br/>
<p align="center"><img src="https://www.w3schools.com/js/pic_htmltree.gif"/></p>
  
---


## A, BR, P, DIV, SPAN, ...의 뜻
* 마크업을 할 일이 많이 없지만 알면 알맞게 사용할 수 있다.
* A : 목적지 / 링크
* BR: 줄 바꿈
* DIV: 영역
* SPAN: 구간 또는 단어, 문단보다 작은 의미
* P: 문장
..
<br/>

* 이런 느낌이다. span < p < div
* p태그 안에 div(display: block) 넣을 수 없다.
---
## DOCTYPE

* 선언문

http://webdir.tistory.com/40

```
<!DOCTYPE html>
```

* HTML5 표준이다.
* 있고 없고의 차이가 있다.

---
## document.body 차이
* style에 별다른 선언을 하지 않은 상태이다.

||선언 전 | 선언 후|
|---|---|---|
|height|최소 height가 화면 사이즈|최소 height가 컨텐츠 사이즈|
|clientHeight|화면 사이즈|컨텐츠 사이즈|
|offsetHeight|컨텐츠 사이즈<br/>(최소 화면 사이즈)|컨텐츠 사이즈|
|scroll(Top/Left)| 예상값 | 0|
|height: 100%|화면 사이즈| 0|
---
## scroll (Top/Left)가 0인 경우
* 왜 0일까요?
	* html도 하나의 DOM이다.
	* html, body 둘 다 컨텐츠 사이즈에 대해 유동적으로 같이 늘어난다.

---
## scroll (Top/Left)가 0인 경우
* 0이 아닌 정상적인 값이 나오려면?
	* 정상적인 방법
		* document.documentElement.scrollTop/Left를 쓴다.
		documentElement는 ```html```이다.
	* 정상적이지 않는 방법(쓰지는 말자)
		* html에 height: 100%; overflow: hidden;
    	body에 height: 100%; overflow: auto;를 쓰면 document.body.scrollTop을 쓸 수 있다.
        
---

## height: 100%;
```html
<body>
  <div style="height: 100%;">1</div>
</body>
```

* doctype 선언 전까지는 아주 잘 된다
* doctype 선언 후 0이다.

```
html, body {
    height: 100%;
}
```
* 쓰면 잘 작동 된다.

