# Javascript SDK

## Installation for Web Applications

Below is the code to add for the base UserLeap installation. The snippet should be added to every page on your website so that UserLeap can properly track your visitors. This snippet can be pasted anywhere on the page, but [preferably at the bottom of the document](https://gtmetrix.com/put-javascript-at-bottom.html), before the `</body>` tag.

```javascript
<script type="text/javascript">
   (function(l,e,a,p) {
     if (window.UserLeap) return;
     window.UserLeap = function(){U._queue.push(arguments)}
     var U = window.UserLeap;U.appId = a;U._queue = [];
     a=l.createElement('script');
     a.async=1;a.src=e+'?id='+U.appId;
     p=l.getElementsByTagName('script')[0];
     p.parentNode.insertBefore(a, p);
   })(document, 'https://cdn.userleap.com/shim.js', 'YOUR_APP_ID');
 </script>
```

Replace YOUR\_APP\_ID with your Environment Id found on the UserLeap [**Connect**](https://app.userleap.com/connect) page

[UserLeap provides you with two environment IDs](). The development environment which can be used to test your installation and integration, and the production environment which should be used for your actual deployment. This allows you to test and verify your UserLeap configuration before enabling it on your live website.

## **Verifying your SDK Installation**

You can use the [People Section](https://app.userleap.com/visitors/all) to verify that your site is sending data to the UserLeap servers. When a user visits your site after you have installed the snippet, they will appear in this view, along with their email address, and if they are eligible to be shown a survey.

### In-Browser Testing

Normally with UserLeap, only users that match the specific targeting of a running survey will ever see the JavaScript snippet in action. This can make it challenging to test out how to survey will look for users on your site. 

In addition to the Live Preview in the UserLeap Dashboard, you can also manually view and test a Survey from within your site by running the command shown below in the browser developer console. It does require that you are running at least one survey in your environment.

{% hint style="warning" %}
The browser developer console isn't normally used during normal web browsing. These instructions may require assistance from a technical colleague.
{% endhint %}

### Instructions

Begin by opening the Javascript console:

{% tabs %}
{% tab title="Chrome" %}
Select **View** &gt; **Developer** &gt; **JavaScript Console**
{% endtab %}

{% tab title="Firefox" %}
Select **Tools** &gt; **Web Developer** &gt; **Web Console**
{% endtab %}

{% tab title="Internet Explorer" %}
Select **Tools** &gt; **Developer Tools** &gt; **Console**
{% endtab %}
{% endtabs %}

In the bottom row there will be an input field to execute JavaScript commands. Run the following command:

```javascript
UserLeap.displaySurvey(surveyId); //THIS IS FOR DEBUGGING ONLY
```

Replace `surveyId` with the id of one of your currently running surveys. You can see the `surveyId` by looking at the end of the URL when viewing the Survey Details in the Dashboard.

For example: `https://app.userleap.com/surveys/439` has a `surveyId` of 439

#### Example:

To view and test a survey with the Id of 100, you would use the following command:

```javascript
UserLeap.displaySurvey(100); //THIS IS FOR DEBUGGING ONLY
```

{% hint style="warning" %}
If you'd like to see a Survey without installing the JavaScript snippet, you can run the displaySurvey function from within the [UserLeap Dashboard](https://app.userleap.com) try it out.

`UserLeap.displaySurvey(118)`
{% endhint %}

## **User Identity**

UserLeap allows you to identify visitors by supplying a userId. While tracking userIds is optional,  it helps to provide a consistent experience across platforms and prevents users from seeing the same survey multiple times.

The user identifier should be unique and mappable to your internal user id in some way.

Set the userId after the installation snippet if they are already logged in or after the user logs in to your website:  


```javascript
<script>
    UserLeap('setUserId', '12345');
</script>
```

This user identifier is stored via cookies and this function can be called multiple times safely. We recommend you set the user identifier every time you initialize UserLeap and anytime your customers login to be safe.

You can also provide UserLeap with the user's email address. It is not required for Web and Mobile surveys, but is required to enable Email-based surveys.

```javascript
<script>
    UserLeap('setEmail', 'user@test.com');
</script>
```

## **Putting it all together**

Here is what the installation looks like on pages that track registered users:

```javascript
<script type="text/javascript">
   (function(l,e,a,p) {
     window.UserLeap = function(){U._queue.push(arguments)}
     var U = window.UserLeap;U.appId = a;U._queue = [];
     a=l.createElement('script');
     a.async=1;a.src=e+'?id='+U.appId;
     p=l.getElementsByTagName('script')[0];
     p.parentNode.insertBefore(a, p);
   })(document, 'https://cdn.userleap.com/shim.js', 'YOUR_APP_ID');
  
   // Increases tracking accuracy across devices
   UserLeap('setUserId', '12345');
  
   // Allows the user to receive email surveys
   UserLeap('setEmail', 'user@test.com');
 </script>
```

## User Attributes

UserLeap lets you build up user profiles to provide more context about the user in order to gain a better understanding of the feedback a user provides. The UserLeap system tracks a default set of attributes, but also allows you to specify custom attributes and values that are specific to your business.

The User Attributes can be used in survey targeting to help refine the cohort of users you wish to survey. They can also be used as filters to drill into the survey response data in the UserLeap Dashboard.

_**User Attributes are limited to 100 values**_

### Default Attributes

UserLeap's JavaScript snippet automatically tracks and attaches the following attributes:

* Browser and version
* Device
* Session count
* Page URL
* Screen size
* Browser Language
* Operating System and Version

### Custom Attributes

Optionally, you can send in custom attributes about the user. This information is visible on the People section of the UserLeap Dashboard when viewing a Visitor.

#### Values

* `attribute` {String} _required_ - the attribute name to set. Attributes beginning with ! are reserved
* `value` {Object} _required_ - the value to set for the specified attribute name \(typically a string or number, but anything convertible to JSON will work\)

```javascript
<script type="text/javascript">
    //for a single attribute
    UserLeap('setAttribute', attribute, value);
    
    //for multiple attributes
    //saves multiple rounds trips and reduces data usage
    UserLeap('setAttributes',{
        key1: value1,
        key2: value2
    });

    //if attributes no longer applies to the user
    //you can delete multiple at a time
    UserLeap('removeAttributes', [key1, key2]);
</script>
```

Some common attributes to set are

* Location
* Referral URL
* A/B test group

## UserLeap Update Notifications \(v1.9.0+\)

On SDK version 1.9.0 and above, UserLeap introduces several new SDK events and exposes a new way to listen to the updates. Here is a sample code block for listening to SDK events in real-time:

```javascript
// an example of a simple listener
const listener = function (e) {
    // does work with data
    console.log(e);
};
// to subscribe to UserLeap survey presented event
UserLeap('addListener', UserLeap.UPDATES.SURVEY_PRESENTED, listener);
// to remove a survey presented event listener
UserLeap('removeListener', UserLeap.UPDATES.SURVEY_PRESENTED, listener);
```

The following supported events are available on `UserLeap.UPDATES`:

| UPDATES Name | Data | SDK Version | Description |
| :--- | :--- | :--- | :--- |
| SURVEY\_HEIGHT | { name: 'survey.height', contentFrameHeight: int } | 1.9.0 | Trigger: on height changes. Data:  height in the event data. |
| SURVEY\_PRESENTED | { name: 'survey.presented' } | 1.9.0 | Trigger: on survey present |
| SURVEY\_CLOSED | { name: 'survey.closed' } | 1.9.0 | Trigger: on survey frame dismiss \(including submission and close\) |
| SURVEY\_LIFE\_CYCLE | { state: 'presented' } or { state: 'dismissed' } | deprecated | Trigger: on survey present and close. Data: lifecycle state type |

## **Logout**

When a user logs out of your webpage, make sure to log out of UserLeap. This will prevent new activity being associated with the wrong user.

```javascript
<script type="text/javascript">
    UserLeap.logoutUser();
</script>
```

## **Displaying Surveys**

UserLeap provides three methods to show a survey on your website

### **Option 1: Code Events**

Let’s track the event you created in [Setting up your first survey](../../product-workflows/launch-a-survey.md). You track events with UserLeap with the following:

```javascript
<script type="text/javascript">
    UserLeap('track', '[TEST] My first event');
</script>
```

A survey will be displayed after this call If the user is eligible to receive a survey. You can see the eligibility of a given user in the [People](https://app.userleap.com/visitors/all) page. 

Note: `UserLeap('track', 'event')` makes a network call so be sure to give it enough time to complete. If you would like to do a redirect or any action that may interfere with the network call, we recommend waiting for the [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) to complete.

```javascript
<script type="text/javascript">
    UserLeap('track', '[TEST] My first event').then(() => {
        // Event successfully tracked!
        // Do your thing here
    });
</script>
```

### **Verifying your Event-based Surveys**

We have checks in place to make sure we show surveys at the right time. To test that your surveys show with the right attributes and events set, be sure to setup the SDK with your **development** `ENVIRONMENT_ID`. This will bypass throttling and the re-survey window.

### **Option 2a: No Code Events - Page URL** 

No Code Events have three flavors, the most common one is Page URLs which allow you to define a single page, or a set of pages that can be used for targeting a survey for delivery. One benefit of using Page URLs is that they can be used for Survey Targeting with just the UserLeap JavaScript snippet installed, with no other changes to your site. To get started:

1. Include the JavaScript snippet in the page\(s\) you want the surveys to be delivered.
2. On the [Events](https://app.userleap.com/events) page, click the “Add” button on the right side of the page
3. Select "No Code"
4. For “Page URL Pattern”, you may type in an exact URL to match or a use a [regular expression pattern](https://www.oreilly.com/content/an-introduction-to-regular-expressions/) to match a set of pages \(e.g. **https://yourdomain.com/.+/accounts** would match [https://yourdomain.com/abcdef/accounts](https://yourdomain.com/*/accounts) and [https://yourdomain.com/123456/accounts](https://yourdomain.com/*/accounts)\).
5. Type in a name \(cannot be changed\) and a description
6. Click “Save”

You can now add this Page URL as a trigger for a survey

### Option 2b: No Code Events - Inner Text or CSS Class 

The No Code options allow you track events when a user clicks specific HTML element\(s\) on a page\(s\) in your app. These are also require the snippet to be installed configured and are configured on the [Events](https://app.userleap.com/events) page.

### Important

Surveys only support 1 trigger at a time. So a single survey may only have 1 Event trigger OR 1 Page URL trigger

### Customizing Appearance

You can set a hard limit on the height of your survey with the following code in the installation snippet

```javascript
UserLeap.maxHeight = '50%';
```

This will set the `maxHeight` property of the iframe.

The survey will show at the bottom right of the window by default. You can customize this behavior starting v1.9.0 to show the survey on the bottom left of the window.

```javascript
UserLeap.framePosition = 'bottomLeft';
```

Setting this parameter will make the survey appear on the bottom left.

Alternatively the survey can be configured to show in each of the 4 corners. Supported parameters are `topLeft` `topRight` `bottomLeft` and `center`To revert to default simply delete `framePosition` property from `UserLeap` 

```javascript
delete UserLeap.framePosition;
```

For `center` position, there's a default dark overlay covering the parent element. To configure a light overlay, you can configure this before presenting the survey: 

```javascript
UserLeap.overlayStyle = 'light';
```

## Performance 

In the modern web, performance is a critical part of any successful website. At UserLeap, we ensure that you can get deep insights about your users without sacrificing your site's performance.

#### **Speed impact on your website**

The script is loaded asynchronously so it doesn't not impact website load times or scroll performance.

**File Sizes:**

The UserLeap JS SDK is broken up into 2 JS files: a controller and a view

controller.js: **188KB**

The controller is responsible for keeping track of your visitors and your interface to track events and set attributes and identities. A vast majority of sessions are not shown surveys which is why we separated the view into a separate file reducing data usage for your users.

view.js: **213KB** \(users only download this when a survey will be presented to them\)

The view contains the code to show the survey and send the responses to UserLeap.

#### **Availability and Load time:**

The UserLeap client-side script is hosted on a leading global CDN powered by AWS CloudFront. This allows for the fastest load times by hosting the script as close to the users as possible.

#### **Cross-browser testing:**

The UserLeap client-side script is tested against all modern browsers, including:

Chrome \(latest versions\*\)  
Firefox \(latest versions \*\)  
Safari 8+  
Internet Explorer 11  
Microsoft Edge 40+  
  
\* Chrome and Firefox are on 6 week release cycles, so best effort support is given to older releases

#### **CPU Usage:**

UserLeap adds minimal CPU overhead \(less than 0.1%\), leaving application responsiveness virtually untouched. Our cross-browser testing suite ensures that UserLeap remains performant across all browsers.  
  


