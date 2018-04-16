# Essentials
링크 : [Vue.js](https://kr.vuejs.org/v2/guide/components.html)

## 목차
> 1. Vue 인스턴스
> 2. 템플릿 문법
> 3. 계산된 속성과 감시자
> 4. 클래스와 스타일 바인딩
> 5. 조건부 렌더링
> 6. 리스트 렌더링
> 7. 이벤트 핸들링
> 8. 폼 입력 바인딩
> 9. 컴포넌트

### 1. Vue 인스턴스 - The Vue Instance
모든 Vue는 **Vue** 함수로 새 인스턴스를 만드는걸로 시작 한다.

#### 인스턴스란?
> - 인스턴스는 객체를 생성하기 위해 만들어진 또 다른 객체를 인스턴스라고 부른다.
> - 인스턴스를 만들기 위해선 객체지향에서 말하는 클래스가 필요하다.
> - **클래스**는 객체지향언어에서 가장 중요한 부분 중 하나이며 다른 객체를 만드는 틀이라고 생각하면 된다.
> - 자바스크립트도 객체지향언어지만 클래스가 아닌 프로토타입 방식의 개체지향언어이다.
> - 만드는건 다르지만 인스턴스를 만든다는 것은 동일.

#### Vue 인스턴스 생성자
아래와 같이 Vue 생성자를 만든다.
```
// vm은 ViewModel의 약자
var vm = new Vue({
	// 옵션
})
```
Vue 객체를 생성할 때 아래와 같이 data, template, el, methods, life cycle callback등의 options를 포함 할 수 있다.
```
var vm = new Vue({
  template: ...,
  el: ...,
  methods: {

  },
  // ...
})
```
각 옵션으로 미리정의한 Vue객체는 확장 후 재사용이 가능하다.

#### Vue 인스턴스 라이프싸이클 초기화
Vue 객체가 생성될 때 초기화 작업을 수행할 수 있다.
> - 데이터 관찰
> - 템프릿 컴파일
> - DOM 에 객체 연결
> - 데이터 변경 시 DOM 업데이트
```
var vm = new Vue({
  data: {
    a: 1
  },
  created: function () {
    // this 는 vm 을 가리킴
    console.log('a is: ' + this.a)
  }
})
```

#### 상속
> - 객체지향에서 가장 중요한 상속이다. 

### 2. 템플릿 문법 - Template Syntax

#### 보간법(Interpolation)
**문자열**
```
<span>메시지: {{ msg }}</span>
```
> -  바인딩의 가장 기본 형태는 Mustache({{ }})를 사용한 텍스트 보간

**원시 HTML**
```
<div v-html="msg"></div>
```
> - 컨텐츠는 일반 HTML 형식으로 삽입

**속성
```
<img v-bind:src="image.jpg" /> 
<img :src="image.jpg" /> 
//v-bind생략가능
```
> - HTML 내부의 값을 데이터로 하고 싶을때
> - Mustaches는 HTML 속성으로 사용 불가 => v-bind 사용

**Javascript 표현식
```
{{ number + 2 }} 
{{ ok ? 'YES' : 'NO }} 
<div v-bind:id="'list-+' + id></div>
```
> - Vue.js는 모든 데이터 바인딩 내에서 Javascript표현식의 모든 기능 사용 가능
> - 이때는 변순 선언 또는 조건문 사용 불가능



### 3. 계산된 속성과 감시자 - Computed Properties and Watchers

### 4. 클래스와 스타일 바인딩 - Class and Style Bindings

### 5. 조건부 렌더링 - Conditional Rendering

### 6. 리스트 렌더링 - List Rendering

### 7. 이벤트 핸들링 - Event Handling

### 8. 폼 입력 바인딩 - Form Input Bindings

### 9. 컴포넌트 - Components Basics
