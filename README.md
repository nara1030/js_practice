JS 연습
=====
* JS 연습 공간
* 틀린 부분이 많을 수 있음
* 나중에 작성해보기 → [URL 치고 페이지가 표시되기까지의 과정 정리](https://github.com/nara1030/TIL/blob/master/docs/thinking_list/process_when_typing_a_url.md)
- - -
## 목차
1. [정리](#정리)
	1. [DOM](#DOM)
	2. [브라우저](#브라우저)
2. [참고](#참고)

## 정리
### DOM
* DOM이란?
	* HTML, XML 문서의 프로그래밍 Interface
		* 웹 페이지를 스크립트 또는 프로그래밍 언어들에서 사용될 수 있게 연결시켜주는 역할 담당
	* [W3C DOM](https://www.w3.org/DOM/), [WHATWG DOM](https://dom.spec.whatwg.org/) 표준은 대부분의 **브라우저에서** DOM을 **구현**하는 기준
* DOM과 자바스크립트
	* API(web or XML page) = DOM + JS(scripting language)
		* DOM은 프로그래밍 언어는 아니지만 DOM이 없다면 자바스크립트 언어는 웹 페이지 또는 XML 페이지 및 요소들과 관련된 모델이나 개념들에 대한 정보를 갖지 못함
	* DOM은 프로그래밍 언어와 독립적으로 디자인
* DOM에 어떻게 접근할 수 있는가?
	* DOM을 사용하기 위해 특별히 해야 할 일은 없음
		* 모든 웹 브라우저는 자신만의 방법으로 DOM을 구현(∴ 스크립트가 접근할 수 있는 웹 페이지 만들기 가능)
	* 스크립트를 작성할 때, 문서 자체를 조작하거나 문서의 children을 얻기 위해 `document` 또는 `window` elements를 위한 API 즉시 사용 가능
* 중요한 데이터 타입들
* DOM interfaces
	1. Interface와 Object
		* 많은 objects(DOM specification)가 여러 개의 다른 interfaces와 연관되어 있음  
			```txt
			1. HTML FORM element
				- HTMLFormElement: name property
				- HTMLElement: className property
			2. table object
				- HTMLTableElement: createCaption, insertRow 등
				- HTMLElement
				- Node
			```
		* table object를 참조하면, 3가지 interfaces 사용 가능  
			```html
			var table = document.getElementById("table");
			var tableAttrs = table.attributes; // Node/Element interface
			for (var i = 0; i < tableAttrs.length; i++) {
				// HTMLTableElement interface: border attribute
				if(tableAttrs[i].nodeName.toLowerCase() == "border")
					table.border = "1"; 
			}
			// HTMLTableElement interface: summary attribute
			table.summary = "note: increased border";
			```
	2. DOM의 핵심 Interface
* DOM API 테스팅

- - -
1. DOM(Document Object Model)
2. DOM tree
3. DOM Query
4. DOM Traversing
5. DOM Manipulation
6. style

##### [목차로 이동](#목차)

### 브라우저
웹 페이지, 즉 DOM은 웹 브라우저를 통해 그 내용이 해석되어 웹 브라우저 화면에 나타나

##### [목차로 이동](#목차)

## 참고
* JS Test
	1. [w3schools](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_default)
	2. [liveweave](https://liveweave.com/)
* DOM
	1. [DOM 소개](https://developer.mozilla.org/ko/docs/Web/API/Document_Object_Model/%EC%86%8C%EA%B0%9C)
	2. [DOM](https://poiemaweb.com/js-dom)
* [브라우저는 어떻게 동작하는가?](https://d2.naver.com/helloworld/59361)
* [모던 자바스크립트 튜토리얼](https://ko.javascript.info/)
* [Where should I put <script> tags in HTML markup?](https://stackoverflow.com/questions/436411/where-should-i-put-script-tags-in-html-markup)
* [제이쿼리](http://tcpschool.com/jquery/intro)
* .

##### [목차로 이동](#목차)
