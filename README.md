# v
<div id="app">
        <input v-model="message">
        <p>{{1+1}}</p>
        <p>메시지: {{ message.length >= 10 ? '10글자 이상' : '10글자 미만'}}</p> <!-- 표현식 작성이 가능-->
        <!-- {{var a = message}} 식이 아니라 문장입력은 안됨 -->
        <!-- https://kr.vuejs.org/v2/style-guide/index.html#%ED%85%9C%ED%94%8C%EB%A6%BF%EC%97%90%EC%84%9C-%EB%8B%A8%EC%88%9C%ED%95%9C-%ED%91%9C%ED%98%84%EC%8B%9D-%EB%A7%A4%EC%9A%B0-%EC%B6%94%EC%B2%9C%ED%95%A8 -->
    </div>
