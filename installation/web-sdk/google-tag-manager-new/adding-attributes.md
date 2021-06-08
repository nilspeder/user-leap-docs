# Adding Attributes

## Sending Attributes to UserLeap

Like events, attributes are just another way to enhance your microsurvey targeting functionality. While events are triggered behaviors that occur on the client-side, attributes can be thought of as groups or segmentations that are assigned based on that behavior.

For instance, if I’m a SaaS company and I have three plans \(free, growth, and enterprise\), I might consider sending UserLeap an attribute of `planType` that could carry any one of those three values. 

There are many options to send attributes to UserLeap using Google Tag Manager \(see below\)

1. Send from GTM’s data layer 
2. Write a custom javascript variable that defines a variable \(attribute\) and correctly determines the value\(s\) that should be assigned
3. Utilize local storage
4. Work with 3rd party cookies

This guide will cover the first option, the Google Tag Manager Data Layer

## What is The Data Layer

The data layer stores information that is critical to your business and works as a middleman between Google Tag Manager and external applications \(Ad accounts, Analytics Tracking, etc\)

### How to Check Your Current Data Layer \(if Applicable\)

1. First you’ll need to make sure you have Google Tag Manager installed. Here’s how to do so
2. Open up the development console and then type in window.datalayer
3. Press return

To open the development console:

Mac: Cmd + Shift + i

Windows: Ctrl + Shift + i

### How to “Push” to Data Layer

If you are just getting up to speed on how the GTM data layer works, we recommend speaking to an in-house developer or someone that owns the internal tag repository. 

Generally speaking, the easiest way to create the data layer is using the `datalayer.push()` method

_Note: The GTM data layer is created by default when you deploy your GTM container_

###  Using the Data Layer to track Events + Attributes

```text
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
 'formLocation': ‘footer’,
 'event': 'new_subscriber'
 });
```

```text
window.dataLayer = window.dataLayer || []; 
window.dataLayer.push({ 
 'event': 'checkout', 
 'customerInformation': [{
        'planid': '52',
        'planName': 'Essentials - 20k',
        'costPerMonth': 79
      }]
});
```

### How to Create a Data Layer Variable in GTM

```text
<head>
   <script>
dataLayer.push({
'customerInformation': [{
'planid': 52,
'costPerMonth': 79,
'planName: 'Essentials - 20k'
'teamid': 12345
 }]
});
   </script>
   <!-- Google Tag Manager -->
   ...
   <!-- End Google Tag Manager -->
</head>
```

In order to create a variable, you’ll need to specify the Data Layer key of which value you want to retrieve. These are key-value pairs, and in the example above might look something like this

 **Key**: customerInformation

 **Value**: planid, planName, costPerMonth, teamid

### **Step By Step** Instructions

Go to variables, and add a new “User Defined Variable”



![](https://lh6.googleusercontent.com/6JcOziYB0rVf9FWk11t-kXf1z2RtUAxK9TcVQDYeW4D0l7qCl7X0FjMjXk-8b1jt9Gko2nPCYGatZY5FrjYevVj4QIE_SAVqBTtByIuhQLODXpCRfFLub9Yh5-JZlmzeYPGmp38S)

![](https://lh6.googleusercontent.com/dOwAfN17wA60qNSZVuOY8HkgLZcBTfHrNabS-0gTEszulUy7WCufvaNNooWkSzdoY52VUhj8GPP-wbY-_hSkTtCu4yb0LfYMwdcKR4n1CHGwMYRcWfq46LQRvvRSTQRrLlx3SxZT)

  
Select a “Data Layer Variable”, give it a name \(we recommend a naming convention to keep everything organized\)

![](https://lh4.googleusercontent.com/H57CRHYLKz048N-N2FQLPOwYGQ9taqcjJseBZaLfrTMzwv1jLJkoAzqU4KclJeDrYlohFJabh-9d0egLLrRItlslmk1jSyfbgUhu4DhREtRWnTLbqvezvviXiEw_47ld2uw5gUA4)

Then we’ll want to add in the key \(the name of the variable\). In the example below I have to specify planid using dot notation since its an object within the customerInformation variable

![](https://lh6.googleusercontent.com/rUijyxjt-7ANzNW9wI6RlO1VUmHlKAsUJU_dl_jv1C16IVJjZhDVPG8azhnn0H2TI1ovU9lHpgeAprtDxrFSZsHpyD3XjJrFzT5FI5SfrTCPaY514gP9Wyjcxd_nkN0tPf9Gf-gj)

Once finished, we’ll just add it to a UserLeap tag and deploy. Make sure the tag dropdown is set to “User Attribute”. The key and value can be set dynamically using the configuration seen below. As for the trigger, all pages is what we recommend

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/v1ubPq4J/8626a017-1802-424e-bd68-93267d229929.jpg?v=a66770d82345e23ceb1bed800766fb8d)

You should start to see an attribute in UserLeap, under [**survey filters**](../../../product-definitions/interacting-with-survey-filters-and-triggers.md), with the name `PlanId`

