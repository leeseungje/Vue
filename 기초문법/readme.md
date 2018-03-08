
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
## 4.v-if.html
## 5,v-else.html
## 6.v-else-if.html
## 7.v-pre.html
## 8.v-cloak.html
## 9.v-once.html
## 10.v-bind.html
## 11.v-for.html
## 12.v-model.html
## 13.v-on.html
