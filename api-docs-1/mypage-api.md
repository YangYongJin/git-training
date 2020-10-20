---
description: get user information
---

# Mypage API

{% api-method method="get" host="https://api.cakes.com" path="/mypage" %}
{% api-method-summary %}
Get User Info
{% endapi-method-summary %}

{% api-method-description %}
get user Info\(needs Authentication\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User Info successfully retrieved.
{% endapi-method-response-example-description %}

```
{   
    "username": "dyyjkd",    
    "realname": "양용진", 
    "unit": "공군 15비", 
    "pro": "false"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message" : "Auth Failed"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="" path="/mypage/edit" %}
{% api-method-summary %}
Edit User Info
{% endapi-method-summary %}

{% api-method-description %}
edit user info\(needs Authentication\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="unit" type="string" required=false %}
소속 부대
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{   
    "unit": "udt 특공"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

