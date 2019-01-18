# CSS 스터디 4주차

* border 1
* border-radius 1
---
## border 1
* 테두리 선
* ex) border: 4px solid black;
* border: size style color;
* border-left, top, right, bottom


---
## border-style
* none
* dotted: 점
* dashed: 저어어어엄
* solid: 실선
* double: 실선 2개
* ...

https://www.w3schools.com/css/tryit.asp?filename=trycss_border-style

---

## border

<img src="http://html-tuts.com/wp-content/uploads/css-arrows-from-borders-explained.png"/>

---
## border-radius 1
* 해당 element의 코너의 반지름을 정할 수 있는 속성
* border-radius: 50%;
	* top-left: 50%, top-right: 50%
	* bottom-right: 50%, bottom-left: 50%
* border-radius: 50% 0px;
	* top-left: 50%, top-right: 0px
	* bottom-right: 50%, bottom-left: 0px
* border-radius: 50% 0px 30%;
	* top-left: 50%, top-right: 0px
	* bottom-right: 30%, bottom-left: 0px
* border-radius: 50% 0px 30% 20%;
	* top-left: 50%, top-right: 0px
	* bottom-right: 30%, bottom-left: 20%


---
## border-radius 1
* border-radius: horizontal / vertical;
<img src="https://user-images.githubusercontent.com/3433062/38003855-70254d1e-3274-11e8-8a68-b6b51d80e447.png">

https://codepen.io/laviperchik/pen/mAHwE

---
## border-radius 1
* 자연스런 버튼: border-radius: 5px;
* 원: border-radius: 50%;
* 럭비: border-radius: 100% 0px;
* 달걀: border-radius: 50% / 40% 40% 60% 60%;
* 반원: border-radius: 50% / 100% 100% 0px 0px;

https://codepen.io/daybrush/pen/geomYR