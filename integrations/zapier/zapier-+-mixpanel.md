# Zapier + Mixpanel



{% hint style="info" %}
**Note**: Using Zapier may require access to admin permissions, please contact your company admin if prompted to do so
{% endhint %}

![When finished you should have this Saved to &quot;My Zaps&quot;](../../.gitbook/assets/image%20%283%29.png)

**Source:** UserLeap

**Destination:** Mixpanel

**Description:** Sends new survey responses in UserLeap as they come into Mixpanel. Each survey generates new Mixpanel events.

Each UserLeap account will come with two API keys, one for your production environment, and the other for your development environment   
****

Create a new Zap

![](../../.gitbook/assets/image%20%2870%29.png)

UserLeap will be the **trigger**

![](../../.gitbook/assets/image%20%2837%29.png)

Search for UserLeap

![](../../.gitbook/assets/image%20%2867%29.png)

"Sign in" to UserLeap using your [**Zapier API Key** ](./#how-to-find-your-api-keys)\*\*\*\*

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/8LubP5NK/511d0a24-02ef-4b63-9b40-10ab7e96f9db.gif?v=edb3c8091586b08c277700adad5796e9)

After that, select a trigger event. The trigger event will be "New Survey Response". Then click "Continue"

![](../../.gitbook/assets/image%20%2859%29.png)

Next, we'll want to test our trigger

![](../../.gitbook/assets/image%20%2836%29.png)

Add an **action** and search for Mixpanel

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/E0uYJRb4/d097a9e0-8860-4bd0-8903-7639c1baa05d.jpg?v=8cddcedb03c91f033324cfc2cabcd41b)

Select **Create or Update Profile.** For all available actions supported by Mixpanel, visit the [**Zapier Library**](https://zapier.com/apps/mixpanel/integrations)\*\*\*\*

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/eDujenYx/1f57555f-f81d-4900-9bbe-0e29a1743261.jpg?v=d924d13241457b5cae8ebcf1e4ea4c84)

Choose your Mixpanel account \(must authenticate with Mixpanel\), then press "Continue" 

![](../../.gitbook/assets/image%20%2822%29.png)

Add in the UserLeap **User ID** field to match to Mixpanel's **Profile\_id**. Select the properties you'd like to export from UserLeap over to Mixpanel. We recommend the following: 

* Survey ID
* Survey Name
* Response
* Question Type

![](../../.gitbook/assets/image%20%2830%29.png)

Test your action, or "Turn on Zap" if you're ready to proceed

![](../../.gitbook/assets/image%20%2849%29.png)

