---
description: api about chatting room and chats
---

# Chat API

{% api-method method="get" host="https://api.cakes.com" path="/room" %}
{% api-method-summary %}
Get All Rooms Info
{% endapi-method-summary %}

{% api-method-description %}
get all rooms\(authentication + user.pro required\).
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
"message":"Successfully get rooms",
"rooms":[
    {
        "chats":[
        "5f8b05d7ef815827cd5a886e",
        "5f8b05f6ef815827cd5a8870",
        "5f8b062526c7f028dc8f30d9",
        "5f8b063326c7f028dc8f30da"
        ],
        "_id":"5f8a9cf4e1b24b1d5f27cb94",
        "user":"5f87117a283e1938131fef3d",
        "createdAt":"2020-10-17T07:27:48.019Z",
        "__v":4
    },
    {
        "chats":[],
        "_id":"5f8a9de4e1b24b1d5f27cb95",
        "user":"5f87117a283e1938131fef3d",
        "createdAt":"2020-10-17T07:31:48.500Z",
        "__v":0
    }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Error .
{% endapi-method-response-example-description %}

```
{    "error": "~~~err"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.cakes.com" path="/room" %}
{% api-method-summary %}
Add Room
{% endapi-method-summary %}

{% api-method-description %}
Add One Room\(authentication required\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
New Room successfully created
{% endapi-method-response-example-description %}

```
{
    "message":"new Room Created",
    "newRoom":
        {
            "chats":[],
            "_id":"5f8d76ee13f71e1795627a3d",
            "user":"5f8b978a565a8110752bcb98",
            "createdAt":"2020-10-19T11:22:22.053Z",
            "__v":0
        }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Error 발
{% endapi-method-response-example-description %}

```
{
    "error" : "~~~reason"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/room/:id" %}
{% api-method-summary %}
Get One Room
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Room.\_id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully get room
{% endapi-method-response-example-description %}

```
{
"room":{
    "chats":
    [
        "5f8b05d7ef815827cd5a886e",
        "5f8b05f6ef815827cd5a8870",
        "5f8b062526c7f028dc8f30d9",
        "5f8b063326c7f028dc8f30da"
    ],
    "_id":"5f8a9cf4e1b24b1d5f27cb94",
    "user":"5f87117a283e1938131fef3d",
    "createdAt":"2020-10-17T07:27:48.019Z",
    "__v":4
    }
}

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Not Available id or etc
{% endapi-method-response-example-description %}

```
{
    "error" : "~~~reason"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="" path="/room/:id/chat/" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Room.\_id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="chat" type="string" required=false %}
한번의 채팅 내
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Successfully add chat
{% endapi-method-response-example-description %}

```
{
    "chat":
        {
            "_id":"5f8d7d390d450124f782ffe0",
            "user":"5f8b978a565a8110752bcb98",
            "chat":"이것도 마찬가지고",
            "createdAt":"2020-10-19T11:49:13.379Z",
            "__v":0
        }
}
    
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
 Not Available id or etc
{% endapi-method-response-example-description %}

```
{
    "error" : "~~~reason"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/room/:id/chat/:chatId" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="chatId" type="string" required=false %}
Chat.\_id
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=false %}
Room.\_id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "chat":
        {
            "_id":"5f8d80cab253f82b2247169a",
            "user":"5f8b978a565a8110752bcb98",
            "chat":"이것도 마찬가지고",
            "createdAt":"2020-10-19T12:04:26.649Z",
            "__v":0
        }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Chat and Room Do not match
{% endapi-method-response-example-description %}

```
{
 message: "wrong room and chat"
 }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

