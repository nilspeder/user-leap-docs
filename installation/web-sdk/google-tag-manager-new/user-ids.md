# User Identification

## **Sending UserLeap UserIDs \(Optional, but Recommended\)**

_If you have any questions, please reach out to success@userleap.com or contact us via the in-product help chat_

UserLeap allows you to identify visitors by supplying a userId. While tracking UserIDs is optional,  it provides a consistent experience across platforms and prevents users from seeing the same survey multiple times. Here’s a quick overview of UserLeap’s [**survey eligibility**](../../../product-definitions/re-survey-windows.md) ****window

{% hint style="info" %}
 UserIds are unique, and the process will differ from client to client. This section is indicative of our own setup. For specific questions, please email **success@userleap.com** or reach out to us via the in-app product support  
{% endhint %}

## Custom JS Variable __

### **Step by Step**

Open  the "Variables" section, next select "New"

![](https://lh4.googleusercontent.com/dA6ZDxCy2CXC1mkTUlHFKsVdbkEHth05_LMOgqZ_yyxlSb5kKbvisWOFik1us_xfWznx646RqD1nq5dFCS64m-gAmslG3HX5EeiJli2uOJp7WSVmrlTS5aDaV3ZW-kd37mGV0gja)

![](https://lh6.googleusercontent.com/Udgq39Ev9z2Vjbl8NXe65_QA6gDAmWrGMK7J91nRbOttRUtXMtTLRj4jSa6v4Tk9kqAeUJGLQpfq0qumAUbO-28ZmDPjQu6_5UuI5AMpVRUG_I7l_bylOfnqxE1EOdkOUjC3PKUG)

_🚨At this step, you may require some assistance from a developer to determine what function/variable on your website/app stores and assigns user IDs_

Add a custom javascript variable 

![](../../../.gitbook/assets/image%20%2844%29.png)

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/12uKNlg5/Google%20Tag%20Manager:%20Custom%20JS%20Variable.jpg?v=dbb41d26199b41b3ed73d12747c3e031)

![](../../../.gitbook/assets/google-tag-manager-save-custom-js-.jpg)

Let's add a new trigger specifically for this new `UL_UserID` variable we just created

![](https://lh3.googleusercontent.com/WQDBBCNfekdIKUvgVWYcniOafUkqzFfV7N3OvyuvyMed4lVsjMFvnO06_sy1aIhfyzEe9UOSdKCHded6bCmrjTKmha3rlu13XxPfU3ozGeBqL7M4zTpCq9LcSoYnuAteSxqQWTs2)

![](../../../.gitbook/assets/image%20%2825%29.png)

We can call this trigger `UL_Overview Page & >0`

_Overview Page = URL on UserLeap where I want the app to send visitor userids for tracking_ 

_&gt;0 = Second criteria that MUST be met for the tag to fire. Only fire this tag, \`_`UL_UserID`_is NOT 0_

![](../../../.gitbook/assets/image%20%2810%29.png)

The trigger we create will be an `Page View` trigger

![](../../../.gitbook/assets/image%20%2863%29.png)

![](../../../.gitbook/assets/image%20%2821%29.png)

Remember, all triggers must be contained within a tag before we can deploy them. So next, we'll create another UserLeap tag - this one for `UL_UserID`

![](https://lh5.googleusercontent.com/nOj84q36GCtswZk7zvGLFcbY7xUzRBWFUEGBKLY_MjQ6UF3Sajm-LADrKTTlp058kCK0g0nIPJP06p8QtXb8RADatQfeW5vc-SN1tZHfLpi6r0jZGSo7exa3PPTEVE5ZOfvQD9R2)

![](https://lh6.googleusercontent.com/HIPG1DcHFNa_ae92-gG8Be7tG7XEUKA-mqBoVWm0f_wik0VJV6-MM_Zhcd7f7-oe8_jPZXr-G2nhl4NlsIzesZxy_6kfDrcMr0BVo8vdtXvrM53mglc10FDV_zIIAMyKjugMyo-Q)

Let's give the tag a title `UL_UserID` tag

![](https://lh5.googleusercontent.com/VlbEmdfb4FADmyi9kAznM7rPIri3JHxZqC1yRn2RasHj8c8MNM-3iXP7Bn6LgAVa2Sho-dsO4ttx3-D78xzg770al7IItgKu58oFa0No9qfdgeiuUFuSUPqpx7mp0FNx3DI9gAB6)

Now we’ll locate the UserLeap tag from the Google Tag Manager library and add our user ID variable \(`UL_UserID`\) along with our new `UL_Overview Page & >0` trigger 

![](../../../.gitbook/assets/image%20%286%29.png)

![](../../../.gitbook/assets/image%20%2826%29.png)

To add the `UL_EnvID` and `UL_UserID` you'll need to click on the respective 'lego-looking" icon in the image below. Add in the trigger as well. When finished, click "Save"

![](../../../.gitbook/assets/image%20%2860%29.png)

"Submit" your changes

![](https://lh5.googleusercontent.com/iOEVBSa4OTkjz6uZ9pbGcUarzoSgD9oPKT5GeiBntkWgVwfkIbRAZ7isKT43h83VfcHrJB81nYrFEKBaydRBVzzOgYsettzdqLjGa_AyzPolTHeSqfACbot8XUCGsL6BlATnQH8n)

