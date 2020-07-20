<h1>{{}}, v-text, v-html</h1>

    <div id="app">
        <input v-model="message">
        <p>{{message}}</p>
        <p>{{1+1}}</p>
        <p>{{ message.length >= 10 ? '10글자 이상' : '10글자 미만'}}</p>
        <p>{{var a = message}}</p>                                                         
    </div>
<br>

    var app = new Vue({
        el: '#app',
        data:{
            message: 'asd'
        } 

    })

- 스크립트 표현식이 가능하지만 문장을 입력하면 오류 발생.
- 표현식이 길 경우 methods나 computed 속성을 사용.
- https://kr.vuejs.org/v2/style-guide/index.html#%ED%85%9C%ED%94%8C%EB%A6%BF%EC%97%90%EC%84%9C-%EB%8B%A8%EC%88%9C%ED%95%9C-%ED%91%9C%ED%98%84%EC%8B%9D-%EB%A7%A4%EC%9A%B0-%EC%B6%94%EC%B2%9C%ED%95%A8

<hr>
<h1>v-for</h1>

    <div id="app">
        <span v-for="item in text">{{item}}</span>
    </div>
<br>

    var app = new Vue({
        el : '#app',
        data : {   
        text: 'Hello World!'
        },
    });
    
<br>
    
    <span>h</span>
    <span>e</span>
    <span>l</span>
    <span>l</span>
    <span>o</span>
    <span> </span>
    <span>w</span>
    <span>o</span>
    <span>r</span>
    <span>l</span>
    <span>d</span>
    <span>!</span>

- 문자열에 v-for를 사용하면 문자가 하나씩 렌더링 된다.
<hr>


<h1>v-for v-if</h1>

    <div id="app">
        <ul>
            <li v-for="user in users" v-if="user.isActive" :key="user.id">
              {{ user.name }}
            </li>
        </ul>
    </div>
<br>

    var app = new Vue({
        el: '#app',
        data: {
            users:[
                {id: 'p1234', name:'홍길동1', isActive: 'true'},
                {id: 'pppps', name:'홍길동2', isActive: 'false'},
                {id: 'sssss', name:'홍길동3', isActive: 'false'}
            ],
        }
    })
    
- v-for가 v-if 보다 먼저 렌더링 되기 때문에 v-for가 사용된 엘리먼트에 되도록 v-if를 사용하면 안된다.
- https://kr.vuejs.org/v2/style-guide/index.html#v-if%EC%99%80-v-for%EB%A5%BC-%EB%8F%99%EC%8B%9C%EC%97%90-%EC%82%AC%EC%9A%A9%ED%95%98%EC%A7%80-%EB%A7%88%EC%84%B8%EC%9A%94-%ED%95%84%EC%88%98
    
    
<hr>
<h1> v-on:submit.prevent / v-on:click.once / v-on:keyup.enter </h1>
<h1> v-model.trim / v-model.lazy </h1>

    <div id="app">
      <form v-on:submit.prevent="onSubmit"><!-- 새로고침 방지 -->
        <input type="text"><button>button</button> 
      </form>
        <p v-on:click.once="doThis">doThis</p>
        <input v-on:keyup.enter="submit"><button>button</button>
        <br>
        <input v-model.trim="data_1">
        <p>{{data_1}}</p>
        <input v-model.lazy="data_2">
        <p>{{data_2}}</p>
    </div>
    

<br>

    var app = new Vue({
        el: '#app',
        data: {
          data_1 : "",
          data_2 : ""
        },
        methods:{
          onSubmit(){
            alert('enter');
          },
          doThis(){
            alert("v-on:click.once");
          },
          submit(){
            alert('v-on:keyup.enter');
          }
        }
    });

- v-one:submit.prevent - form 태그 사용시 발생하는 새로고침 방지한다.
- v-on:click.once - 한번만 실행한다.
- v-on:keyup.enter - 키 이벤트를 발생한다.
- v-model.trim - 좌우 공백 제거한다.
- v-model.lazy - input 태그에 포커스가 벗어나면 업데이트를 한다.
