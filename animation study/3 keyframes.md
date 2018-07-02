# CSS Animation 3
* keyframes

---
## keyframes

```css
@keyframes animationname {
	keyframes-selector {
		css-styles;
	}
    25% {
    }
    from {
    }
    to {
    }
}
```

@-rule 중 하나인 keyframes

---
## keyframes
keyframes selector는

* from, to
* 0 ~ 100%

로 설정할 수 있다.

* from은 0%, to는 100%다.

---
## keyframes
* from, to와 %는 같이 쓸 수 없다.


---
## keyframes

@rule도 브라우저 prefix가 있다.

* @keyframes
* @-webkit-keyframes
* @-moz-keyframes
* @-ms-keyframes
* @-o-keyframes


---
## keyframes

* 0%를 설정안하면 애니메이션을 제외한 현재 적용되고 있는 스타일이 적용된다.

```css
.han {
	width: 30px;
}
@keyframes {
	30% {
	    	width: 100px;
	}
}
```

---

## keyframes

* 100%를 설정안하면 100%는 현재스타일이다.

```css
.han {
	width: 30px;
}
@keyframes {
	0% {
	    	width: 30px;
	}
	30% {
	    	width: 100px;
	}
/*	100% {
    		width: 30px;
	}*/
}
```

---

## keyframes

* 실습
* https://codepen.io/daybrush/pen/oyPqvO


