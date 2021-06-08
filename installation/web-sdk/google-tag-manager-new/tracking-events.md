# Tracking Events

## **Setting up Events as Triggers**

**‌⚠️** The types of triggers will vary as per your individual use-case, for more information on what all is possible please visit Google Tag Manger's[ trigger configuration documents](https://support.google.com/tagmanager/answer/7679316?hl=en)

**‌**In UserLeap, each survey requires a trigger. UserLeap triggers, **not to be confused** with Google Tag Manager triggers, determine when and where to survey users. A helpful way to think of a trigger is “the action that causes your survey to appear”. Here are some common Events that people use to trigger a microsurvey:

* Finished Onboarding
* Visited Dashboard
* Logged In
* Canceled Subscription
* URL matches \*.\/settings\/.\*

**‌**With Google Tag Manager, no coding is required to send these events to UserLeap. To do this, you’ll need to complete the following steps, which we walk you through below:

1. Make sure the “triggers” \(such as clicks, page views, scrolls\) are configured in the variables tab
2. Apply the relevant trigger\(s\) to the container
3. Apply trigger to tag, and publish

### **Configuring Built-in Variables using Google Tag Manager**

**‌**In this example, we are going to configure an event that tracks a specific button on your website and add that to UserLeap

‌Out of the box, meaning without the need of any custom code, Google Tag Manager allows you to track events such as clicks, pages, scrolls, etc. Let's go ahead and enable these variables.

Please note that you do not need to configure all of these variables, only the ones you foresee needing/wanting Google Tag Manager to track. Variables that are NOT assigned to a trigger will not have an impact on your Google Tag Manager implementation

#### **Step by Step**

**‌**Click on "Variables"

