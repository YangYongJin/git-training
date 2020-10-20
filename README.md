---
description: API Documentation about project Ask
---

# 사용 안내서

## API에 연동하는 

우선 개발서버를 활성화시켜야 한다. 이를 위해서 우선 서버를 작동시켜야한다.  

```
$ cd backend/
$ npm install
$ npm start
```

{% hint style="info" %}
작동 전 backend 폴더 내에 .env 파일을 만들어 다음과 같이 설정해 놓는다.
{% endhint %}

{% code title=".env" %}
```bash
PORT=4000
MONGO_URI=mongodb+srv://sample:sample123@cluster0.khztw.gcp.mongodb.net/blog?retryWrites=true&w=majority
JWT_SECRET=02750204a32b72079ee621b8bfdadf0b1ada419ee8a58ee93ca138629e0a5b6735d169a01402752ff0066de7507da840daca07d293f34bca8037ee1e92086892
```
{% endcode %}

서버를 돌아가게 만든 후에는 react의 경우 package.json의 "proxy"를 통해 api에 접근할 수 있다.  

{% code title="package.json" %}
```bash
"proxy": "http://localhost:4000"
```
{% endcode %}

proxy가 설정되면 \(axios  등을 이용하\) api를 가져올수 있다.

```bash
ex) /register => http://localhost:4000/register
```

