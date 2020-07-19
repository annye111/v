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
https://kr.vuejs.org/v2/style-guide/index.html#%ED%85%9C%ED%94%8C%EB%A6%BF%EC%97%90%EC%84%9C-%EB%8B%A8%EC%88%9C%ED%95%9C-%ED%91%9C%ED%98%84%EC%8B%9D-%EB%A7%A4%EC%9A%B0-%EC%B6%94%EC%B2%9C%ED%95%A8

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
    
v-for가 사용된 엘리먼트에 절대 v-if를 사용하지 마세요.
v-for가 v-if 보다 먼저 렌더링 되기 때문<br>
https://kr.vuejs.org/v2/style-guide/index.html#v-if%EC%99%80-v-for%EB%A5%BC-%EB%8F%99%EC%8B%9C%EC%97%90-%EC%82%AC%EC%9A%A9%ED%95%98%EC%A7%80-%EB%A7%88%EC%84%B8%EC%9A%94-%ED%95%84%EC%88%98
    
    
<hr>
<h1>v-for key</h1>
v-for와 key값을 항상 사용해야된다
