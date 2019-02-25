---
description: 注意：防止只对转换后得链接直接打开有效，在链接里面分享出去的是不受防封保护的!
---

# 添加防封域名配置

{% api-method method="get" host="http://houtai.qt27.cn/weixin/weixinNisDomains?userName=xxx&domains=xxx&type=1" path="" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
域名防封API接口配置说明，如请求原来 v1.com  返回 v2.com ，假设v1.com/xxx?a=1&b=2 需要防封，则将链接转换为: v2.com/xxx?a=1&b=2即可！
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="type" type="integer" required=false %}
请求类型 0=添加域名  1=删除指定域名的配置关联
{% endapi-method-parameter %}

{% api-method-parameter name="domains" type="string" required=false %}
需要防封的域名不带http eg: v1.cn
{% endapi-method-parameter %}

{% api-method-parameter name="userName" type="string" %}
 注册的手机号码/账号.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": 200,
    "msg": "结果描述", //返回200=添加/删除成功 201=添加已经达到上限  202=会员过期无法添加
    "domain" : "v2.com"  //返回可用的防封链接
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



