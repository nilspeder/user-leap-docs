# Websites & Web Applications

There are many ways that UserLeap can help you to conduct user research via your websites and web applications. To get started, we’re going to outline the two easiest ways which are either through our [Javascript code snippet](../installation/web-sdk/javascript-sdk.md) or integration with[ Google Tag Manager](../installation/web-sdk/google-tag-manager-new/). 

Getting started with UserLeap is easy! Oftentimes a UserLeap base implementation takes as little as 30 mins. Of course, this varies from customer to customer and really depends on the availability and the complexity of your research needs.

## Tasks

1. [Deploy UserLeap JavaScript snippet or Google Tag Manager](websites-and-web-applications.md#task-1-deploy-userleap-javascript-snippet-or-google-tag-manager)
2. [Add No Code Event](websites-and-web-applications.md#task-2-add-a-no-code-event)
3. [Choose a Template](websites-and-web-applications.md#task-3-choose-a-template) 
4. [Design Questions & Audience](websites-and-web-applications.md#task-3-choose-a-template) 
5. [Launch Microsurvey](websites-and-web-applications.md#task-5-launch-microsurvey) 

## Task 1. Deploy UserLeap JavaScript snippet or Google Tag Manager

UserLeap provides both a web SDK via Javascript and a Google Tag Manager integration that lets your website or web application recognize customer interactions on your web and application pages. These interactions are referred to as “events” for UserLeap. We’ve provided a list of considerations to decide which installation option is right for you:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Considerations</th>
      <th style="text-align:left">UserLeap Web SDK</th>
      <th style="text-align:left">UserLeap Google Tag Manager Integration</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Availability</b>
      </td>
      <td style="text-align:left">
        <p>&lt;b&gt;&lt;/b&gt;</p>
        <ul>
          <li>Web SDK Environment IDs are available from the UserLeap Account</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>Likely already installed on your website</li>
          <li>Easy to add UserLeap to your GTM container</li>
          <li>Environment IDs are available from the UserLeap Account</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Skillset, Access &amp; Permissions</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>Knowledge, permission &amp; access of your codebase and repository</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>Novice to basic Google Tag Manager knowledge</li>
          <li>Permission to GTM</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Capacity</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>30 minutes</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>30 minutes</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Website or Web App Surface Area</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>Easy to install on both surface areas</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>Often already installed on your marketing site and possibly part of your
            application if the application is hybrid</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

Below are the most basic steps for installing UserLeap’s SDK via Javascript or the Google Tag Manager integration. A more detailed description of installation and configuration options can be located in the installation guide section of these documents.

1. Add a team member
   1. Identify a colleague who has access to your code base and code repositories
   2. In the “Navigation Pane”, click “Settings”.
   3. Click “Team”
   4. Click “Add Member”
   5. Enter their first and last name, plus email address and assign them the developer role
   6. Click “Save”
2. Request that the JavaScript snippet be installed or that Google Tag Manager add UserLeap to its deployment
   1. In the “Navigation Pane”, click “[Connect](https://app.userleap.com/connect)”.
   2. Click JavaScript or Google Tag Manager so you can provide the information to your colleague.
   3. Using the sample copy below, email or message your colleague asking them to install the snippet on your website or web application

```text
Hi there - 

Can you find 30 minutes to accept the UserLeap invite that I 
sent you and install the [JavaScript snippet or Google Tag Manager]? 

The invite was sent via your email address from UserLeap. 

Once you’ve accepted the invite, the snippet is described here in this link under 
https://app.userleap.com/connect 
on the card at the top. 

Make note that you'll need the Environment IDs contained there. 

If you need any help, you can contact the UserLeap Customer Success team
https://docs.userleap.com/userleap-support

Thank you, 

[Your Name] 

```

If you need any help with either of the deployment, please reach out or book time with our [Product Support and Customer Success](../userleap-support/) teams. We’re happy to lend you a hand getting started!

## Task 2. Add a No Code Event

Your website or web application has many pages, buttons, and interactions with UI elements that can be tracked as an event and recognized by UserLeap in order to conduct **In Product** Research. 

To get started, once you’re clear on what you would like to research you’ll need to spend time in your website or web application to determine which page or what button you’d like  your microsurvey to trigger on in order to collect user insights. 

Your pages, buttons, interactions on the UI and style sheet definitions translate to concepts in UserLeap and are considered to be part of UserLeap’s "No Code" events. ****

1. Choose a page or a button in your website or web application.
2. Keep that page open as you navigate to the next step; you're going to need to copy information from this page into the UserLeap application. 
3. Open the UserLeap application 
4. In the Navigation Pane, click  “[Events](https://app.userleap.com/events)” .
5. Click “Add” 
6. Click “No Code Event”
7. Click “Page URL” for a trigger based on page loading or “Inner Text” for a trigger based on a button, link or UI element event in the page
8. In the Name field, enter the Event name
9. In the Description field, enter the Event description.
10. If Page URL was clicked, in the URL Pattern field, enter the Page URL.
11. If InnerText was clicked, in the Inner Text field, enter the inner text of the element..
12. Click “Save”. 

This event is now available for both immediate and future use within your microsurveys.

## Task 3. Choose a Template 

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

## Task 4. Design Questions & Audience 

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

1. Choose “Web” as the platform
2. Under the “Survey Trigger”, choose the “No Code Event” that you added in the step above
   1. Select the dropdown to search and choose the correct event for your mobile microsurvey. 
3. Add a filter in your microsurvey to refine the target audience that should receive your microsurvey. Similar to your survey trigger, select an event or attribute to segment your eligible users for this microsurvery. 
4. Click “Save Changes”
   1. Saving the changes of your microsurvey places it into a status called Draft. 

To learn more about designing microsurvey questions, visit the following topics: 

* Total Responses 
* Resurvey Options 

## Task 5. Launch Microsurvey

1. Click the purple “Launch Survey” button in the top right corner, you should start to see responses come in as time progresses.

If you need any help with either of these installations, please reach out or book time with our [Product Support and Customer Success teams](../userleap-support/). We’re happy to lend you a hand getting started. ****

{% page-ref page="responses-and-insights.md" %}

## FAQ  

