# mParticle

## **What is mParticle?**

mParticle – a customer data platform \(CDP\) that helps B2C companies unify customer data and connect it anywhere to improve marketing performance, enhance analytics, and transform the customer experience

### **What Inputs Does UserLeap Support?**

We currently support [**Web**](https://docs.mparticle.com/developers/sdk/web/getting-started/) and [**Mobile**](https://docs.mparticle.com/developers/sdk/ios/getting-started/) \(iOS\)

mParticle will forward data server to server if they detect that the UserLeap kit is not included in your product. In this case, UserLeap will not be able to deliver microsurveys 

{% hint style="warning" %}
**Note**: with a server-to-server connection, UserLeap may still deliver [**email microsurveys**](../product-workflows/creating-an-email-survey.md) ****
{% endhint %}

Choose from one of the supported inputs in ****[**mParticle**](https://app.mparticle.com/setup/inputs/apps)

## **mParticle Web SDK Setup**

To send data from your web app to your mParticle workspace input, navigate to **Setup &gt; Inputs** and select the **Web** platform. The web SDK only needs the API Key \(not the API secret\), which you’ll replace in the snippet below. ****[**Reference the guide section**](https://docs.mparticle.com/guides/getting-started/create-an-input) for information on creating inputs.

The following snippet should be included on every page of your web app. Ideally, it should be placed within the `<head>` tag or otherwise be loaded as soon as possible on each page

```javascript
<script type"text/javascript">
    window.mParticle = {
        config: {
            isDevelopmentMode: true //switch to false (or remove) for production
        }
    };
    
    (
      function(t){window.mParticle=window.mParticle||{};window.mParticle.EventType={Unknown:0,Navigation:1,Location:2,Search:3,Transaction:4,UserContent:5,UserPreference:6,Social:7,Other:8};window.mParticle.eCommerce={Cart:{}};window.mParticle.Identity={};window.mParticle.config=window.mParticle.config||{};window.mParticle.config.rq=[];window.mParticle.config.snippetVersion=2.2;window.mParticle.ready=function(t){window.mParticle.config.rq.push(t)};var e=["endSession","logError","logBaseEvent","logEvent","logForm","logLink","logPageView","setSessionAttribute","setAppName","setAppVersion","setOptOut","setPosition","startNewSession","startTrackingLocation","stopTrackingLocation"];var o=["setCurrencyCode","logCheckout"];var i=["identify","login","logout","modify"];e.forEach(function(t){window.mParticle[t]=n(t)});o.forEach(function(t){window.mParticle.eCommerce[t]=n(t,"eCommerce")});i.forEach(function(t){window.mParticle.Identity[t]=n(t,"Identity")});function n(e,o){return function(){if(o){e=o+"."+e}var t=Array.prototype.slice.call(arguments);t.unshift(e);window.mParticle.config.rq.push(t)}}var mp=document.createElement("script");mp.type="text/javascript";mp.async=true;mp.src=("https:"==document.location.protocol?"https://jssdkcdns":"http://jssdkcdn")+".mparticle.com/js/v2/"+t+"/mparticle.js";var c=document.getElementsByTagName("script")[0];c.parentNode.insertBefore(mp,c)}
    )("REPLACE WITH API KEY");
```

When you add an input, you should be provided with a Key and Secret from mParticle: 

![](../.gitbook/assets/image%20%2823%29.png)

If done correctly you should the input listed  [**here**](https://app.mparticle.com/connect)\*\*\*\*

\*\*\*\*

![](../.gitbook/assets/image%20%2846%29.png)

## mParticle Mobile \(iOS\) SDK Setup

UserLeap supports iOS as an input for passing events and attributes from mParticle. For full documentation, read their [**iOS guide**](https://docs.mparticle.com/developers/quickstart/senddata#ios)\*\*\*\*

### Finding your API Keys

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/xQub7RJQ/121688a3-8d54-4666-9e91-d6b6e3a04a07.gif?v=e7650f72172218079bec3299e5c4b2bb)

###  <a id="create-an-input"></a>

### **How to Connect UserLeap & mParticle**

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/geubgEme/0a23c6ed-a39e-4817-87ea-cd204a3c6bcd.gif?v=6f814146cae6c79f5256e10a33d22493)

[**Here's a direct link** ](https://app.mparticle.com/directory/1169)to UserLeap 

![](https://lh5.googleusercontent.com/7voJ3ShOEskRXyzcPWoNsPEzxp7_4xSD2NlAtu7LwWLVN76tc1Jit5vvJyaumhTbklQ2nFh07xweoMak4GqH4DHD8ssjDnaHkBuVo4DHbbsrvIomIHebhyU7oCXbi-Xr1D13Ydmz)

Let’s start by configuring events to send to UserLeap

![](https://lh3.googleusercontent.com/xzTpar7dQkTP1Jja2zGMlhKC3s1VKfwjRSc4aZbUvVB4xN5EZRJxDydSYv0NbVkz_XFIDSNHqDepEmT59vvy6qrk_uOYfMkKuQCxDSVJzQnis95-j2MZVUlGGddRaixFntO9lJyn)

Both your Environment ID and API Key can be found on the UserLeap ****[**Connect page**](http://app.userleap.com/connect)**.** If you would like to keep the same settings for development and production, you can choose to do so

Give the configuration a name - _the idea is to have two setups one for your UserLeap production environment and the other for the UserLeap development environment_

See above on how to find your API keys for mParticle

![](../.gitbook/assets/image%20%2845%29.png)



Now we'll configure an audience 

![](../.gitbook/assets/image%20%2818%29.png)

Please give the configuration a name and then enter in your API Key. Click Save when finished

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/llu5Nl0Y/f310c812-2951-4514-81ac-432ccb5aa899.png?v=97d640eaec799d919268526340b47d65)



You may need to create an audience in mParticle if you have not done so already. Go to the [**Audience page**](https://app.mparticle.com/audiences) in mParticle to ceate a new audience

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/ApuYzdXv/9f5b0b88-6736-4b20-8998-8bf66bcac52f.png?v=c61974a371ec0da0049185dc423c609f)

## Can mParticle Trigger a UserLeap Microsurvey?

Yes! Events sent from the mParticle SDK can in fact be used to trigger a UserLeap microsurvey. For full details on events, please read more [**here**](../product-definitions/events.md) ****\(or see table below\). 

![](../.gitbook/assets/image%20%2816%29.png)

{% hint style="warning" %}
**Note**: mParticle events sent using server-to-server \(mParticle firehose\) cannot be used to trigger a microsurvey. These events can however be used as a [**survey filter**](../product-definitions/interacting-with-survey-filters-and-triggers.md)
{% endhint %}

## Can mParticle Events/Attributes be Used as a UserLeap Microsurvey Filter?

For [**survey filters**](../product-definitions/interacting-with-survey-filters-and-triggers.md) ****you can use events that are sent though the mParticle SDK OR events that are sent network to network from mParticle to UserLeap. 

Attributes sent from mParticle \(also known as audiences in mParticle\) can be used as a survey filter. To learn more about attributes, read [**here**](../product-definitions/attributes.md) ****\(or see table below\)

![](../.gitbook/assets/image%20%2858%29.png)

