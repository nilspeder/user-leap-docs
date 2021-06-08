# Base Install

## Installing UserLeap Javascript

_If you have any questions, please reach out to success@userleap.com or contact us via the in-product help chat_

To install the UserLeap codebase, you’ll need to do these two things:

1. Create an environment ID variable and add it to Google Tag Manager
2. Create a tag that consists of your environment ID variable and a trigger \(default to all page views

### 1\) Create an Environment ID Variable

_if you're unsure of where to find the environment ID,_ [_click here_ ]()\_\_

{% embed url="https://share.getcloudapp.com/QwublXo2" caption="Creating an Environment ID Variable" %}

### **Step by Step**

Open up the “Variables” section of Google Tag Manager

![](https://lh5.googleusercontent.com/eFUvQFELqk6Qtx6lLP6flalsyGiKQrqWtLRRhNhC2_A6oLhOCSMvzT9sm0I4UWkKH-sQrPt9N4cQkDf4yLPKapf65Ql_fR25OBORlDXE2ZrzJ7_qC6jUKz8wEu2iJQ-P4PNzmbh3)

Create a new user-defined variable

![](https://lh6.googleusercontent.com/Udgq39Ev9z2Vjbl8NXe65_QA6gDAmWrGMK7J91nRbOttRUtXMtTLRj4jSa6v4Tk9kqAeUJGLQpfq0qumAUbO-28ZmDPjQu6_5UuI5AMpVRUG_I7l_bylOfnqxE1EOdkOUjC3PKUG)

We’ll name this new variable `UL_EnvID (Production)` and make this a constant variable type

![](https://lh3.googleusercontent.com/sv4fzttKzHOJxDw7D7gQuMGM30PWkHAXw1-RIj1yoG8K9dftAHrVXtmCNJ8ug_K0h-ukdg20wdP-rF_3MvyUZcs1f5jGjF5BBkoJbFKP1LkrvgHdVMTe9r3EErNV-vux5kg2v7_A)

Please add your UserLeap environment ID below and then click “Save"

![](https://lh5.googleusercontent.com/gOp_Ne7LiE1leVAQAVS0X3FNaSazcnUSO-6UYG7Gji5suUoEJz-rLktcCoUwKlLYPD_uSWiS4OrA6-tWCvT3kzGpTMeFc_Nfblu_c6DgPYFmGNF3Zh_o4OjvqJcf_Fxs8JTP3coF)

### **2\) Creating the UserLeap Installation Tag**

Now that we have the environment ID and the trigger \(`All Pages` - in GTM by default\), we can put it all together inside a tag. UserLeap supplies its own custom tag template which can be found in the tag library.

{% embed url="https://share.getcloudapp.com/L1uOpyL2" %}

### **Step by Step**

Click “Tags” and then click on “New” 

![](https://lh5.googleusercontent.com/nOj84q36GCtswZk7zvGLFcbY7xUzRBWFUEGBKLY_MjQ6UF3Sajm-LADrKTTlp058kCK0g0nIPJP06p8QtXb8RADatQfeW5vc-SN1tZHfLpi6r0jZGSo7exa3PPTEVE5ZOfvQD9R2)

![](https://lh6.googleusercontent.com/HIPG1DcHFNa_ae92-gG8Be7tG7XEUKA-mqBoVWm0f_wik0VJV6-MM_Zhcd7f7-oe8_jPZXr-G2nhl4NlsIzesZxy_6kfDrcMr0BVo8vdtXvrM53mglc10FDV_zIIAMyKjugMyo-Q)

Let's give the tag a title 

![](https://lh5.googleusercontent.com/VlbEmdfb4FADmyi9kAznM7rPIri3JHxZqC1yRn2RasHj8c8MNM-3iXP7Bn6LgAVa2Sho-dsO4ttx3-D78xzg770al7IItgKu58oFa0No9qfdgeiuUFuSUPqpx7mp0FNx3DI9gAB6)

Now we’ll locate the UserLeap tag from the Google Tag Manager library and add our environment ID variable \(`UL_EnvID`\) along with the `All Pages`trigger \(there by default\)

![](../../../.gitbook/assets/image%20%286%29.png)

![](../../../.gitbook/assets/image%20%2826%29.png)

To locate the `UL_EnvID` variable we just created, you'll want to click on the "lego-looking" icon in the "Environment ID" field below. Once finished, click on the triggering portion for us to add our `All Pages` trigger

![](../../../.gitbook/assets/image%20%2828%29.png)

![](../../../.gitbook/assets/image%20%2842%29.png)

Once you've added the trigger, click save in the top right 

![](../../../.gitbook/assets/image.png)

Finally, we'll submit all our changes. Congrats! You have now installed UserLeap across your webpage/web-based application

![](https://lh5.googleusercontent.com/iOEVBSa4OTkjz6uZ9pbGcUarzoSgD9oPKT5GeiBntkWgVwfkIbRAZ7isKT43h83VfcHrJB81nYrFEKBaydRBVzzOgYsettzdqLjGa_AyzPolTHeSqfACbot8XUCGsL6BlATnQH8n)

