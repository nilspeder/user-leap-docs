---
description: UserLeap install instructions for Web
---

# Web Applications

## Options for Install

To install UserLeap on your web landing page or web application, you have the following two options: 

{% page-ref page="javascript-sdk.md" %}

{% page-ref page="google-tag-manager-new/" %}

## **Sending Events to UserLeap**

UserLeap relies on event tracking to accurately deliver surveys at configurable intervals, all dependent upon user behavior. 

Once you've installed the UserLeap SDK, the next step is to send UserLeap events that you would like to use to trigger a microsurvey. The two types of events we support are:

1. [No Code](https://app.userleap.com/events)
2. Code

No Code Events can be configured within the UserLeap UI and oftentimes do not require additional support from an engineer/dev partner. We call these codeless \(or no code\) events.

### **Sending Events with JavaScript Install**

_If you are using the JavaScript SDK to install UserLeap, you can read more about sending events by reading the_ [_Display Survey_](javascript-sdk.md#displaying-surveys) _information in our JavaScript documentation_

### Sending Events with Google Tag Manager

_If you are using Google Tag Manager to install UserLeap, you can read more about how to configure events by reading our_ [_Tracking Events_](google-tag-manager-new/tracking-events.md#setting-up-events-as-triggers) _step by step guide located in the GTM documentation_

## **Sending Attributes to UserLeap**

* Note: Attributes with more than **100 distinct values** will be auto-rejected

Similar to Events, Attributes help you better target audiences that you would like to survey. Attributes are custom traits that are defined on the client side and are used as [survey filters](../../product-workflows/launch-a-survey.md) in UserLeap.

### Sending Attributes with JavaScript Install

If you are using the JavaScript SDK as your method of install, sending attributes is simple and involves invoking  

```javascript
UserLeap('setAttribute', attribute, value)
```

Similarly, you can also do the following

```javascript
UserLeap('setAttributes',{
        key1: value1,
        key2: value2
    });
```

For more information on sending custom attributes read [here](javascript-sdk.md#custom-attributes)  


### Sending Attributes with Google Tag Manager

There are many ways you can send attributes using GTM, and it can vary from setup to setup. Three of the most popular ways to do so are: 

1. [Google Tag Manager's Datalayer](google-tag-manager-new/adding-attributes.md)
2. Capturing from your Local Storage
3. [Creating a Custom JavaScript Variable](https://support.google.com/tagmanager/answer/7683362?hl=en)

