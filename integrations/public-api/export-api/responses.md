# Responses

{% api-method method="get" host="https://api.userleap.com" path="/v1/responses" %}
{% api-method-summary %}
Get Responses
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to retrieve up to 1000 responses at a time.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API key based authorization, format as `Bearer YOUR_KEY`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="cursor" type="string" required=false %}
A Base64 encoded string, used for pagination, that represents an opaque cursor position. Will return a `null` value if there are no additional responses
{% endapi-method-parameter %}

{% api-method-parameter name="sid" type="integer" required=false %}
An integer id for a specific Survey
{% endapi-method-parameter %}

{% api-method-parameter name="start" type="integer" %}
The earliest creation date for a survey response to return, represented as milliseconds from epoch time
{% endapi-method-parameter %}

{% api-method-parameter name="end" type="integer" %}
The latest creation date for a survey response to return, represented as milliseconds from epoch time
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Responses successfully retrieved
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
          "externalUserId": "35c52a35-2f59-4d2f-946c-36d19137a95a",
          "responseGroupUid": "8f41fd42-a034-49b6-8a7f-8a231fd6b49a",
          "response": "A more robust data export api",
          "questionText": "What would make UserLeap more valuable for you?"
      },
      {
          "visitorId": 33094801,
          "surveyId": 154,
          "questionId": 226,
          "questionType": "OPEN",
          "updatedAt": "2020-10-28T21:37:31.028Z",
          "createdAt": "2020-10-28T21:37:31.028Z",
          "externalUserId": null,
          "responseGroupUid": "18e38583-d6b6-4629-b2ce-c51072308f98",
          "response": "Something something cheeseburgers",
          "questionText": "What would make UserLeap more valuable for you?"
      }
    ]
}
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
Could not find responses matching this query.
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

