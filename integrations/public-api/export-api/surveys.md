# Surveys

{% api-method method="get" host="https://api.userleap.com" path="/v1/surveys" %}
{% api-method-summary %}
Get Surveys
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you retrieve up to 1000 surveys at a time.
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
A Base64 encoded string representing an opaque cursor position
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="array" required=false %}
One or many of \(IN\_PROGRESS, PAUSED, COMPLETED, DRAFT, ARCHIVED, NEW\). Can be passed as `?status=PAUSED,COMPLETED`, `?status[]=PAUSED&status[]=COMPLETED` or `?status=PAUSED&status=COMPLETED`
{% endapi-method-parameter %}

{% api-method-parameter name="start" type="integer" %}
The earliest creation date for a survey to return, represented as milliseconds from epoch time
{% endapi-method-parameter %}

{% api-method-parameter name="end" type="integer" %}
The latest creation date for a survey to return, represented as milliseconds from epoch time
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully found one or more surveys.
{% endapi-method-response-example-description %}

```
{   
    "cursor": "Y3JlYXRlZEF0OjE1NTMyMDAxNTMwMTk=",
    "data": [
        {
            "id": 12,
            "name": "Understand Appeal",
            "status": "COMPLETED",
            "platform": "web",
            "type": "CONTINUOUS",
            "totalResponseLimit": null,
            "completedAt": "2019-06-12T19:23:35.522Z",
            "launchedAt": null,
            "createdAt": "2018-07-18T08:02:09.858Z",
            "updatedAt": "2019-06-12T19:23:35.522Z",
            "questions": [
                {
                    "id": 118,
                    "questionText": "How interested are you in using UserLeap?",
                    "routingOptions": null,
                    "type": "LIKERT",
                    "optionsProperties": {
                        "labels": {
                            "left": "Not at all interested",
                            "right": "Extremely interested"
                        },
                        "introText": "Thanks for using UserLeap. Tell us about your experience."
                    },
                    "options": []
                },
                {
                    "id": 105,
                    "questionText": "What aspect of UserLeap is most appealing?",
                    "routingOptions": null,
                    "type": "OPEN",
                    "optionsProperties": null,
                    "options": []
                }
            ],
            "constraints": [
                {
                    "type": "SESSION_COUNT",
                    "event": null,
                    "value": 1,
                    "comparisonType": "gte"
                },
                {
                    "type": "TIME_ON_PAGE_DELAY",
                    "event": null,
                    "value": 2,
                    "comparisonType": "eq"
                }
            ]
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
If one or more of your query parameters are not valid, an array of validation messages will be returned.
{% endapi-method-response-example-description %}

```
[
    "\"start\" must be a valid date"
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
You may have an invalid or API key and you should check your authorization header. There is no message with this status code.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find surveys matching this query.
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



