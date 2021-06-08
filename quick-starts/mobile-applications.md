# Mobile Applications

To install UserLeap on your mobile application, you and your team may choose iOS, Android and React Native. For a simple mobile install, most teams can complete this work in 1 to 4 hours. 

## Tasks

1. [Deploy & Initialize a UserLeap Mobile SDK ](mobile-applications.md#task-1-connect-and-initialize-a-userleap-mobile-sdk)
2. [Set the User Identity & Attributes ](mobile-applications.md#task-2-set-the-user-identity-and-attributes)
3. [Track & Add an Event ](mobile-applications.md#task-3-track-and-add-an-event)
4. [Choose a Template](mobile-applications.md#task-4-choose-a-template) 
5. [Design Questions & Audience](mobile-applications.md#task-5-design-questions-and-audience) 
6. [Launch Microsurvey](mobile-applications.md#task-6-launch-microsurvey)

## Task 1. Deploy & Initialize a UserLeap Mobile SDK 

UserLeap provides [iOS, Android and React Native SDKs](). Choose the SDK based on your engineering team’s preferences. 

1. Partner with engineering to choose your Mobile SDK.
2. Install the Mobile SDK on your product’s mobile application.
   1. Add a team member
      1. Identify a colleague who has access to your code base and code repositories
      2. In the “Navigation Pane”, click “Settings”.
      3. Click “Team”
      4. Click “Add Member”
      5. Enter their first and last name, plus email address and assign them the developer role
      6. Click “Save”
   2. Request from your engineering team that the Mobile SDK be installed.
      1. Initialize the module first by accessing the [Connect](https://app.userleap.com/connect) tab and copying the Production Environment ID from the correct operating system overview card.
      2. Compose the following message: 

```text
Hi there - can you find 90 minutes to accept the UserLeap invite that I sent you 
and install the UserLeap Mobile SDK?

The invite was sent via your email address from UserLeap. 
Once you’ve accepted the invite, the snippet is described here in this link under 
https://app.userleap.com/connect on the card at the top. 

Make note that you'll need the Environment IDs contained there. 

If you need any help, you can contact the UserLeap Customer Success team
https://docs.userleap.com/userleap-support


Thank you,

[Your Name] 
```

## Task 2. Set the User Identity & Attributes 

1. For any user attributes accessible from within your mobile application, partner with your engineering team to identify the user ID and/or email address and pass along any additional user attributes to UserLeap via the Mobile SDK.
   1. UserLeap automatically tracks and attaches the following attributes:
      1. App version
      2. iOS/Android version
      3. SDK version
      4. Device type
      5. System language

## Task 3. Track & Add an Event

1. Verify with your engineering team that they have configured the events and attributes to track in your production mobile application
   1. Please note that UserLeap has implemented an auto-accept mechanism within the Mobile SDK that allows a call of UserLeap.track\("YOUR\_TRACKING\_EVENT"\) to instantiate the event. 
      1. Once your Engineering team has enabled that name for the event, it becomes available to you in the UI when designing the Microsurvey to Trigger the microsurvey. Thus as long as that's enabled a survey designer shouldn't have to manually create it. 
      2. Alternatively a survey designer can "Add an Event" via the UI and choose "Code" to name an event, then share that name with their engineer to have them instantiate the event UserLeap.track\("YOUR\_TRACKING\_EVENT"\)
      3. If you need help managing this workflow between team members, download this product team Microsurvey, Event & Attribute Tracker or contact [Customer Success](../userleap-support/)
   2. Make a note of a particular event in your mobile app and its name as you will need it later when you define your audience in the microsurvey.
   3. In the Navigation Pane, click [Events](https://app.userleap.com/events) and locate the event that they defined 
   4. The green Daily Usage icon shows that UserLeap is tracking that event. Hold the pointer over the icon to view the event throughput. 
   5. You are now ready to begin designing your microsurvey

## Task 4. Choose a Template

Navigate to the "[Templates](https://app.userleap.com/collections)" section within your account to browse expert written microsurvey templates. Templates are organized into use case collections to help you easily find what you need, like:

* Onboard More Customers
* Create Better Content
* Launch a New Product or Feature
* Recruit Interview Participants
* Reduce Customer Churn
* & more!

Choose the collection that best fits your business problem. Then browse, preview, and select the template that best supports your research.

1. Scan and hover over each template.
2. Observe the preview on the right side.
3. To choose the template, either select the template card or click the green "Customize and Launch" button on the right, under the preview of the template.
4. If you'd rather not use a template, you can always choose to "Create from Scratch" via the purple button in top right corner to create your custom survey.

## Task 5. Design Questions & Audience 

**For the Question selection:** 

1. Review the questions
2. Customize by changing the wording, deleting a question or adding a question. 
3. Click “Save Changes” after customizing
   1. Saving the changes of your microsuvery places it into a status called Draft. 

To learn more about designing microsurvey questions, visit the following topics: 

* Skip Logic
* Default Text
* Thank You Card

**For the Audience selection:** 

1. Choose “Mobile” as the platform
2. Under the “Survey Trigger”, choose the event that you added in the step above in partnership with your engineering team.
   1. Select the dropdown to search and choose the correct event for your mobile microsurvey. 
3. Add a filter in your microsurvey to refine the target audience that should receive your microsurvey. Similar to your survey trigger, select an event or attribute to segment your eligible users for this microsurvery. 
4. Click “Save Changes”
   1. Saving the changes of your microsurvey places it into a status called Draft. 

To learn more about designing microsurvey questions, visit the following topics: 

* Total Responses 
* Resurvey Options 

## Task 6. Launch Microsurvey

1. Click the purple “Launch Survey” button in the top right corner, to view responses as your audience completes the microsurvey

If you need any help with either of these installations, please reach out or book time with our [Product Support and Customer Success teams](../userleap-support/). We’re happy to lend you a hand getting started. ****

{% page-ref page="responses-and-insights.md" %}

## FAQ 

  


