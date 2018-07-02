# CSS Amimation 5

* opacity
* fade in, out
* blink

---
## opacity
* 불투명도
* 기본값 : 1


---
## fade in
* 점점 나타나다.
* opacity가 0에서 1로 가는 효과
## fade out
* 점점 사라지다.
* opacity가 1에서 0로 가는 효과

---
## fade in

https://codepen.io/daybrush/pen/GGPbXb

```css
@keyframes fadeIn{
/*    0% {
        opacity: 0;
    }*/
    100% {
        opacity: 1;
    }
}

```
---

## fade out
https://codepen.io/daybrush/pen/eKbwQG

```css
@keyframes fadeOut{
/*    0% {
        opacity: 1;
    }*/
    100% {
        opacity: 0;
    }
}

```

---

## Blink 1

https://codepen.io/daybrush/pen/BVvgXj

```css
@keyframes blink {
    50% {
    	opacity: 0;
    }
}
```


---

## Blink 2

https://codepen.io/daybrush/pen/PaXMoq

```css
animation-direction: alternate;


@keyframes blink {
    100% {
    	opacity: 0;
    }
}
```

---
## Loading(Blink)

https://codepen.io/daybrush/pen/VdqovJ
