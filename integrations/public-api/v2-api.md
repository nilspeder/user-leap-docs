# v2 API



{% api-method method="post" host="https://api.userleap.com" path="/v2/users" %}
{% api-method-summary %}
Create/Upsert user with attributes and events
{% endapi-method-summary %}

{% api-method-description %}
Creates a visitor with the specified \`userId\`. If a visitor already exists with that \`userId\`, the visitor's data will be updated with the provided data in the body.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API-Key &lt;API\_KEY&gt;
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="userId" type="string" required=true %}
Unique identifier for your reference. You can use this identifier to GET this visitor. This should also correspond to the userId you set with our SDKs
{% endapi-method-parameter %}

{% api-method-parameter name="events" type="array" required=false %}
An array of event objects. An event object has the following structure:  
{  
    event: String,  
    timestamp: unix timestamp \(milliseconds\)  
}
{% endapi-method-parameter %}

{% api-method-parameter name="attributes" type="object" required=false %}
{attributeName: attributeValue}. attributeValue must be a string, int, or bool
{% endapi-method-parameter %}

{% api-method-parameter name="emailAddress" type="string" required=false %}
Email address for this visitor. 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=202 %}
{% api-method-response-example-description %}
This request will be processed asynchronously.  
Making a GET request immediately after may result in a 404.  
Making another POST request immediately after with the same \`userId\` is supported.
{% endapi-method-response-example-description %}

```
Accepted
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.userleap.com" path="/v2/users/:userId" %}
{% api-method-summary %}
Get events and attributes of a visitor
{% endapi-method-summary %}

{% api-method-description %}
Fetch all events and attributes associated with a given visitor
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API-Key &lt;API\_KEY&gt;
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="userId" type="string" required=true %}
The unique identifier you have set for the visitor with the POST request above or by calling \`setUserId\` with our SDKs
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "id": "a926111b-fa62-49f7-8666-2c94ca8b18fc",
    "createdAt": 1612739790947,
    "attributes": {
        "plan": "enterprise",
        "completed_flow": false
    },
    "events": [
        {
            "event": "Clicked Signup",
            "count": 1,
            "createdAt": 1612739790947,//first instance of event
            "updatedAt": 1612739912314//most recent instance of event
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
You may receive a 404 if you request this resource right after creating it
{% endapi-method-response-example-description %}

```
Not Found
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

