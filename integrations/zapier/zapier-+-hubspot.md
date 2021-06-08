# Zapier + Hubspot

{% hint style="info" %}
**Note**: Using Zapier may require access to admin permissions, please contact your company admin if prompted to do so
{% endhint %}

![When complete, you should have this saved to &quot;My Zaps&quot;](../../.gitbook/assets/image%20%2824%29.png)

**Source:** UserLeap

**Destination:** Hubspot

**Description:** Having quick access to your HubSpot contacts' latest comments or satisfaction scores is essential to providing a best-in-class customer experience. This Zap makes it simple and efficient to save your latest microsurvey responses to HubSpot contacts. With this integration, whenever a new UserLeap response is received, Zapier will automatically create or update the correlating HubSpot contact, as well as an engagement for them

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

Look for Hubspot as the **action**

![](../../.gitbook/assets/image%20%2819%29.png)

In order to update contact information in Hubspot, we must first locate the contact in Hubspot and tie in a Hubspot identifier. To do this you'll need to first add an action to  **Find Contact** and follow that up with one to **Update Contact**

For all available actions supported by Hubspot, visit the [**Zapier Library**](https://zapier.com/apps/hubspot/integrations)\*\*\*\*

![](../../.gitbook/assets/image%20%2841%29.png)



Choose your Hubspot account \(must authenticate with Hubspot\), then press "Continue" 

![](../../.gitbook/assets/image%20%2856%29.png)



Locate your Hubspot email field and select it as the **First Search Property Name.** Next, use the **Email** property found in UserLeap and use it as the **First Search Property Value**. 

Determine whether or not you would like to create a new Hubspot Contact if the email value of the UserLeap response does not exist in your CRM \(optional\). Press "Continue"



![](../../.gitbook/assets/image%20%2848%29.png)

Add a third action, from Hubspot, this will allow Hubspot to **Update Contact**. Then press "Continue"

![](../../.gitbook/assets/image%20%2868%29.png)

Please note that you should already have an existing property in Hubspot to populate this data. If a custom/in-built property does not exist, or you would like to create a new one, read this blog on how to [**Manage your Properties**](https://knowledge.hubspot.com/crm-setup/manage-your-properties)\*\*\*\*

In order to **Update Contact** Hubspot requires that we match on an Object ID, this will be brought in from the first action \(**Find Contact**\). Again, make sure to update any existing/new properties as needed

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/Jru4EGnX/bc0a0832-bcf8-4948-9220-a798bdedc791.gif?v=4e7198edb1844211379fdc0213e2b107)



When finished, you can either "Test Action" or "Turn on Zap"

![](../../.gitbook/assets/image%20%2831%29.png)



