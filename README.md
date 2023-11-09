# vue를 이용한 포트폴리오 사이트 만들기
Vue는 자바스크립트 프레임워크로서, 사용자 인터페이스를 구축하기 위한 오픈 소스 프로젝트입니다. Vue.js는 웹 애플리케이션의 프론트엔드 개발에 주로 사용되며, 간단하고 가볍게 시작할 수 있는 구조를 가지고 있어 많은 웹 개발자들에게 인기가 있습니다. Vue는 MVVM (Model-View-ViewModel) 아키텍처를 기반으로 하고 있으며, 다른 프레임워크 및 라이브러리와 통합하기 쉽도록 설계되어 있습니다.

1. 선언적 렌더링: Vue는 HTML 템플릿을 사용하여 데이터와 DOM을 연결하고, 데이터의 변경이 자동으로 화면에 반영되도록 해줍니다. 이를 통해 UI 업데이트를 간단하게 처리할 수 있습니다.

2. 컴포넌트 기반: Vue는 컴포넌트 기반 아키텍처를 지원하며, 재사용 가능한 UI 요소를 생성하고 조합할 수 있습니다.

3. 반응형 데이터: Vue는 데이터와 뷰 간의 양방향 바인딩을 지원하며, 데이터 변경 시 자동으로 UI가 업데이트됩니다.

4. 디렉티브: Vue 디렉티브를 사용하여 DOM 요소에 특별한 동작을 부여할 수 있습니다. 예를 들어, v-for 디렉티브를 사용하여 반복 요소를 생성하거나, v-bind 디렉티브를 사용하여 속성을 동적으로 설정할 수 있습니다.

5. 상태 관리: Vue 애플리케이션에서 중앙 상태 관리를 위한 Vuex 라이브러리를 사용할 수 있습니다.

6. 라우팅: Vue 라우터를 사용하여 싱글 페이지 애플리케이션 (SPA)을 구현할 수 있습니다.

## 셋팅
`npm init vue@latest`<br>   
√ Project name: ... vue-project2023   
√ Add TypeScript? ... <span style="color: blue">No</span> / Yes   
√ Add JSX Support? ... No / <span style="color: blue">Yes</span>   
√ Add Vue Router for Single Page Application development? ... No / <span style="color: blue">Yes</span>           
√ Add Pinia for state management? ... <span style="color: blue">No</span> / Yes   
√ Add Vitest for Unit Testing? ... <span style="color: blue">No</span> / Yes   
√ Add an End-to-End Testing Solution? » <span style="color: blue">No</span>   
√ Add ESLint for code quality? ... No / <span style="color: blue">Yes</span>   
√ Add Prettier for code formatting? ... No / <span style="color: blue">Yes</span>   