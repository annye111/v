{{}}, v-text, v-html

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
v-for

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
    

    
