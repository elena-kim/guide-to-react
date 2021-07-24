# the-easiest-react

## Contents
- [개요](#개요)
- [개발 준비](#개발-준비)
- [명령어](#명령어)
- [CRA 구조](#cra-구조)
- [State와 Props](#state와-props)
- [Life Cycle](#life-cycle)

<br>

***


## 개요
**React**는 사용자 인터페이스를 만드는 데 사용되는 오픈소스 자바스크립트 라이브러리로, 페이스북에서 개발했습니다. 싱글 페이지 애플리케이션이나 모바일 애플리케이션 개발에 사용될 수 있으며 리액트를 사용하는 웹 사이트 및 프로그램은 아래와 같은 것들이 있습니다.

![](https://img.shields.io/badge/-Netflix-E50914?style=for-the-badge&logo=Netflix&logoColor=white)
![](https://img.shields.io/badge/-Discord-5865F2?style=for-the-badge&logo=Discord&logoColor=white)
![](https://img.shields.io/badge/-Reddit-FF4500?style=for-the-badge&logo=Reddit&logoColor=white)
![](https://img.shields.io/badge/-Amazon&nbsp;AWS-232F3E?style=for-the-badge&logo=Amazon-AWS&logoColor=white)
![](https://img.shields.io/badge/-Twitch-9146FF?style=for-the-badge&logo=Twitch&logoColor=white)
![](https://img.shields.io/badge/-Twitter-1DA1F2?style=for-the-badge&logo=Twitter&logoColor=white)
![](https://img.shields.io/badge/-Instagram-E4405F?style=for-the-badge&logo=Instagram&logoColor=white)
![](https://img.shields.io/badge/-Facebook-1877F2?style=for-the-badge&logo=Facebook&logoColor=white)
![](https://img.shields.io/badge/-npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)

### 프론트엔드 프레임워크 간 비교
- Angular
- Vue
- React

<br>

### React가 인기있는 이유?
[참고](https://www.freecodecamp.org/news/the-react-handbook-b71c27b0a795/)

**다른 대안보다 덜 복잡함**  
React가 발표되었을 때 Ember.js와 Angular 1.x가 프레임워크로 가장 많이 선택되었습니다. 이 두 가지 모두 코드에 너무 많은 규칙을 부과하여 기존 앱을 이식하는 것이 전혀 편리하지 않았습니다.

React는 기존 프로젝트에 매우 쉽게 통합되도록 선택했습니다. 기존 코드베이스에 이를 도입하기 위해 Facebook에서 그렇게 해야 했기 때문입니다. 또한, 이 2개의 프레임워크는 테이블에 너무 많은 것을 가져온 반면 React는 전체 MVC 스택 대신 View 레이어만 구현하기로 선택했습니다.

**완벽한 타이밍**  
당시 Google은 Angular 2.x와 함께 이전 버전과의 비호환성 및 주요 변경 사항을 발표했습니다. Angular 1에서 2로 이동하는 것은 다른 프레임워크로 이동하는 것과 같았습니다. 따라서 React가 약속한 실행 속도 향상과 함께 개발자가 시도하고 싶어하는 것이 되었습니다.

**페이스북 지원**  
물론 페이스북의 지원을 받는 것은 프로젝트가 성공할 경우 이익을 얻을 것입니다.

Facebook은 현재 React에 큰 관심을 가지고 있으며 Open Source의 가치를 보고 있으며 이는 자체 프로젝트에서 React를 사용하는 모든 개발자에게 큰 장점입니다.

<br>

### React 특징
[참고](https://medium.com/react-native-seoul/react-%EB%A6%AC%EC%95%A1%ED%8A%B8%EB%A5%BC-%EC%B2%98%EC%9D%8C%EB%B6%80%ED%84%B0-%EB%B0%B0%EC%9B%8C%EB%B3%B4%EC%9E%90-01-react-js%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80-ad8ba252ee28)

### ✔️ React는 선언형(Declarative)이다.
리액트는 선언형 성격에 맞게 컴포넌트(원하는 결과, 뷰)를 얻기 위해 `<tag></tag>` **jsx 문법**을 통해 구현한다. 즉, jsx를 얻기 위한 알고리즘에 대한 구현을 하지 않는다. 이와 같은 선언형 특성은, 리액트를 사용할 때 화면 설계라는 초점에 맞춰서 개발할 수 있도록 해주므로, 다른 부분에 대한 고민을 최소화 해주어 **높은 생산성을 보장**할 수 있도록 해준다.

### ✔️ React는 컴포넌트 기반으로 재사용성이 뛰어나다.  
**컴포넌트**는 독립적인 단위의 소프트웨어 모듈을 말한다. 즉 소프트웨어를 독립적인 하나의 부품으로 만드는 방법이다. 리액트는 웹에서 쓰는 각 요소들을 컴포넌트로 만들 수 있게 해 기존의 UI를 다른 화면에서 다시 쓰거나, 다른 프로젝트에서 다시 쓸 수 있도록 하는 장점(**높은 재사용성**)을 가진다.

### ✔️ React는 Virtual DOM(가상돔)기반으로 가볍다. 
Another notable feature is the use of a virtual Document Object Model, or virtual DOM. React creates an in-memory data-structure cache, computes the resulting differences, and then updates the browser's displayed DOM efficiently. This process is called **reconciliation**. This allows the programmer to write code as if the entire page is rendered on each change, while the React libraries only render subcomponents that actually change. This selective rendering provides a major **performance boost**. It saves the effort of recalculating the CSS style, layout for the page and rendering for the entire page.

<br>

***

## 준비

1. [node.js](https://nodejs.org/ko/download/)
2. 코드 에디터 (VSCode, Atom, WebStorm, Sublime 등..)

(+. [Yarn](https://classic.yarnpkg.com/en/docs/install#windows-stable) : `Yarn`은 조금 개선된 버전의 npm. [더 나은 속도, 더 나은 캐싱 시스템](https://www.keycdn.com/blog/npm-vs-yarn))

<br>

## npm 명령어
리액트 프로젝트 생성
```npm
npx create-react-app <project name>
```

라우터 규칙을 위한 npm 설치
```npm
npm i react-router-dom
```

리액트 시작
```npm
npm start
```

리액트 종료:  `ctrl + C`
```npm
>> 일괄 작업을 끝내시겠습니까 (Y/N)?
```
<br>
  
## CRA 구조
![image](https://user-images.githubusercontent.com/74305823/126419275-183bed58-1742-4214-9a22-0a630f537aeb.png)

<br>

## State와 Props
TBD...

<br>

## Life Cycle
![image](https://user-images.githubusercontent.com/74305823/126578543-9bee3b64-5ee3-417c-9e26-bdba1abfed03.png)
[**react-lifecycle-methods-diagram**](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

TBD...
