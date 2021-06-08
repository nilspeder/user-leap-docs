---
description: 'How to set up SSO authentication, using Okta'
---

# Okta

## UserLeap Okta Integration

Step by Step 

1\) Contact [sso@userleap.com](mailto:sso@userleap.com) or success@userleap.com to claim the email domain\(s\) that your SSO users will use to sign in

2\) Log into your UserLeap account and navigate to the [SSO Settings Page](https://app.userleap.com/settings/sso)

3\) Select the “SSO Enabled” option, and click “Save”

4\) An “Important Values” section should appear.  Take note of the values provided.  You will use them to configure your Okta integration in step 10

5\) Log into your Okta account and go to the Admin section.  Make sure you are using the “Classic UI”.  Then navigate to “Applications”

![](https://lh3.googleusercontent.com/jslJQ2pfeI1rJqomZusYDHL9dvvxe13fvLwRc7nG0EP58Xenri2vg4EEedZRTQFHcvKxHseMH7YxMJhCNctBQLidMF7VrjOMvT2MIjcvt8jBwT38JRJt1bbc3rzbFYVE2Rnl0iiS)

6\) Click on the “Add Application” button

![](https://lh6.googleusercontent.com/ppxa0JK8v9ikzl1ec1kXtRSyifU449y_CueAhn6yfR5UUYgluqSmuas3bQRzYN5gRRttLimn0Sq-YESbA7fTtneY5KfAwChbIPy9j_GKJn3fAcuFCH7hEZhulrjFliY-fLmiivgC)

7\) Click on the “Create New App” button on the right

![](https://lh5.googleusercontent.com/15cfgkXb47RAUWLWClUa9XGeFUzpVMlomqdUCWma8Ver6IQp39krpnn9I2ztDYzVRXh7MFODDs3_wtnMGJKCSB3jMJOyKXROtAGsnXuJw5BtK3xKIL_E9d1mIsDqd8dTDoEPDZIx)

8\) A modal should appear.  Select “Web” for the platform and “SAML 2.0” for the sign on method.  Then click the “Create” button

![](https://lh4.googleusercontent.com/Gzz3MqbkESPVm8TY_Sw--57D5aJ26JIcgNk8HVlVp6iQBhq2-YXP8rGQv-lOHUvxdkbpVpu61moEBzH58lw0KQZERjp7-dZ6SBy98tfN7omuQvEV2FYiPzcvYPlYinZFMWaEZb_G)

9\) Enter in the name you want for your UserLeap application integration and click “Next”

10\) The next screen is where you will configure the SAML settings.  Use the values you were provided by the UserLeap SSO settings page in step 4 to enter the **ACS URL** into the **Single sign on URL** and the **Entity URI** into the **Audience URI**

![](https://lh6.googleusercontent.com/QCKdbHkMDz7dUgb4TiKpn4tI9QlfW_vcswRUlBh3VZvrXzWolARukBB8QndfhRfrU8a_yW7Nx-snMEcZkN4wRVZhGKctaWcgyJdRH_MfJTuvBCpnWS-iBp_cj_uEeolRkoFNMPlK)

Keep the **Use this for Recipient URL and Destination** URL option selected, and leave the **Allow this app to request other SSO URLs** option blank

11\) ****Select the “EmailAddress” option for the **Name ID format** field and “Email” for **Application username**

![](https://lh5.googleusercontent.com/ST6zePvXisDMtHYsIFuI4tlIK1t7_aB9yK67cUALQiWhjGmGJVP9imux0Kh76trsWQRz11KXCVi7O9JDysn7dIA4tJH9egJslM5ow2ljdkmpr0mHk_qkm0V1QiK6AtglqOM5ZMh2)

12\) In the attributes section add an attribute so that there are two.  Enter “name” and “role” for the **Name** fields.  Leave the **Name format** fields as “Unspecified”.  In the **Value** fields enter [Okta Expression Language](https://developer.okta.com/docs/reference/okta-expression-language/) expressions that will provide the name and role for your UserLeap users.  The “role” field needs to evaluate to one of:  `admin` ,  `developer` ,  or  `viewer` . UserLeap roles are described [here](../product-workflows/account-creation-and-login.md). If you are not sure what to enter here you can add  `String.join(" ", user.firstName, user.lastName)` for “name” and  `admin`  for “role”

![](https://lh5.googleusercontent.com/3s6peu4ORVCCLDIn7ogmUIruDYDtyQX_HMrEzEac7aUKSNURQp001kH6vgPFrzXqdAuZ8j3mnA0EPg5Oar5IZFJt9ZuLh-6Mxi6Bg-_USUHwdkWBuCbjDbcTheuTd5n85-bRUmWo)

13\) Leave the **Group Attribute Statements** section blank. Scroll down to the bottom of the page and click the “Next” button

14\) Fill out the necessary fields in the **Feedback** section and click the “Finish” button

15\) You should now be taken to your new app’s integration page.  Click on the **Sign On** tab, and then click on the “View Setup Instructions” button

![](https://lh5.googleusercontent.com/vV07kjLCzI59IrJ-YxjzE9KhE--sEQIpLR8QvZjM3wxL82Y_EAfPlWBIiZ9HCeYBpVYEF2Pg7op0RNjRzVgFsXW4YATLdsZ7aZLo-YctifbZHm92R0R8vyrDGMFPA3OtrkUhldmq)

16\) A new page with configuration values will appear.  You will be using these values to configure UseLeap SSO in the next step

![](https://lh5.googleusercontent.com/CsThP1cVzRF1lVkyjXrLdESX-RE_PX8DHU-zKwdnouRRwPCkrCEeiw1Vp77pP1lmADcW55lUBA09LCcBVqmeux3uCUyZzGC1nfYsj9n-MiGkJFpCowfrAvCpmB1AlhGvSwxoqpZ-)

17\) Navigate to the UserLeap [SSO Settings Page](https://app.userleap.com/settings/sso).  Copy the values from the previous step into the corresponding fields in the “Your Identity Provider” section

* **Identity Provider Single Sign-On URL → Entry Point URL**
* **Identity Provider Issuer → Issuer URL**
* **X.509 Certificate → X.509 Certificate**

18\) Click the “Save” button in the **Your Identity Provider section**. Users that are assigned to the Okta app integration you created should now be able to sign up using the “Sign in with SSO” link in the UserLeap login page.  You can assign users in the Assignments tab of your Okta application integration

![](https://lh6.googleusercontent.com/SU_1DSygYIjDMQ5CqJ6sKfOR_aqIOnwHmZI5M9gMGTDmOG_6JSjVd6IzwKBYTS2HTkaDzS620C-Ok6p1OxowLbllDFwHkEhYRw9JDC_jF42HBDGR-xaMXh_9Z6eHeYZWMRO8ts0Z)

\*\*\*\*

