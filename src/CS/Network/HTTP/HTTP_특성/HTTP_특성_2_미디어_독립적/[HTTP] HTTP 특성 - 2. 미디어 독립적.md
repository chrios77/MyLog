### HTTP의 특성 - 2
HTTP의 2번째 특성은 미디어 독립적 프로토콜이라는 점이다. 클라이언트는 HTTP 요청 메시지를 통해 서버의 지원을 요청할 수 있고, 서버는 HTTP 응답 메시지로 요청받은 자원에 대해 응답할 수 있다. 그렇다면 HTTP로 어떤 자원을 주고받을 수 있을까? 이를 위해 RFC 9110 문서의 3장 1절의 Resources에 있는 문장을 참고해봤다.

![](https://velog.velcdn.com/images/chrios99/post/e7eb3b79-278e-4d30-9844-198a95baf319/image.png)

위 이미지의 빨간줄에 대한 해석은 'HTTP가 요청하는 대상을 지원한다. HTTP는 자원의 특성을 제한하지 않으며, 단지 자원과 상호 작용하는 데 사용할 수 있는 인터페이스를 정의할 뿐이다. 대부분의 자원은 URI로 식별된다.' 라는 뜻이다. 즉, HTTP는 주고받을 자원의 특성과 무관하게 그저 자원을 주고받을 수단인 인터페이스의 역할만 수행한다. 또한, HTTP를 통해서 HTML, JPEG, PNG, JSON, XML, PDF 등 다양한 종류의 자원을 주고받을 수 있다.

HTTP에서 메시지로 주고받는 자원의 종류를 미디어 타입(media type) 혹은 Multipurpose Internet Mail Extensions Type, 줄여서 MIME 타입이라고 한다.

이를 통해 알 수 있는 것은 HTTP는 주고받을 미디어 타입에 제한을 두지 않고 독립적으로 동작이 가능한 미디어 독립적인 프로토콜이라는 것이다.

### 미디어 타입
미디어 타입은 일종의 웹 세상의 확장자 같은 개념이다. HTTP를 통해 송수신하는 정보의 종류는 미디어 타입으로 나타낼 수 있다.

- 미디어 타입의 기본 형태
  미디어 타입은 기본적으로 슬래시를 기준으로 하는 '타입/서브타입' 형식으로 구성된다. 타입은 데이터의 유형을 나타내고, 서브타입은 주어진 타입에 대한 세부 유형을 나타낸다.

'''html
type/subtype
'''

미디어 타입의 종류는 매우 다양하고, 필요에 따라 새로운 미디어 타입을 등록할 수 있다. 그러므로 모든 미디어 타입을 알 필요는 없고, 그때그때 찾아서 사용하면 된다.

#### 미디어 타입 - 타입의 종류
미디어 타입의 타입에는 text, image, video, audio, application, multipart 등이 있다.

text는 일반 텍스트 형식의 데이터를 나타내는 타입.
image는 이미지 형식의 데이터를 나타내는 타입.
video는 비디오 형식의 데이터를 나타내는 타입.
audio는 오디오 형식의 데이터를 나타내는 타입.
application는 바이너리 형식의 데이터 타입.
multipart는 각기 다른 미디어 타입을 가질 수 있는 여러 요소로 구성된 데이터를 나타내는 타입.

#### 미디어 타입 - 서브타입 종류
서브타입의 종류는 타입마다 다양하다.

##### text
text 타입일 때 사용할 수 있는 서브타입으로는 plain, html, css, javascript 등이 있다.

plain은 '평문 텍스트 문서' 라는 의미이다.

'''html
type/plain
'''

html은 'HTML 문서' 라는 의미다.

'''html
type/html
'''

css는 'CSS 문서' 라는 의미다.

'''html
type/css
'''

javascript는 '자바스크립트 문서' 라는 의미다.

'''html
type/javascript
'''

##### image
image 타입일 때 사용할 수 있는 서브타입은 png, jpeg, webp, gif 등 다양하다.

png는 'PNG 이미지' 라는 의미이다.

'''html
image/png
'''

jpeg는 'JPEG 이미지' 라는 의미이다.

'''html
image/jpeg
'''

webp는 'WebP 이미지 '라는 의미다.

'''html
image/webp
'''

gif는 'GIF 이미지' 라는 의미다.

'''html
image/gif
'''

##### video
video 타입일때 사용할 수 있는 서브타입은 mp4, ogg, webm 등 다양하다.

mp4는 MP4 비디오 라는 의미다.

'''html
video/mp4
'''

ogg는 OGG 비디오 라는 의미다.

'''html
video/ogg
'''

webm은 WebM 비디오 라는 의미다.

'''html
video/webm
'''

##### audio
audio 타입일 때 사용할 수 있는 서브타입은 midi, wav 등 다양하다.

midi는 MIDI 오디오 라는 의미다.
'''html
audio/midi
'''

wav는 WAV 오디오 라는 의미다.

'''html
audio/wav
'''

##### application
application 타입일 때 사용할 수 있는 서브타입은 octet-stream, pdf, xml, json, x-www-form-urlencoded 등 다양하다.

octet-stream는 알 수 없는 바이너리 데이터를 포함한 일반적인 바이너리 데이터 라는 의미다.

'''html
application/octet-stream
'''

pdf는 PDF 문서 형식 데이터 라는 의미다.

'''html
application/pdf
'''

xml는 XML 형식 데이터 라는 의미다.

'''html
application/xml
'''

json는 JSON 형식 데이터 라는 의미다.

'''html
application/json
'''

x-www-form-unlencoded는 HTML 입력 폼 데이터, 키-값 형태의 입력값을 URL 인코딩한 데이터 라는 의미다.

'''html
application/x-www-form-unlencoded
'''

##### multipart
multipart 타입일 때 사용할 수 있는 서브타입은 form-data, encrypted 등이 있다.

form-data는 'HTML 입력 폼 데이터' 라는 의미다.

'''html
multipart/form-data
'''

encrypted는 '암호화된 데이터' 라는 의미다.

'''html
multipart/encrypted
'''

#### 기타 사항
*는 여러 미디어 타입을 통칭하기 위해 사용된다. 예를 들어,

'''html
text/*
'''

는 text 타입의 머든 서브타입을 나타낸다.

'''html
image/*
'''

는 image 타입의 모든 서브타입을 나타낸다.

혹은 이렇게도 사용할 수 있다

'''html
*/*
'''

이는 모든 미디어 타입을 나타낸다.

#### 미디어 타입의 매개변수
미디어 타입에는 매개변수가 포함될 수 있다. 그러나 필수는 아니고 선택이다.

매개변수까지 적은 미디어 타입의 형태는

'''java
타입/서브타입;매개변수=값
'''

형태이다.

예를 들어,


'''html
text/html;charset=UTF-8
'''

이 미디어 타입의 의미는 HTML 문서 타입이며, HTML 문서 내에서 사용된 문서는 UTF-8로 인코딩되었음을 의미한다.

> 참고 문헌:
1. 혼자 공부하는 네트워크, 강민철 저, p.274 ~ p.276
2. https://developer.mozilla.org/ko/docs/Web/HTTP
3. https://www.rfc-editor.org/rfc/rfc9110.html