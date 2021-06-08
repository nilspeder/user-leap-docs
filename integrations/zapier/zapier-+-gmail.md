# Zapier + Gmail

{% hint style="info" %}
 **Note:** Zapier may require access to admin permissions, please contact your company admin if prompted to do so
{% endhint %}

**Source:** UserLeap

**Destination:** Gmail

**Description:** Save time by automating your follow-up process with new respondents to your UserLeap survey. With this integration, a custom email will be automatically sent from your Gmail account to a specified recipient. Send thank you's, schedule interviews, trigger updates, and more!

## **Can UserLeap Help Recruit Participants?**

Yes! UserLeap's template gallery comes with 80+ ready to go templates that are great for:

* [**Acquiring More Customers**](https://app-staging.userleap.com/collections/2)\*\*\*\*
* [**Launching a New Product/Feature**](https://app-staging.userleap.com/collections/4)\*\*\*\*
* [**Onboarding New Customers**](https://app-staging.userleap.com/collections/3)\*\*\*\*

and more!

We also have a whole collection for [**Recruiting Interview Participants**](https://app-staging.userleap.com/collections/12)

## How Does Zapier Help Recruit Participants?

1. Launch a survey using one of the [**Recruiting Interview Participants**](https://app-staging.userleap.com/collections/12) ****templates
2. Create a filtered workflow in Zapier that emails a pre-built link to anyone that agrees to be part of the study \(e.g. [**Calendly**](www.calendly.com)\)

{% hint style="info" %}
The workflow below is built off this [**microsurvey template**](https://app-staging.userleap.com/collections/12?template=1479)\*\*\*\*
{% endhint %}

Each UserLeap account will come with two API keys, one for your production environment, and the other for your development environment 

  
****Create a new Zap, and select **UserLeap** as the trigger

![](https://lh3.googleusercontent.com/38r_-KTOAelzuLY4yAixqbC6DlfgKutUe4BdYa9P-BbyTUxLnjaNzvZM8PQ6hlI46Z2tIQ1ba69gcQ1hkre468ovFSexVUDKhKXBKYPMPyq-NS1FON5YxWfRTxVwmPNz4HmyS7x1)

![](https://lh6.googleusercontent.com/9wRl9l5Fdej-NlgaA-wXv6DxroEhvcAN71XcZGrIVrMDRDDVD8T3FBcHXFEk677z792p34s928vG-VxrAZp888IluM3ipPfG74ZH5FZpUXnAHEtCFxUhhTcoAly9CKXLzfymH4T5)

**‌**

If asked, "Sign in" to UserLeap using your ****[**Zapier API Key**](http://app.userleap.com/connnect)**.** If you’re unable to locate your Zapier API Key, please contact support

![](https://lh5.googleusercontent.com/tS_QdQnFUZHnYLJM290iFxmOURHpiOgG-RdAaFvRhu6q03LR-zy7wHqkoQPu3UYL38cE9RBpb0UeXHYen_hKG8Um2cL50ttmx49dhWVviyrVBgKYZvvzT7SJa5tr5mx1CtwIwH7m)

**‌**

Select **New Survey Response** as the Trigger Event

![](https://lh5.googleusercontent.com/7RbhSe8K8Z_O_PFsNAq2WuriDCivFlvpOhJX5v2WWaGvm--QXR25xieWJ9f9xrkDPanrtPwOyZ0YNauLmseEQEhVBMM9thrJV1oxBdnjy3gIbZ-o17ECCAfzddQicCOacOCKSOI2)

**‌**

Click “Continue” and then “Test trigger” \(testing is optional\)

![](https://lh5.googleusercontent.com/rlT9vntcE4IHuMOoxlDTfDHtOj9jDwIv3MOQVqyTGKDhN0EG2zd-RjoLfVU7BxYgU_MYS1vfQy2v9XS_tnzx6OHXKOmRFb4xO8lH7UhsDGpXoLvWJuvMwcP1HSh0oLnq2-B8_RXL)

**Add a filter** before selecting an app

![](https://lh5.googleusercontent.com/KoVuHVt8MOtevdVEBNtQOLH7wegRV97E58_uIIgSGQ3bsoQXJq9uJP7exNSssD5-asO9rLcFfrf8cSRyAVzb0NBGlreDHS7JK28j6TDo7PEVjw-cXF1teTSeybGWdhFgzv34GWu2)

**‌**

We only want to send an email to participants that have "accepted" the opportunity to be part of a study. Here an idea of how to create the filters, this may vary depending on your microsurvey question configuration.

**‌**

The two filters below work as ANDs. This flow will activate when the following two conditions are met:

**‌**

* This Survey Name contains Recruit \(please make sure you add this to the title\)
* There's a response that has someone's email \(the "@" symbol\)

![](https://lh4.googleusercontent.com/l0nKmOviKld1irFbOmTg0ogXy_ScxJvXv6ChXqz1RQ3sEdoelH51rskSzRtIByPhGkYa47sbCtBdcwby7Xa25hDT_ihnUOuejcb-wPoa1Qo0eMY8l6jsO0r6Bi-h13Jc5kArOaJZ)

Search for Gmail as the action \( e.g. where should the data be sent to\)  
****

![](https://lh3.googleusercontent.com/xHjp4mUuKZJSm6e9C9jfwblwh8F6dc30732-lgQylW9Jz_vwAg3GNd5k4ZMx54SY15lt4XvSr8Jmmpu9eb472ssxZGxblIjpEDGVKA648kx2tFah1pjqu6EgKskd1o-u1_HhqlYc)

Choose the Send Email action. For all available actions supported by Gmail, visit the[ **Zapier Library**](https://zapier.com/apps/gmail/integrations)\*\*\*\*

You may be prompted to authenticate/sign in to Gmail  
****

![](https://lh3.googleusercontent.com/yz8xV-XUwlrhXD4RUylrv-8IY9X4q_NyQer09N9LSsZGMGO4hAmhB-jP41VCvvpfZi-AVoKruZHNJ4x8LD-2J81hQPcyzyMF8E6i4aIbJeu3matVLHkdnS5QhTiLR7jXVQQmjEID)

**‌**

Fill out the fields highlighted below \(some are optional\). You'll notice how you can use UserLeap provided fields to create a more personalized experience

**‌**

**Example:** in the example below I added the UserLeap Survey Name in the subject of the email

\*\*\*\*

![](https://lh4.googleusercontent.com/Fhchfg7C_nykie4181juVaj5qL2sroD06ot_gwVMKwmLFHdaIk33ghwrA3-Ufpws0zzc2YPIwAvjpOM_3Xxz9hmXpoi8XlaCwHetwB5AXPLIH-3vXgXROyzPH11bcjNOCrgMVb8G)

  
****

**‌**

Once finished press "Continue"  


You have the option to test your Zap or skip and make live  




