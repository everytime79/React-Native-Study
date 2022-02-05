- 사전 공부 & 연습

# React

- 컴퓨팅에서 리액트는 자바스크립트 라이브러리의 하나로서 사용자 인터페이스를 만들기 위해 사용된다. 
- 페이스북과 개별 개발자 및 기업들 공동체에 의해 유지보수된다. 리액트는 싱글 페이지 애플리케이션이나 모바일 애플리케이션의 개발 시 토대로 사용될 수 있다.

> [출처](https://ko.wikipedia.org/wiki/%EB%A6%AC%EC%95%A1%ED%8A%B8_(%EC%9B%B9_%ED%94%84%EB%A0%88%EC%9E%84%EC%9B%8C%ED%81%AC))

## 새 프로젝트 생성

1. Visual Studio Code 을 실행하고 터미널을 연다.

2. **react-native init --version 0.61.5 react_01**
입력하여 새로운 react 프로젝트를 생성

3. **cd react_01**
  새로 생성한 프로젝트 폴더로 이동

4. 상단 메뉴 - file - add folder to workspace 를 클릭하여 생성한 폴더를 선택하여 보기 쉽게 셋팅

5. **npm start** -> 우측 + 버튼을 통해 새 터미널 생성 -> **react-native run-ios** -> 시뮬레이터 실행

* ( 만약 시뮬레이션에서 붉은 화면으로 오류가 뜬다면, xcode, vscode 를 모두 셧다운 하고 재실행 -> 3번부터 다시 )

- 실행화면

![](https://images.velog.io/images/everytime79/post/9b6cfdd6-6b73-4938-ae7e-32668f0b1958/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-09%2023.51.33.png)

## 텍스트 출력

- 시뮬레이션에 보이는 화면 App.js 에서 출력된 화면이다.

텍스트를 출력하기 위해서는 react native 모듈에서 view와 text 클래스를 가져와야 한다.

**import { View, Text } from 'react-native';**

![](https://images.velog.io/images/everytime79/post/a87240fb-d410-4bf5-967d-934a2b29cb4f/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-09%2023.56.59.png)

View 안에 Text -> Hello World
(수정 후 저장 필요)

![](https://images.velog.io/images/everytime79/post/3d27ad86-3c72-4097-8925-7a39b41bb5b1/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-09%2023.58.37.png)

왼쪽 상단에 출력된 hello world의 위치를 정해줘야 한다.
Style을 추가해본다.

![](https://images.velog.io/images/everytime79/post/79cdba10-2783-4498-ba4b-267c14b9a021/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-10%2000.31.03.png)

( 수정중 )
