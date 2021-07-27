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
**React**는 사용자 인터페이스를 만드는 데 사용되는 오픈소스 자바스크립트 라이브러리로, 페이스북에서 개발했습니다. 싱글 페이지 애플리케이션이나 모바일 애플리케이션 개발에 사용될 수 있으며 리액트를 사용하는 회사로는 아래와 같은 곳들이 있습니다.

![](https://img.shields.io/badge/-Netflix-E50914?style=for-the-badge&logo=Netflix&logoColor=white)
![](https://img.shields.io/badge/-Discord-5865F2?style=for-the-badge&logo=Discord&logoColor=white)
![](https://img.shields.io/badge/-Reddit-FF4500?style=for-the-badge&logo=Reddit&logoColor=white)
![](https://img.shields.io/badge/-Amazon&nbsp;AWS-232F3E?style=for-the-badge&logo=Amazon-AWS&logoColor=white)
![](https://img.shields.io/badge/-Twitch-9146FF?style=for-the-badge&logo=Twitch&logoColor=white)
![](https://img.shields.io/badge/-Twitter-1DA1F2?style=for-the-badge&logo=Twitter&logoColor=white)
![](https://img.shields.io/badge/-Instagram-E4405F?style=for-the-badge&logo=Instagram&logoColor=white)
![](https://img.shields.io/badge/-Facebook-1877F2?style=for-the-badge&logo=Facebook&logoColor=white)
![](https://img.shields.io/badge/-Uber-000000?style=for-the-badge&logo=Uber&logoColor=white)
![](https://img.shields.io/badge/-WhatsApp-25D366?style=for-the-badge&logo=WhatsApp&logoColor=white)
![](https://img.shields.io/badge/-Airbnb-FF5A5F?style=for-the-badge&logo=Airbnb&logoColor=white)
![](https://img.shields.io/badge/-Dropbox-0061FF?style=for-the-badge&logo=Dropbox&logoColor=white)
![](https://img.shields.io/badge/-Yahoo!-6001D2?style=for-the-badge&logo=Yahoo!&logoColor=white)

<br>

### JavaScript 프레임워크 비교

<table>
  <thead>
    <th>Angular</th>
    <th>Vue</th>
    <th>React</th>
  </thead>
  <tbody>
    <tr>
      <td align="center"><img src="http://angular.kr/assets/images/logos/angular/angular.png" width="100"/></td>
      <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/f/f1/Vue.png" width="70"/></td>
      <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/800px-React-icon.svg.png" width="130"/></td>
    </tr>
    <tr>
      <td align="center"><a href="https://angular.io/"/>angular.io</td>
      <td align="center"><a href="https://reactjs.org/"/>reactjs.org</td>
      <td align="center"><a href="https://vuejs.org/"/>vuejs.org</td>
    </tr>
    <tr>
      <td align="center">Google 개발 (2010년)</td>
      <td align="center">전 Google 직원 Evan You 개발 (2014년)</td>
      <td align="center">Facebook 개발 (2013년)</td>
    </tr>
    <tr>
      <td>Angular는 app 개발에 필요한 모든 것을 제공하기 때문에 러닝커브가 상당히 높습니다. TypeScript, MVC 외에도 Angular 내부의 동작 매커니즘과 제공 기술들도 알아야 합니다.</td>
      <td>Angular와 React보다 상대적으로 배우기 쉽고, 두 프레임워크로부터 Vue로 변경이 쉬운 편입니다. 하지만 Vue의 단순성과 유연성은 잘못된 코드를 허용하여 디버그 및 테스트를 어렵게 만들 수도 있습니다. </td>
      <td>가이드 문서가 상당히 잘 되어 있으며, 대부분의 문제도 Stackoverflow에 올라와 있습니다. Angular와 달리 완전한 프레임워크가 아니라서 추가 기능들에 대해 third-party 라이브러리가 필요합니다.</td>
    </tr>
  </tbody>
</table>

<br>

### React가 인기있는 이유?

- **다른 대안보다 덜 복잡하다**: React가 발표되었을 당시, 프레임워크로는 `Ember.js`와 `Angualr 1.x`가 주를 이루었습니다. 하지만 이 두 가지 모두 코드에 너무 많은 규칙을 적용했기 때문에 기존 앱을 이식하는 것이 전혀 편리하지 않았습니다. <br> <br> React는 기존 프로젝트에 매우 쉽게 통합되도록 했습니다. 이미 존재하는 코드베이스에 이를 도입하기 위해서는 Facebook에서 그렇게 해야만 했기 때문입니다. 또한, 두 프레임워크는 너무 많은 것을 테이블에 제공했지만, React는 전체 MVC 스택 대신 View 계층만 구현하기로 선택했습니다.

- **완벽한 타이밍**: 당시 Google은 `Angular 2.x`를 이전 버전과의 비호환성 및 주요 변경사항과 함께 발표했습니다. 하지만 Angular 1에서 2로 이동하는 것은 다른 프레임워크로 이동하는 것과 같았습니다. 따라서 React가 약속한 실행 속도 향상과 함께 개발자가 시도하고 싶어하는 것이 되었습니다.

- **페이스북의 지원과 리소스**: React는 페이스북 앱과 웹사이트, 그리고 인스타그램에서 많이 사용되고 있습니다. 페이스북은 그들의 생산 환경에서 5만여 개가 넘는 React Component를 사용합니다. 또한 React팀은 각 릴리즈에 대한 세부 정보를 지속적으로 제공하는 블로그를 운영중입니다. <br> <br> 페이스북은 React에 변경사항이 발생할 때마다 변경을 자동화하는 [**Codemod**](https://github.com/reactjs/react-codemod)를 제공하고 있습니다. Codemod란 코드베이스의 변경을 자동화하는 command-line 도구로, React에 변화가 생겼을 때 이전 구성 요소를 새로운 사양으로 자동 대체합니다.

<br>

### React 특징

- **선언형(Declarative)**:  React는 선언형 성격에 맞게 컴포넌트(원하는 결과, 뷰)를 얻기 위해 `<tag></tag>` jsx 문법을 통해 구현합니다. 즉, jsx를 얻기 위한 알고리즘에 대한 구현은 하지 않습니다. <br> <br> 이와 같은 선언형 특성은, 리액트를 사용할 때 화면 설계라는 초점에 맞춰서 개발할 수 있도록 해주므로, 다른 부분에 대한 고민을 최소화하고 높은 생산성을 보장할 수 있도록 해줍니다.

- **Component 기반**:  Component는 독립적인 단위의 소프트웨어 모듈을 말합니다. 즉 소프트웨어를 독립적인 하나의 부품으로 만드는 방법을 말하는데요. 리액트는 웹에서 쓰는 각 요소들을 컴포넌트로 만들 수 있게 해 기존의 UI를 다른 화면에서 다시 쓰거나, 다른 프로젝트에서 다시 쓸 수 있도록 하는 장점(높은 재사용성)을 가집니다.

- **Virtual DOM**: DOM(Document Object Model, 문서 객체 모델)은 HTML, XML 문서의 프로그래밍 인터페이스입니다. DOM 자체는 빠르지만 요소의 개수가 늘어날수록 CSS 재연산, 레이아웃 구성, 페이지 리페인트의 과정이 반복되면서 성능상 이슈가 발생하게 됩니다. Virtual DOM은 실제 DOM에 접근하여 조작하는 대신에, 이를 추상화시킨 자바스크립트 객체를 구성하여 사용합니다. <br> <br> React는 메모리 내에 데이터 구조 캐시를 만들고 결과 차이를 계산한 다음, 브라우저에 표시된 DOM을 효율적으로 업데이트하는데, 이 과정을 [재조정](https://ko.reactjs.org/docs/reconciliation.html)(Reconciliation)이라고 합니다. 이를 통해 React 라이브러리는 실제 변경되는 하위 구성요소만 렌더링하게 되고, 성능은 크게 향상됩니다.

<br>

***

## 개발 준비

- node.js [설치](https://nodejs.org/ko/download/)
- 코드 에디터 _(VSCode, Atom, WebStorm, Sublime 등..)_
- [선택사항] Yarn [설치](https://classic.yarnpkg.com/en/docs/install#windows-stable) &nbsp; `Yarn은 조금 개선된 버전의 npm입니다.`  
  <br>  
  > [npm vs Yarn - 어떤 패키지 관리자를 써야 할까?](https://www.keycdn.com/blog/npm-vs-yarn) 

<br>

## 명령어
- 프로젝트 생성
  ```npm
  npx create-react-app <project name>
  ```

- 리액트 실행
  ```npm
  npm start
  ```

- 리액트 종료:  `ctrl + C`
  ```npm
  >> 일괄 작업을 끝내시겠습니까 (Y/N)?
  ```
<br>
  
## CRA 구조
![image](https://user-images.githubusercontent.com/74305823/126419275-183bed58-1742-4214-9a22-0a630f537aeb.png)

<details open>
  <summary><b>public</b>: Virtual DOM이 들어갈 빈 html이 존재 </summary>

  &nbsp;&nbsp;&nbsp; - **favicon.ico**: 페이지 아이콘 이미지 파일  
  &nbsp;&nbsp;&nbsp; - **index.html**: 가상 DOM이 들어가기 위한 빈 html  
  &nbsp;&nbsp;&nbsp; - **manifest.json**: 웹 앱을 다운로드하고 네이티브 앱과 유사하게 사용자에게 제공하는 데 필요한 정보가 담긴 JSON 파일 
</details>
  
<details open>
  <summary><b>src</b>: 리액트 개발이 이루어지는 메인 폴더 </summary>

  &nbsp;&nbsp;&nbsp; - **index.js**  
  ```javascript
  import React from 'react';
  import ReactDOM from 'react-dom';
  import './index.css';
  import App from './App';
  import registerServiceWorker from './registerServiceWorker';
  
  ReactDOM.render(<App />, document.getElementById('root'));
  registerServiceWorker();
  ```
  
  &nbsp;&nbsp;&nbsp; - **App.js**
  ```javascript
  import logo from './logo.svg';
  import './App.css';

  function App() {
    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <p>
            Edit <code>src/App.js</code> and save to reload.
          </p>
          <a
            className="App-link"
            href="https://reactjs.org"
            target="_blank"
            rel="noopener noreferrer"
          >
            Learn React
          </a>
        </header>
      </div>
    );
  }

  export default App;
  ```
</details>

<br>

## State와 Props
TBD...

<br>

## Life Cycle
![image](https://user-images.githubusercontent.com/74305823/126578543-9bee3b64-5ee3-417c-9e26-bdba1abfed03.png)
[**react-lifecycle-methods-diagram**](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

TBD...

<br />

### References

:bookmark_tabs: [reactjs.org](https://reactjs.org/)  
:bookmark_tabs: [Web app manifests](https://developer.mozilla.org/en-US/docs/Web/Manifest)  
:bookmark_tabs: [The React Handbook](https://www.freecodecamp.org/news/the-react-handbook-b71c27b0a795/)  
:bookmark_tabs: [Why You Should Use React.js For Web Development](https://www.freecodecamp.org/news/why-use-react-for-web-development/)  
:bookmark_tabs: [Angular vs React vs Vue: Which Framework to Choose in 2021](https://www.codeinwp.com/blog/angular-vs-vue-vs-react/)
 
