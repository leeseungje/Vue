
# Essential

## 1.v-text.html
기본적인 텍스트를 Javascript로 입력시키는 방식 
```
<div id="app"> 
  <h1>
    Hello
    <span v-text="name"></span>
  </h1>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      name: "Vue 입니다."
    }
  });
</script>
```

## 2.v-html.html
v-text는 텍스트 관련만 쓸 수 있다면 v-html은 html도 겸해서 쓸 수 있다.
```
<div id="app"> 
  <h1>
    Hello
    <span v-html="name"></span>
  </h1>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      name: "<i>Vue 입니다.</i>"
    }
  });
</script>
```

## 3.v-show.html
```
<div id="app"> 
  <h1>
    Hello
    <span v-show="show" v-html="name"></span>
  </h1>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      name: "<i>Vue 입니다.</i>",
      show: false
    }
  });
</script>
```

## 4.v-if.html
```
<div id="app"> 
  <h1 v-if="value > 10">value 가 10보다 크다</h1>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      value : 20
    }
  });
</script>
```

## 5,v-else.html
```
<div id="app"> 
  <h1 v-if="value > 10">value 가 10보다 크다</h1>
  <h1 v-else>value 가 10보다 작다</h1>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      value : 0
    }
  });
</script>
```

## 6.v-else-if.html
```
<div id="app"> 
  <h1 v-if="value > 10">value 가 10보다 크다</h1>
  <h1 v-else-if="value === 10">value 값이 10이다</h1>
  <h1 v-else>value 가 10보다 작다</h1>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      value : 10
    }
  });
</script>
```

## 7.v-pre.html
```
<div id="app"> 
  <h1 v-if="value > 10">value 가 10보다 크다</h1>
  <h1 v-else-if="value === 10">value 값이 10이다</h1>
  <h1 v-else>value 가 10보다 작다</h1>
  <h3 v-pre>{{ 엘리먼트가 모두가 보인다 }}</h3>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      value : 10
    }
  });
</script>
```

## 8.v-cloak.html
```
<div id="app" v-cloak> 
  <h1 v-if="value > 10">value 가 10보다 크다</h1>
  <h1 v-else-if="value === 10">value 값이 10이다</h1>
  <h1 v-else>value 가 10보다 작다</h1>
  <h3 v-pre>{{ 엘리먼트가 모두가 보인다 }}</h3>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      value : 10
    }
  });
</script>
```

## 9.v-once.html
```
<div id="app" v-cloak> 
  <h1 v-once v-if="value > 10">value 가 10보다 크다</h1>
  <h1 v-else-if="value === 10">value 값이 10이다</h1>
  <h1 v-else>value 가 10보다 작다</h1>
  <h2 v-once>초기값 : {{ value }}</h2>
  <h2>변경값 : {{ value }}</h2>
  <h3 v-pre>{{ 엘리먼트가 모두가 보인다 }}</h3>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      value : 0
    }
  });
</script>
```

## 10.v-bind.html
```
<div id="app" v-cloak>
  <h1>{{ name }}</h1>
  <h2>{{ Date() }} - 자바스크립트 입력도 가능</h2>
  <img :src="images ? image : another_image" :title="image_title">
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      name: "v-bind (생략 가능)",
      images: false,
      image: "http://i.imgur.com/XXTIDLh.gif",
      another_image: "http://postfiles2.naver.net/20140903_225/zzeuyoung_1409736850255aC7z8_GIF/daily_gifdump_680_06.gif?type=w1",
      image_title: "이미지 타이틀 입니다."
    }
  });
</script>
```

## 11.v-for.html
```
<div id="app" v-cloak> 
  <ul>
    <li v-for="(list, index) in todos">
      {{ index + 1 }} {{ list.text }}
    </li>
  </ul>

  <ul>
    <li v-for="list in todos">
      {{ list.text }}
    </li>
  </ul>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      todos: [
        { text : "입력문 1" },
        { text : "입력문 2" },
        { text : "입력문 3" },
        { text : "입력문 4" },
        { text : "입력문 5" },
        { text : "입력문 6" },
        { text : "입력문 7" }
      ]
    }
  });
</script>
```

## 12.v-model.html
```
<div id="app" v-cloak>
  <h1>Hello {{ name }}</h1>
  <input type="text" v-model="name">
  <h3><input type="checkbox" v-model="images">이미지 바뀌는 체크박스</h3>
  <img :src="images ? image : another_image">
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      name : "leeseungje",
      images : false,
      image: "http://i.imgur.com/XXTIDLh.gif",
      another_image: "http://postfiles2.naver.net/20140903_225/zzeuyoung_1409736850255aC7z8_GIF/daily_gifdump_680_06.gif?type=w1",
      image_title: "이미지 타이틀 입니다."
    }
  });
</script>
```

## 13.v-on.html
```
<div id="app" v-cloak>
  <h1 v-once>현재 값 : {{ number }}</h1>
  <h1>바뀌는 값 : {{ number }}</h1>
  <button @click="up">증가</button>
  <button @click="down">감소</button>
</div>
<script>
  var app = new Vue ({
    el: "#app",
    data: {
      number : 0
    },
    methods : {
      up : function() {
        this.number++;
      },
      down : function() {
        this.number--;
      }
    }
  });
</script>
```

