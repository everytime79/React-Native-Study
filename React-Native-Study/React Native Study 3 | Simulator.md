# ios Simulator

## 실행

npm start -> 새로운 터미널 추가 ->

![](https://images.velog.io/images/everytime79/post/c3cc0cf9-93ab-499e-a5f3-6d90a3a2a671/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-04%2000.27.06.png)

새로운 터미널에서 react-native run-ios 입력 ->

ios 시뮬레이터가 보이는 것을 확인 

![](https://images.velog.io/images/everytime79/post/67e34567-d7ac-442f-b9c1-ed2e4a87ac86/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-04%2000.43.40.png)

* 시뮬레이터에서 보이는 기본 화면은 App.js 를 통해 보이는 것

![](https://images.velog.io/images/everytime79/post/1897ecf0-9036-47ac-9d7e-13f0f211718c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-04%2000.45.30.png)

## 새로고침

* App을 수정하고 나서 커맨드 키 + R 을 누르면 새로고침이 된다. 
* 커맨드 키 + D 를 눌러 Disable Fast Refresh 를 확인할 수 있는 데, Fast Refresh 가 활성화 되어 있다면, 이것은 코드를 수정하고 저장을 하면 새로고침을 할 필요 없이 바로 반영이 된다. 만약 Disable Fast Refresh 를 누르면 저장을 해도 바로 반영이 되지 않는다. 

## 기기 선택

예시로 만약 아이폰 8 플러스 가상머신을 사용해보고 싶다면,

react-native run-ios --simulator="iPhone 8 Plus"

라고 입력하면 된다. 

* 다른 모델명을 보고싶다면, 1.52.1 Visual Studio Code 기준
시뮬레이터 - 상단 메뉴 - File - Open Simulator - IOS 14.2 를 누르면 여러 기종들이 있는 것을 확인할 수 있다.

![](https://images.velog.io/images/everytime79/post/21959709-da55-4ffc-a461-2e541f08b671/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-04%2000.59.49.png)

* 만약, Visual Studio Code가 구버전일 경우, 시뮬레이터 - 상단 메뉴 Hardware - Device - ios 13.? 에서 확인할 수 있다. 

# Android Simulator

## 실행

수정중
