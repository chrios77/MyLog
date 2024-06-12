# [HTML] body 태그

![](https://velog.velcdn.com/images/chrios99/post/c2aa55ea-77b0-4762-887f-61625f42c698/image.png)

> 사진 출처 : https://namu.wiki/w/HTML

### HTML의 기본 구조

head 태그에 대해 알아보기 전에 HTML 문서의 기본 구조를 다시 한 번 보자.

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- 문서의 정보(메타데이터) -->
    </head>
    <body>
        <!-- 문서의 내용 -->
    </body>
</html>

```
위의 코드가 HTML의 기본 구조이다.

### body 태그의 위치

```html
<body>
        <!-- 문서의 내용 -->
    </body>
```

이 코드를 body 태그라고 한다.

HTML 기본구조 중에서 head 태그는 어디에 위치해 있을까?

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- 문서의 정보(메타데이터) -->
    </head>
    <body>
        <!-- 문서의 내용 -->
    </body>
</html>

```

아주 금방 찾아낼 수 있을 텐데 HTML 기본구조를 살펴보면 body 태그는 head 태그 다음에 위치한다는 것을 알 수 있다.

### body 태그란?
body 태그는 해당 HTML 문서의 텍스트, 하이퍼링크, 이미지, 리스트 등과 같은 모든 콘텐츠를 포함하는 영역을 정의할 때 사용한다. 간단히 말하자면 HTML 문서의 내용이다.

웹 사이트에 들어가면 사용자 눈에 직접적으로 보여주는 내용들이기도 하다. 즉, 컴퓨터 화면에 보여지는 부분을 body 태그를 통해 구현할 수 있게 된다.

**참고)** 어떤 자료에서는 body 태그를 섹션 루트라고도 한다. 그러나 그냥 문서의 주내용이라고 보는 것이 이해하기 편한 것 같다.

### body 태그의 특징
- html 태그의 두 번째 자식 요소이다.
- body 태그는 하나의 HTML 문서에 하나만 존재할 수 있다.
- HTML의 기본 구조에 반드시 필요한 필수 태그이다.
- 반드시 head 태그를 형제 요소로 두고 있어야 하며 이때, head 태그가 먼저 위치해 있어야 한다.
- body 태그는 스크립트 연동을 포함한 응용 프로그램의 연동 등에서 활용되는 태그이다.
-


### body 태그를 잘못 마크업한 사례 - 1. body 태그가 여러 개인 경우

```html
<!DOCTYPE html>
<html>
    <head>

    </head>
    <body>

    </body>
    <body> <!-- HTML 문서에는 하나의 body 태그만 존재해야 합니다. -->

    </body>
</html>
```

이 코드를 보면 body 태그가 2개이다. HTML 문서에서 body 태그는 하나만 존재해야 하므로 이런 형태의 코드는 있을 수 없다.

### body 태그를 잘못 마크업한 사례 - 2. body 태그가 없는 경우

```html
<!DOCTYPE html>
<html>
    <head>

    </head>
    <div> <!-- body 태그가 존재하지 않음 -->

    </div>
</html>
```

이 코드를 보면 body 태그가 존재하지 않는다. HTML 문서에서 HTML 기본구조에 성립하기 위해 반드시 body 태그는 하나가 존재해야 한다. 그러므로 이런 형태의 코드는 있을 수 없다. 또한, 올바르지 않은 마크업은 자바스크립트의 구현이나 다른 웹 기술 등의 연동에 있어서 오류가 생길 가능성도 매우 커져 올바르게 사용해야 한다.

### body 태그의 속성
body 태그의 속성으로는 link, alink, vink, bgcolor, background, text 등이 있다.

- link  속성의 속성값은 color이며, 링크에 연결된 텍스트의 색깔을 설정할 때 사용한다.
- alink 속성의 속성값은 color이며, 링크를 클릭 시 변경되는 색깔을 설정할 때 사용한다.
- vlink 속성의 속성값은 color이며, 방문한 적이 있는 링크의 색깔을 설정할 때 사용한다.
- bgcolor 속성의 속성값은 color이며, 배경 색깔을 설정할 때 사용한다.
- background 속성의 속성값은 URL이며, 배경이미지를 설정할 때 사용한다.
- text 속성의 속성값은 color이며, HTML 문서 안에 들어가는 글자의 기본 색깔을 설정할 때 사용한다.

### body 태그의 사용법
여는 body 태그에 속성과 속성값을 적어주고 속성값에는 ""를 사용하여 나타낸다. 아래 코드는 그 예시이다.

```html
<body link = "FF0000" alink = "#FFA500" vlink = "#1010B5" bgcolor = "#F3F3F3" background = "" text = "591717">
	<!-- 문서의 내용 -->
</body>
```

### 그러나 HTML5에서 body 태그의 속성들은?
HTML5에서는 body 태그의 속성들을 더 이상 지원하지 않는다. body 태그의 속성들은 주로 예쁘게 꾸미는 디자인에 관한 내용들인데, 이를 이젠 CSS로 작성하게 되었다. 이러면 코드의 가독성이 높아지고 코드 수정 시에도 편해진다.

> 참고 문헌:
1. https://codingeverybody.kr/html-html-%ED%83%9C%EA%B7%B8-%EC%98%AC%EB%B0%94%EB%A5%B8-%EC%9D%B4%ED%95%B4%EC%99%80-%EC%82%AC%EC%9A%A9-%EB%B0%A9%EB%B2%95/
2. https://www.tcpschool.com/html-tags/body
3. https://it-plus.tistory.com/entry/HTMLHTML5-1%EA%B8%B0%EB%B3%B8%ED%83%9C%EA%B7%B8-body-510
4. https://developer.mozilla.org/ko/docs/Web/HTML/Element/body
5. https://www.w3schools.com/tags/tag_body.asp