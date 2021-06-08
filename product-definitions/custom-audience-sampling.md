# Audience Sampling

## **Setting Sampling Parameters**

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/wbuwWXem/3802ab8b-c060-4c5e-83f8-44c713ccd95b.jpg?v=383e7a26e62ecad74cbe8ae2787f4f03)

UserLeap, by default, will determine the total number of responses that need to be collected in order to meet [**statistical significance**](https://www.greenbook.org/marketing-research/statistical-significance-03377#:~:text=What%20is%20statistical%20significance%3F&text=To%20say%20that%20the%20observed,drawn%20would%20yield%20similar%20results.) \(yes we do all the math, so you don't have to!\). 

When adjusting microsurvey sampling, there's two things you have to consider:

1. Delivery Options
2. Setting Confidence

There are **two** delivery options to choose from, "Deliver until statistically confident" or "Deliver Continuously"

### **Deliver Until Statistically Confident**

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/OAuPBoon/fb92d813-9ede-4ecc-a8ff-be5d2f4701b8.png?v=895d80cd8019152c0d1a51b63ff31c94)

UserLeap will collect a fixed number of responses, after which the microsurvey will be set to complete.

### **Deliver Continuously**

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/mXupADGB/0950ddf9-e6a2-416e-8093-b1883cf47226.png?v=5a6a715c110f66113ac06236d14351c2)

UserLeap will deliver a fixed number of responses **per day** and will continue doing so until paused \(or marked as completed\)

{% hint style="info" %}
The responses each day is the **maximum** number of surveys UserLeap will **send** in a single day. If you are experiencing a 33% response rate, you can expect 18 responses/day
{% endhint %}

### **Setting Confidence**

We automatically recommend that all microsurveys run at the 95% confidence interval \(High confidence, slower results\). However, you do have the option to adjust to accommodate your own user research needs

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/E0uYzXed/253a1fac-9c99-4331-994d-4b220bed7dd2.png?v=0c3e4057871d71f8e5456187e94bd5f9)

* Lower confidence, fastest results \(80% confidence interval\)
* Medium confidence, faster results \(90% confidence interval\)
* **High confidence, slower results \(95% confidence interval\)**
* Highest confidence, slowest results \(98% confidence interval\)
* Custom

## **Custom Audience Sampling**

UserLeap incorporates best in class practices to limit [**sampling bias**](https://www.scribbr.com/methodology/sampling-bias/#:~:text=Sampling%20bias%20occurs%20when%20some,external%20validity%2C%20specifically%20population%20validity.). How does this sampling work? We use what's known as the [**leaky bucket**](https://en.wikipedia.org/wiki/Leaky_bucket)**.** 

What you should know is that under standard guidelines, not everyone that qualifies for a microsurvey will receive one. Instead, we throttle sends to ensure a microsurvey runs over a period of time \(days or in some cases a week, depending on response rate\) 

### How to Override Sampling in UserLeap

Want to have more control over your microsurvey delivery? By setting a UserLeap microsurvey to **Deliver Continuously** AND selecting **Custom** from the dropdown you can effectively nullify our pre-sets for sampling

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/z8u68G0l/2bdd2c1a-7bbf-4dfa-b579-6652ab7356b5.gif?v=b233f34f1c98186fd6d969fb2087038d)

{% hint style="info" %}
Please enter a value between **1 - 100** for custom sampling. Setting this value to **100** will ensure that all qualifying users will receive a microsurvey
{% endhint %}

Another option, is to tell UserLeap exactly how many responses to collect before the microsurvey should be set to complete

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/8Lubq02E/7bc5c85d-83d3-460b-a34b-214d5cb73609.gif?v=a7dec9525a9eeb72c0f768eb21dd8bff)