![](https://lh5.googleusercontent.com/UBqXj8PfSkkQc8hwwuQ-b-uGGo0U3LkUe3XGoyFbEN38gyHX6RAtdPdYPbFBu-v0FXxgnpUzwePbSWOcagbho4t6cWfKxr4zSED6bfwZB7YxmjFfQjfBRaA2qFjhOcVdZxYc0AE3)

**‌**

Select "Configure"

![](https://lh5.googleusercontent.com/ZIw-ryEQzO6O0LTe4Sg2ZKOcGrpSeZS2Ycf4Ko4AEyiZyFzO2K_b1fwYxbd1h-PoPMWwo060WqzD6M-yxR0UNLjW-AZQ3Kz8IPR7R2raeMmYSeYLp1nIyo498mBX6a43q896sccK)

**‌**

Select all the variables you want to enable

![](https://lh5.googleusercontent.com/FX_I6q81YAHXvtTazPO667rFT1RWKaHaJWyN6Fv6Vca78PSKFX8e1EV7Mmd3W0njo3Dv1Q7nDbkwYb5SclIGt_v2cmCYzgxCrI5IkTjLlOrDnrhJYmB9EAX5OfHjvPE_s7bY8-fP)

### **‌Apply Triggers to Track an Event**

**‌**

This specific event trigger is for click-text \(i.e. targeting the text given to a button in the CSS of a page- also known as inner text\). 

Let's name this UL\_Click Text - \[Name of Button\]

#### **Step by Step**

Let's create a new trigger that helps us track anytime someone clicks on button text. We'll name this trigger UL\_Click Text - \[Name of Button\]

Click on the “Triggers” container on the left

![](https://lh4.googleusercontent.com/h9cw4ujeuxXN01LG8RBOBODW--DyC0VXP0DP6cbE9E-tNbO6N5NPnC3aBwEwROCz3armqJj8qcKchLh1sw9iz-chJAM2i1vgS5e-Tlu7K4yGrvlohLSoM41z5s9dd3sQdMzUKfJb)

Give your Trigger a name, we provided an example name above but feel free to customize it  
****

![](https://lh6.googleusercontent.com/EOXkjJV2ScJfvuDV2yIMfehY4wGQsVP_HIV40H7UzrfDjnXxiylx6kulhBjs47K6ttj4Y2tG16bZZkBYY2g1mPykhgcbqA5DpNGD34HPoymVUwx6ZzsLu5N7vqkzVl4iTbSWLPUo)

Once you click on the “Trigger Configuration” portion, you’ll want to select the “All Elements” trigger type  
****

![](https://lh4.googleusercontent.com/20RudGgi62oYQ0L5QnFFA6iQGz7N7hk2r9ydzxcDrLiIUk96RIYQOEhmiTYSpOXbinzKIN5ORrJ5P_FyXOZjaPtm1AoNo0sWNe5jh9b-kxJWIJfwNyBEaZdN7NWjXl7ekN9XB-9K)

After selecting the “All Elements” trigger, make sure you change to fire on “some clicks”. Next, filter for Click Text and contains \[name of your button text\] 

![](https://lh6.googleusercontent.com/MaeXGs0AtJS6N2i4yfRNC86J3mXx9Yj03YxCSjaec6eQp82nChNq8BhUTNdr4zeehc5ScbcCrfnScHnIMKtKpIcwySMu0m39mBUwNLoxUVY8Bnoi4KBU9C1JOc_6KftWICjSCaUr)

### **Create a Tag to House the Variable and Trigger**

When complete, don't forget to "Publish" to make the changes live on your website

#### **Step by Step**

Remember, all triggers must be part of a tag before we can deploy them. So next, we'll create the UserLeap tag for this click-text event.

![](https://lh6.googleusercontent.com/aKwCpp-2MqeAloArzyVZE2mVHbly_osV9T3nwCMFIpCcQy1YxmztKJvL7jPTIL7ZTzJiNB8bVZMe0yp8-9OgdEQSOfuagX6oNulg4War8ohAm3GURVX5k7AnN6PUySSn-Uwxqhcu)

![](https://lh6.googleusercontent.com/AKllQgX2e8YainGlpBiFHOz2k71Yw9DpvgHao-ZondWaI7qQ2DTCfB0Sn9rG1E2kFu8L8QwMi6JPvHJULUj0_d-X7igUjsbF9LLSYCw5CpuAbuJ6_TgZRPki1Sr45W1Cg3zw6N_2)

![](https://lh3.googleusercontent.com/qGPlNEyG6_R34J0ifvP-9fdYK5Gp2AmnLYY0OPZD9WMescU67m5dYcalQzLwXWFvAUwPo5O_abPAyXH_IMs8EM_nfFyDmrXYs7qdSxEKqIlalGSYh2v2nmnt3q8rY7vGpvoAMr6h)

\*\*\*\*

**‌**Let's give the tag a title. We’ll name it UserLeap Events

![](https://lh5.googleusercontent.com/ZLATWmovSbUGgvJNvhjEIkRFGjx1M2uLtUXAtlNZ5s3DsiVnR_0AdjLk3Ia4sN0AYxemzR3gtd09s0MqsybA41gnuX4YqidPEq5xzI666q22wTSAAPqtHTm2iYYkmQ95hw3IsFz6)

To add the UL\_EnvID you'll need to click on the respective 'lego-looking" icon in the image below. Add our UL\_Click Text trigger.

For the "Event Name" you have two options:

* Name the event: Clicked on Analytics \(or anything similar\)
* Use dynamic naming, based on the "text" that was clicked \(recommended\)
  * If you plan to add more triggers to the same tag, option number two is a lot easier to both manage and scale!

‌For dynamic naming, click into the "lego-looking" icon next to the "Event Name" and then select the "Click Text" option. This will effectively name ANY click tracked by GTM and sent to UserLeap as {{Click Text}}

In this case we'll modify the name a bit further to read as Clicked On {{Click Text}}This will add a bit more context as we most likely plan to add future click interactions to the same tag. Once finished, click “Save”   
****

Make sure to publish your changes by click on "Submit"

![](https://lh3.googleusercontent.com/gXLBA3ikB6ORRe1TQRV0UQ4ydU32OUgaZaJbUiJRVOTVVYwhXrWbLDtbxxWlUEwGkzN4zsbh0U2i_dCBDCDPF_eBZM-QXln_JyGjpEWYmzjFdTALK1cMTwShh26fOQUqaDPq_Mlo)

**‌**

⚠️ if you wish to test your variables, tags, and triggers before deployment, please read this[ documentation from Google](https://support.google.com/tagmanager/answer/6107056?hl=en)



