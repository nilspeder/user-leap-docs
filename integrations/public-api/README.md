# Public API

The UserLeap Public API is organized around [**REST**](http://en.wikipedia.org/wiki/Representational_State_Transfer). Our API has predictable resource-oriented URLs, accepts [**JSON-encoded**](http://www.json.org/) ****request bodies, returns [**JSON-encoded**](http://www.json.org/) responses, and uses standard HTTP response codes, authentication, and verbs.

UserLeap offers API access to both your[ **Production and Development environments**](). You can use your Development environment to validate your usage of the UserLeap API before interacting with your live data. The API key you use to authenticate the request determines whether the request is against Production data or Development data. Team members with the Admin or Developer roles can see the API Keys.

This is an early version of the UserLeap Public API. We welcome your feedback and feature requests.

### **Locate Your API Keys**

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/p9ubQ0vO/642dc13f-6641-4d29-8b1d-8a054e7f0160.gif?v=ad570551d86dbb8320491998a51b71d0)

### Authentication

UserLeap uses API keys to authenticate requests to the Public API. Your API keys grant access to your data stored in UserLeap, so be sure to keep them secure! Do not share your API keys in publicly accessible areas such as GitHub or client-side code.

Authentication to the API is performed via the HTTP Authorization Header. Include this header on all requests to the API.

The header name is Authorization, and an example value is

```text
API-Key 8abaf7cb-fake-fake-fake-c608317728bd
```

Using the command line tool curl, you would use the following snippet to include the API key with a request.

```text
curl https://api.userleap.com/v1/users/1234567890 \
 -H "Authorization: API-Key 8abaf7cb-fake-fake-fake-c608317728bd"
```

HTTP clients in all programming languages allow for custom headers to be set. If you need assistance using the UserLeap API with a specific language, please let us know.

All API requests must be made over [HTTPS](http://en.wikipedia.org/wiki/HTTP_Secure). Calls made over plain HTTP will fail. API requests without authentication will also fail.

### **Users**

The User object defines a visitor in the UserLeap system that has registered on your site and their User Id has been provided by the SDK with the setUserIdentifier function. The API allows for you to read and update properties of individual users.

#### The user object

| Property | Type | Description |
| :--- | :--- | :--- |
| id | string | The ID of the user in your system |
| emailAddress | string | The Email Address of the user |
| attributes | map | A key-value map of custom attributes you can set on the user |

#### Example User Object

```javascript
{
  "userId": "1234567890",
  "emailAddress": "customer@email.com",
  "attributes": {
    "plan_type": "standard"
  }
}
```

#### Retrieve a user

Retrieves the details of an existing user. You need to provide the user Id of the user at the end of the URI.

```text
GET - https://api.userleap.com/v1/users/:userId
```

#### Create/Upsert a user

Typically, users are created via the JavaScript web snippet, or by a Mobile SDK. For workflows where surveys are not delivered via the web or mobile apps, we allow customers to create users via the Public API. For this use-case, customers typically send in an email address and/or userId.

Sets one or more properties on a new user to be created. The newly created user is returned back.

If an `id` is provided in the body and it matches an existing user, that user will be returned

```text
POST - https://api.userleap.com/v1/users
```

Example Creating a User and setting their email address and user id to your stored values:

```bash
curl https://api.userleap.com/v1/users \
 -X POST \
 -H "Authorization: API-Key 8abaf7cb-fake-fake-fake-c608317728bd" \
 -H "Content-Type: application/json" \
 -d "{\"emailAddress\": \"user@email.com\", \"id\": \"very_fake_id_123\"}"
```

#### Update a user

Sets one or more properties on an existing user. Any properties not included are left unchanged. New attributes are merged into the existing attributes map.

```text
POST - https://api.userleap.com/v1/users/:userId
```

Example Setting a User's email address:

```bash
curl https://api.userleap.com/v1/users/1234567890 \
 -X POST \
 -H "Authorization: API-Key 8abaf7cb-fake-fake-fake-c608317728bd" \
 -H "Content-Type: application/json" \
 -d "{\"emailAddress\": \"user@email.com\"}"
```

#### Create a User Event

User events are tracked from the web and mobile SDKs using the tracking methods there, however if you want to add events that are triggered from a background or backend process, here's how. 

Records an occurrence of a preconfigured event. Returns a 201 status code if successful, 404 if the event isn't configured.

```bash
POST - https://api.userleap.com/v1/users/:userId/events
```

Example Creating a Login event for a user with your own stored user id:

```bash
curl https://api.userleap.com/v1/users/1234567890/events \
 -X POST \
 -H "Authorization: API-Key 8abaf7cb-fake-fake-fake-c608317728bd" \
 -H "Content-Type: application/json" \
 -d "{\"name\": \"Login\", \"timestamp\": \"2020-04-30T23:05:38.687Z\"}"
```

The `timestamp` property is optional and is recorded as `now()` if no value is passed. Accepted values for timestamps are _millisecond_ representations of UNIX Epoch time and ISO standard datetime strings.

### Rate Limiting

We currently limit 1000 requests per 5 minute interval for a given API Key.

If you need a higher limit, please reach out to support@userleap.com

