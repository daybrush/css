## CSS STUDY


* overflow

---


## IOS 및 Safari 이슈
* border-radius가 있는 경우 overflow 미적용 이슈


```css
-webkit-mask-image: -webkit-radial-gradient(white, black);
```
* border가 있는 경우.. border에는 영향을 끼침...

---
## border과 border-radius관련 safari 이슈
* 조건
	* border-radius가 걸려있지 않은 모서리가 있다. (상/하)
		* **좌/우는 잘 적용 된다.**
	* 모서리에 border가 걸려있다.
* 결과
 	* overflow가 border-radius 형태로 적용되지 않는다.
* 해결방법
	* border-top 또는 border-bottom을 대체할 수 있어야 한다.