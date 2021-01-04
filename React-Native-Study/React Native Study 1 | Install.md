# 공부 시작

* 블로그의 글들은 강의를 들으며 복습 & 공부용으로 기록합니다.

* 오타와 틀린 부분은 지적해주시면 감사하겠습니다. 

<span style="color:red">** 글에 문제가 있을 경우 알려주시면 바로 삭제하겠습니다. **</span>

# React Native
- 페이스북에서 만든 오픈소스 모바일 응용 프로그램
- 네이티브 앱 개발을 위한 자바스크립트 프레임 워크
- 크로스 플랫폼
- 하나의 코드 개발을 통해 IOS 와 안드로이드에서 동일하게 동작시킬 수 있는 API
- 자바스크립트를 기본 언어로 사용
- Java, Kotlin 언어에 의존하는 안드로이드 네이티브 앱, 혹은 Swift 언어에 의존하는 ios 네이티브 앱 개발보다 진입 장벽이 낮고, 훨씬 쉽다는 장점을 가지고 있다.

>html, css, 자바스크립트, ES6, 리액트의 선수 지식이 도움이 됨

## 원리

![](https://images.velog.io/images/everytime79/post/7d3ae855-33bf-40b6-b8a3-45ed3ea6fd9a/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2014.58.03.png)

[사진 & 영상 출처](https://www.inflearn.com/course/%EB%A6%AC%EC%95%A1%ED%8A%B8-%EB%84%A4%EC%9D%B4%ED%8B%B0%EB%B8%8C-%EA%B8%B0%EC%B4%88/dashboard)

## 2가지 방법
1. Expo CLI
	* Pros
        * 개발 환경 구축 용이
        * 실제 개발이 쉽고 편함
    * Cons
        * OS Layer와 직접 상호작용 불가능
        (Java, Kotlin, Obj-C, Swift 로 추가 작성 불가)
        * Expo에서 제공해주는 모듈만 사용 가능
        * Expo Client에서는 잘 동작하지만 
        실제 Simulator & 단말기에서 동작하지 않을 수 있음
        * 개발 관점에서의 자유도 낮음

2. React Native CLI
	* Pros
        * Expo로는 접근하지 못하는 Native 기능에 접근 가능
        (Native 모듈 사용 자유도 높음)
        * 원하는 언어로 추가 작성 가능
        (Custom Native 모듈 사용 가능)
        * 필요한 기능이 있는 경우 모듈을 직접 제작 가능
        * OS Layer와 직접적인 상호작용 가능
    * Cons
        * 초기 개발환경 구축 및 실제 앱 개발 시, 다소 시간이 소요
        * 단, Mac 환경일 경우에만, IOS & Android 시뮬 지원
        (윈도우에서는 IOS 시뮬을 지원하지 않음)

## 초기 환경 구축 & 설치할 항목
1. nvm ( Node Version Manager )
2. node.js
3. npm ( Node Package Manager )
4. Android Studio
5. Java
6. Xcode
7. visual Studio Code
8. CocoaPod
9. React Native CLI

### nvm ( MacOS )
1. 터미널 열어 코드를 복사 & 붙여넣기 , 비밀번호 입력
**0.33.11 version을 사용했습니다.**

>설치 참고 : [https://gist.github.com/falsy](https://gist.github.com/falsy/8aa42ae311a9adb50e2ca7d8702c9af1)

```
sudo curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```

>**에러 : xcrun error**
해결방법 참고 : [swtpumpkin](https://swtpumpkin.github.io/develop/mojave-update-git-error/)

```
// 에러 코드
xcrun: error: invalid active developer path
(/Library/Developer/CommandLineTools), missing xcrun at:
/Library/Developer/CommandLineTools/usr/bin/xcrun
```

**해결 방법 : 터미널 열고 아래 코드를 한 개씩 순서대로 추가**

```
// 설치
xcode-select --install

// 확인
xcode-select -v
-> xcode-select version 2384.

// 다시 nvm 설치
sudo curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```

2. (에러 없으면 진행) 확인
```
nvm ls
-> -bash: nvm: command not found
// 이렇게 떠도 정상
```

3. 아래 코드를 통해 vi 에디터를 실행
```
vi ~/.bash_profile
```

4. 'i' 버튼을 눌러 아래 코드를 insert
```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
```

5. 위 코드를 복붙했다면, 'ESC' 키 -> ':wq' (저장 후 종료) 치고 엔터
만약 E45: 'readonly' option is set~ 이 뜬다면 :wq! 치고 엔터

6. 재시작 합니다. 아래 코드 치고 엔터

```
source ~/.bash_profile
```

7. 버전 확인 -> **nvm 설치 완료**
```
nvm --version
0.33.11
```

### node.js
1. 설치한 nvm 을 사용하여 설치가 가능합니다.
2. 터미널에 코드를 입력합니다.

```
nvm install 10.15.1 

-> 실행하면 
~ Creating default alias: default -> 10.15.1 (-> v10.15.1) 라고 뜸
```

**10.15.1 version을 사용했습니다.**

3. 확인 -> **node.js 설치완료**

```
node -v
v10.15.1
```

>nvm 을 통해 node.js 여러 버전을 사용할 수 있다.
-> nvm install ?.?.? 코드를 통해 설치가 가능하고
-> nvm ls 를 통해 설치한 모든 항목을 볼 수 있다.
(이 때, -> 가 있는 버전이 선택된 버전이다.)
-> 10.15.1 혹은 선택한 버전을 사용하기 위해 nvm use 10.15.1 입력

### npm

>- node.js로 개발된 프로그램을 편리하게 설치, 업데이트, 삭제 해주는 프로그램
- node.js로 생성 & 작성된 패키지를 관리하는 프로그램

npm은 node.js가 설치하면 함께 설치가 된다.
1. 확인은 해준다. 

```
 npm --version
6.4.1
```

### Android Studio

1. [Android Studio](https://developer.android.com/studio?hl=ko) 에 가서 dmg 파일 다운로드
2. 다운받은 dmg 파일을 더블 클릭, Android Studio -> Applications로 옮긴다.
3. 다 옮겨지면 런치패드에서 실행

4. Do not import settings 선택
![](https://images.velog.io/images/everytime79/post/28ae4c7a-e1cb-40be-9e77-e21917383d23/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2019.55.58.png)

5. Welcome, **Next** -> Standard, **Next** -> UI Theme 선택 후 **Next** -> **Finish** -> Downloading Components -> 완료되면 **Finish**

6. 설치가 완료되면 하단 Configure을 눌러 SDK Manager 열기

![](https://images.velog.io/images/everytime79/post/d36314ba-fe2c-49c3-8524-7ded1b494275/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2020.08.36.png)

7. **android 10.0(Q) version을 사용했습니다.**
하단의 Show Package Detail -> 설치할 항목들을 클릭하여 체크 표시

![](https://images.velog.io/images/everytime79/post/e1b5e404-c683-4f20-b16e-aed87b7818ba/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2021.23.27.png)

8. 체크로 선택한 후 아래 Apply - OK 를 눌러 설치한다.

![](https://images.velog.io/images/everytime79/post/89d5be0f-6840-44e5-a3e4-6e6c2d707d18/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2020.57.04.png)

9. 이번에는 Configure -> AVD Manager 을 열어준다. 하단의 + Create Virtual Device.. (definition) 을 클릭

10. Phone에서 원하는 가상 디바이스를 선택 후 Next - 다운받은 SDK 버전을 확인하고 Next - Finish

![](https://images.velog.io/images/everytime79/post/7c6981cc-6f51-44d2-a959-d46621a8ccb2/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2021.27.44.png)


### Android Studio 환경 변수 설정
>[zsh, bash 환경설정 참고](https://richwind.co.kr/119)

11. **환경 변수 설정**, 터미널 열고 아래 코드 입력 ->

```
vi ~/.bash_profile
```

12. 알파벳 E -> i 를 순서대로 눌러 수정을 한다.  -> 아래 코드 복사해서 상단에 붙여넣기

```
export ANDROID_HOME=/Users/Soo/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

![](https://images.velog.io/images/everytime79/post/56b832aa-7a84-47e5-ad72-33ab98c9b0ee/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2021.37.34.png)

> - **주의사항** : export ANDROID_HOME=/Users/Soo/Library/Android/sdk
이 부분에서 주소는 SDK Manager 에서 상단 주소와 같게 타이핑해준다.

![](https://images.velog.io/images/everytime79/post/7e2ac921-7b31-476f-be85-22d04f35d6bb/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2021.35.10.png)

13. 입력을 하고 ESC 키 -> :wq -> 엔터

14. 확인 
```
adb 
// 상단으로 올라가보면 아래처럼 확인할 수 있다.
Soo@Park-MacBookPro ~ % adb
Android Debug Bridge version 1.0.41
Version 30.0.5-6877874

```

> 만약, **zsh: command not found: adb**
```
adb version
zsh: command not found: adb
// 이렇게 나온다면, vi를 다시 열어 하단 빈 곳에 코드 한 줄을 추가시킨다. ->
export PATH=${PATH}:/Users/*이름*/library/android/sdk/tools:${PATH}:/Users/*이름*/library/android/sdk/platform-tools
// *이름* 은 내 맥북 사용자 명
```

여기까지 안드로이드 스튜디오 설치 완료

### JAVA

1. Oracle 홈페이지 - [Java SE 11 (LTS) Oracle JDK Download](https://www.oracle.com/kr/java/technologies/javase-jdk11-downloads.html) 에서 macOS Installer .dmg 파일을 다운받아준다.
( 약 166.82 MB, 로그인 필수 )

2. 다운받은 .dmg 파일을 더블 클릭 -> JDK .pkg 파일 더블 클릭 -> 설치를 진행한다. 

3. 확인

```
java --version

java 11.0.9 2020-10-20 LTS
Java(TM) SE Runtime Environment 18.9 (build 11.0.9+7-LTS)
Java HotSpot(TM) 64-Bit Server VM 18.9 (build 11.0.9+7-LTS, mixed mode)
```

>자바 경로는 
```
cd /Library/Java/JavaVirtualMachines/
ls
-> jdk-11.0.9.jdk
```

4. 설치 완료

### Xcode
앱스토어 - Xcode 검색 후 받기를 통해 설치하면 된다.

추가로 Xcode 실행 후 상단 메뉴 Xcode - Preferences... - Locations - Command Line Tools -> Xcode ?.?.? 가 설정되어 있는지 확인한다.
안되어 있으면 설정

### Visual Studio Code

>[visual studio code](https://code.visualstudio.com/) 홈페이지에서 다운
혹은
[버전 선택](https://code.visualstudio.com/updates/v1_52) 하여 다운

January 2020 (version 1.42를 추천?)

Mac을 사용하기 때문에 Mac 클릭

![](https://images.velog.io/images/everytime79/post/6c6e0571-1c4a-4e30-90ca-0a1d47d533ce/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-03%2022.05.21.png)

### [CocoaPod, 블로그 링크](https://soosdev.tistory.com/5)

터미널을 열고
sudo gem install cocoapods -v 1.8.4 (사용할 버전)
* 만약 오류가 뜬다면, 사용하는 Mac버전과 호환되는 코코아팟 버전을 찾아 설치

pod --version 

입력하여 설치가 잘 되었는지 확인한다. 

### React Native CLI

(글로벌 설치)
npm install -g react-native-cli

react-native --version 

->react-native-cli: 2.0.1
react-native: n/a - not inside a React Native project directory

똑같이 설치가 잘 되었는지 확인한다. 


