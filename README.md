# Vuejs
# Vuejs란?
-	대화형 웹 인터페이스를 개발하는데 사용하는 JavaScript 프레임워크
-	MVVM(Model – View – ViewModel) 패턴을 기반으로 디자인 되어 있다.

# MVVM
-	Model – View – Viewmodel
-	MVC에서 컨트롤러가 ViewModel로 변경된 개념
-	ViewModel은 View가 필요로 하는 데이터와 액션을 담고 있는 컨테이너 개념

# Vuejs 특징
-	AngularJS, Backbone, React에 비해 매우 작고 가볍다.
-	View에 초점을 맞춰 만들어진 프레임워크
(Javascript framework가 서버의 데이터를 Ajax통신으로 데이터를 가져와서 데이터를 처리해서 화면을 구성한다. 서버의 작업을 최소화 시켜서 서버의 부담감을 줄인다. Vuejs도 마찬가지로 동작된다. 눈에 보이는 UI요소에 포커스 하여 만들어졌다.)
-	가상 DOM을 사용한다.
(vueJS가 가지고 있는 라이브러리를 통해서 HTML을 만들어준다.)
-	데이터 바인딩
(세팅되어 있는 데이터를 원하는 HTML 구성요소에 세팅할 수 있다.)
-	컴포넌트
(컴포넌트를 이용하여 HTML을 재사용할 수 있다.
-	이벤트 핸들링
(v-on을 이용해서 이벤트 등에 관련된 여러가지 처리를 할 수 있다.)
-	애니메이션 및 효과
-	라우팅 등
# 본 강좌에서 사용하는 개발도구
-	Java 최신버전
-	Eclipse 최신버전
-	Apache tomcat 최신버전
-	Oracle 11g
-	크롬 최신 버전

# 지원 브라우저
-	ES5 이상을 지원하는 모든 브라우저를 지원한다.

# 개발방식
-	Vue Devtools
-	CDN
-	NPM
-	CLI

# Vue 생성
-	npm install –g npm
-	npm install –g @vue/cli
-	vue create hellovue
-	vue add router
-	vue add vuex

-	{{}} Mustache Expression(콧수염 표현식): 문자열 보간(interpolation)법으로 브라우저가 HTML을 렌더링할 때 Vue의 모델이라는 것을 알려주어서 반영시키는 선언적인 템플릿 표현식이다. 브라우저가 {{}}을 만나면 그 안의 내용을 모델(데이터) 객체의 속성 값을 반영해서 결과화면으로 보인다. {{}}은 모델(데이터)을 HTML이 아닌 일반 텍스트로 해석한다.

# View Model
-	View Model은 Model과 View 사이에서 관찰자 및 중재자 역할을 한다. MVC의 Controller가 MVVM에서는 View Model의 역할을 한다. 프론트엔드는 여러 레이어간의 화면 흐름과 데이터 흐름을 제어하는 것이 아니라 화면 단만의 데이터(모델) 변화를 화면(View)에 반영시키는 것이다.
-	Vue 객체 = View Model

# Vue 객체의 라이프 사이클
-	각 상황에 필요한 처리가 있으면 Vue 라이프사이클에 관련된 함수로 처리할 수 있다.

 
el 속성을 이용해서 어떠한 tag를 관리할 지를 지정해줄 수 있다.
Var vm1 = new Vue({
	// el: ‘#test1’
})
vm1.$mount(‘#test1’)
Vue 객체에 태그를 할당한다. 이렇게 mount 함수를 이용해서도 el처럼 관리할 태그를 지정해줄 수 있다.
vm1.$destroy()
Vue 객체에 마운트 된 태그를 관리하는 요소를 소멸시킨다. Destroy 함수는 객체 자체가 소멸되는 것은 아니고 서로 간에 값을 주고 받을 수 있는 요소를 소멸시키는 것이다.

# Template
-	v-html: 지정된 데이터를 html 코드로 인식하여 바인딩한다.
-	v-bind:속성명: 지정된 데이터를 지정된 속성 값으로 설정한다.
