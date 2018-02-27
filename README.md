# Vue 기초 문법
링크 : [작업물](https://github.com/leeseungje/Vue/tree/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95)

# 1. v-text
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/1.v-text.html)
제일 기본 적인 디렉티브 엘리먼트에 v-text="name" 값을 넣어주고 script에 name 값을 컨트롤 할 수 있다.

# 2. v-html
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/2.v-html.html)
v-text와 같은 내용 이지만 text는 안에 앨리먼트를 넣으면 바로 표시가 되지만 이 디렉티브를 사용하면,
앨리먼트 효과를 먹는다.

# 3. v-show
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/3.v-show.html)
해당 태그에 v-show="show(아무거나 넣어도 된다.)" 라는 문법을 넣고 script data 안에 show : true OR false 를 넣으면,
true 일시 텍스트 노출, false 일시 텍스트 비노출 된다.

# 4. v-if
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/4.v-if.html)
조건문으로 값을 충족 시켯을 시 텍스트 노출하는 디텍티브 이다.

# 5. v-else
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/5%2Cv-else.html)
if문에서 충족 시키지 않았을 시 else문을 노출시키는 디렉티브 이다.

# 6. v-else-if
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/6.v-else-if.html)
if와 else의 중간 디렉티브 이다. 
중간에서 멈출때 사용 한다.

# 7. v-pre
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/7.v-pre.html)
1. v-text 와 비슷하지만 Vue.js의 {{ }} 이런 태그를 그대로 표현이 가능하다.

# 8. v-cloak
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/8.v-cloak.html)
최초 랜더링시 script 읽지 않을때 해당 디렉티브가 먼저 노출되는 부분이 있는데 이태그를 사용하면 load 후 노출된다.
하지만 style 에서 [v-cloak] 에 대한 display: none 을 추가 해야지 제대로 동작 한다.

# 9. v-once
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/9.v-once.html)
초기에 딱 한번 렌더링 하는 디렉티브 

# 10. v-bind
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/10.v-bind.html)
예를 들어 img 태그에 src 데이터 값을 넣고 싶다면, v-bind:src Or :src 값을 넣을 수 있다.
그리고 조건문을 사용하여 images 라는 값을 넣어 true를 넣어주면 첫번째값, false면 두번째값을 넣을 수 있다.

# 11. v-model
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/12.v-model.html)
지금 까지 배웠던건 **단 방향 데이터** 한쪽으로만 데이터가 흐르지만 v-model을 사용하면 **양 방향 데이터**,
페이지 로드 시 에도 데이터 값을 바꿔 줄 수 있다.

# 12. v-for
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/11.v-for.html)
배열 렌더링 디렉티브 즉 여러 리스트를 작성시 스크립트에서 배열로 저장하고 html에서 v-for을 이용해 저장된 배열값을 
뿌리는 방식

# 13. v-on
[링크](https://github.com/leeseungje/Vue/blob/master/%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95/13.v-on.html)
이벤트 처리 디텍티브로 v-on 또는 @를 사용 한다. **v-on: or @이벤트이름="메소드이름"**

# 객체

# 1. **Computed**
[[링크]](https://github.com/leeseungje/Vue/blob/master/%EA%B0%9D%EC%B2%B4/1.computed.html)
## 미리 계산된 객체
* Javascript 로 따지면 onload와 비슷 하다.
* Javascript 에선 함수 호출을 **example()** 이런식으로 호출하지만,
* Vue.js 에선 **{{ example }}** 이런식으로 호출 한다.
* Computed 에서는 app 안에 있는 data 값들을 실시간으로 바인딩 하고 있다.
* Vue는 app.result가 app.num1, app.num2에 의존하는 걸 알기 때문에 app.num1, app.num2 둘 중에 누가 바뀌어도 app.result에 의존하는 바인딩을 모두 업데이트 한다.
