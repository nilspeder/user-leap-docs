# Themes

{% api-method method="get" host="https://api.userleap.com" path="/v1/themes" %}
{% api-method-summary %}
Get Themes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API key base authorization, format as `Bearer YOUR_KEY`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start" type="integer" required=false %}
The earliest creation data for a generated theme to return, represented as milliseconds from epoch time
{% endapi-method-parameter %}

{% api-method-parameter name="end" type="integer" required=false %}
The latest creation date for a generated theme to return, represented as milleseconds from epoch time
{% endapi-method-parameter %}

{% api-method-parameter name="cursor" type="string" %}
A Base64 encoded string representing an opaque cursor position
{% endapi-method-parameter %}

{% api-method-parameter name="sid" type="integer" %}
An integer id for a specific Survey
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Themes successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "cursor": "Y3JlYXRlZEF0OjE1ODA5MzAyNzg2OTY=",
  "data": [
      {
          "visitorId": 19720642,
          "surveyId": 227,
          "questionId": 369,
          "questionType": "OPEN",
          "updatedAt": "2020-02-21T23:33:23.248Z",
          "createdAt": "2020-02-21T23:33:23.248Z",
          "responseGroupUid": "8f41fd42-a034-49b6-8a7f-8a231fd6b49a",
          "response": "A more robust data export api",
          "questionText": "What would make UserLeap more valuable for you?",
          "theme": "Easy data export"
      },
      {
          "visitorId": 33094801,
          "surveyId": 154,
          "questionId": 226,
          "questionType": "OPEN",
          "updatedAt": "2020-10-28T21:37:31.028Z",
          "createdAt": "2020-10-28T21:37:31.028Z",
          "responseGroupUid": "18e38583-d6b6-4629-b2ce-c51072308f98",
          "response": "Something something cheeseburgers",
          "questionText": "What would make UserLeap more valuable for you?",
          "theme": "I wish they had food"
      }
    ]
 {
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
If one or more of your query parameters are not valid, an array of validation messages will be returned
{% endapi-method-response-example-description %}

```
[
    "\"start\" must be a valid date"
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
You may have an invalid API key and you should check your authorization header. There is no message with this status code.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find themes matching this query.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=429 %}
{% api-method-response-example-description %}
Your application has made too many requests in too short a time.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



