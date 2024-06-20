# npm: 'npm' 용어가 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램 이름으로 인식되지 않습니다

### 상황
Svelte를 학습하기 위해 npm install를 입력해 보았다. 그랬더니 "npm: 'npm' 용어가 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램 이름으로 인식되지 않습니다" 라는 오류가 나왔다.

### 해결책
처음에는 terminal이 powershell이라고 되어 있어 참고 문헌을 활용하여 키보드로 Ctrl + Shift + P를 눌러 terminal: select default profile를 입력하고 Command Prompt 클릭했다.

그러나 해결되지 않았다.

그래서 다른 글들을 살펴봤다.

이번 참고 문헌에서는 nodejs가 설치되어 있지 않으면 그럴 수 있다고 하였고 nodejs를 설치를 했던 것으로 기억하는 나는 '엥? 설마?' 라는 생각에 시스템 환경 변수 편집에 들어가 Path에 nodejs 파일의 경로를 추가해줬다.

그 후, 컴퓨터를 재부팅하고 VS code에서 다시 npm install를 입력하였더니 오류없이 실행되었다!!

> 참고 문헌:
1. https://velog.io/@bey1548/npm-npm-%EC%9A%A9%EC%96%B4%EA%B0%80-cmdlet-%ED%95%A8%EC%88%98-%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%ED%8C%8C%EC%9D%BC-%EB%98%90%EB%8A%94-%EC%8B%A4%ED%96%89%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8A%94-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8-%EC%9D%B4%EB%A6%84%EC%9C%BC%EB%A1%9C-%EC%9D%B8%EC%8B%9D%EB%90%98%EC%A7%80-%EC%95%8A%EC%8A%B5%EB%8B%88%EB%8B%A4
2. https://velog.io/@myway00/npm-%EC%97%90%EB%9F%AC-npm%EC%9D%80%EB%8A%94-%EB%82%B4%EB%B6%80-%EB%98%90%EB%8A%94-%EC%99%B8%EB%B6%80-%EB%AA%85%EB%A0%B9-%EC%8B%A4%ED%96%89%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8A%94-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8-%EB%98%90%EB%8A%94-%EB%B0%B0%EC%B9%98-%ED%8C%8C%EC%9D%BC%EC%9D%B4-%EC%95%84%EB%8B%99%EB%8B%88%EB%8B%A4.-npm-npm-%EC%9A%A9%EC%96%B4%EA%B0%80-cmdlet-%ED%95%A8%EC%88%98-%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%ED%8C%8C%EC%9D%BC-%EB%98%90%EB%8A%94-%EC%8B%A4%ED%96%89%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8A%94-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8-%EC%9D%B4%EB%A6%84%EC%9C%BC%EB%A1%9C-%EC%9D%B8%EC%8B%9D%EB%90%98%EC%A7%80-%EC%95%8A%EC%8A%B5%EB%8B%88%EB%8B%A4.-%EC%9D%B4%EB%A6%84%EC%9D%B4-%EC%A0%95%ED%99%95%ED%95%9C%EC%A7%80-%ED%99%95%EC%9D%B8%ED%95%98%EA%B3%A0-%EA%B2%BD%EB%A1%9C%EA%B0%80-%ED%8F%AC%ED%95%A8%EB%90%9C-%EA%B2%BD%EC%9A%B0-%EA%B2%BD%EB%A1%9C%EA%B0%80-%EC%98%AC%EB%B0%94%EB%A5%B8%EC%A7%80-%EA%B2%80%EC%A6%9D%ED%95%9C-%EB%8B%A4%EC%9D%8C-%EB%8B%A4%EC%8B%9C-%EC%8B%9C%EB%8F%84%ED%95%98%EC%8B%AD%EC%8B%9C%EC%98%A4