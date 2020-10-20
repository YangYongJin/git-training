---
description: API lists for auth
---

# Auth API

{% api-method method="post" host="https://api.cakes.com" path="/register" %}
{% api-method-summary %}
Register
{% endapi-method-summary %}

{% api-method-description %}
signup for new user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
아이디\("ex: dyyjkd"\)
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
비밀번호
{% endapi-method-parameter %}

{% api-method-parameter name="realname" type="string" required=true %}
실명\("ex: 양용진"\)
{% endapi-method-parameter %}

{% api-method-parameter name="unit" type="string" required=true %}
소속부대\("ex: 공군 15비 보급대대 운영통제"\)
{% endapi-method-parameter %}

{% api-method-parameter name="pro" type="boolean" required=true %}
 전문상담관 여
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
User successfully registered.
{% endapi-method-response-example-description %}

```
{    "message": "Auth Successfully Created" }
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
register fail
{% endapi-method-response-example-description %}

```
{ "error" : "err" }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.cakes.com" path="/login" %}
{% api-method-summary %}
Login
{% endapi-method-summary %}

{% api-method-description %}
login api
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
아이디
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
비밀번호
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{ message: "Auth succesful" }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.cakes.com" path="/logout" %}
{% api-method-summary %}
Logout
{% endapi-method-summary %}

{% api-method-description %}
logout request
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
logout method
{% endapi-method-response-example-description %}

```
{ message: "Succesfully Logout" }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



