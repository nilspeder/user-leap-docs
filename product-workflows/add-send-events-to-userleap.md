# Add Events to UserLeap

## **UserLeap Terminology**:

### **Events**

An event is an action that takes place in your web or mobile application. Events are used as both a trigger and a filter for a micro survey.

Examples of events include: 

1. \*\*\*\*[**Visited a page** ](page-url-events-and-regex.md)\(i.e. visited the dashboard page\)
2. Clicked a button
3. Page scrolls

All events are located on the [**Events page**](https://www.app.userleap.com/events)\*\*\*\*

_Refresh your knowledge of events and attributes_ [_**here**_](../product-definitions/)_\*\*\*\*_

### **Trigger**

The event that must take place for a user to qualify for a survey. Each survey MUST have a trigger. Triggers are also known as events. 

### **Filter**

Filters are useful when you want to segment the audience that should qualify for a survey. We’ll sometimes reference these as “survey filters.” Multiple survey filters are treated as ANDs and not ORs.

### **Adding Events to UserLeap**

Assuming that you’ve installed our SDK \([**installation docs**](http://docs.userleap.com/installation)\), the next step is for you to send an event. This must be done prior to launching a survey\*

\*_if you launch a survey before installation, the survey will be “active” in UserLeap, but will NOT trigger on your web-page/mobile application._ 

UserLeap currently supports three types of Events:

1. Programmatic events
2. \*\*\*\*[**Page URL events**](page-url-events-and-regex.md)\*\*\*\*
3. Interactive events

_Page URL events and interactive events only apply to web and mobile web \(mobile web = web browser app on a mobile device_

UserLeap also supports native integrations with both [**Segment**](http://docs.userleap.com/integrations/segment) ****and [**mParticle**](../integrations/mparticle.md)\*\*\*\*



{% hint style="info" %}
If you have any questions please email us at **success@userleap.com** or use the in-product help chat
{% endhint %}

