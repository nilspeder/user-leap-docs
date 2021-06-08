# FAQs

## **Do you minify the JavaScript snippet?**

Yes, the script is fully minified to keep the bundle as small as possible and load times as short as possible.

## Do you use a framework for the Javascript snippet and will it interfere with my code?

The snippet is vanilla javascript and designed to not pollute the window or javascript default behavior. The widget itself is built using the tiny and fast [hyperapp](http://t.sidekickopen24.com/e1t/c/5/f18dQhb0S7lM8dDMPbW2n0x6l2B9nMJN7t5X-FfhMynN4XXHP2dV8NWW56dxVL4c2Pyv102?t=https%3A%2F%2Fgithub.com%2Fhyperapp%2Fhyperapp&si=7000000001348012&pi=4d965cfd-30bc-48ba-9122-bd342a321f79) framework. 

An iframe is used for the loading and display of the microsurveys, which keeps the two environments isolated. The exception to this is the `window.UserLeap` object, which you’ll create explicitly when you paste in the snippet. Any actions you are meant to access as part of the integration will be accessible from this object after initialization.

## If I use Intercom for chat, will they overlap?

UserLeap's microsurveys appear to only a small sample of your user base \(often less than 3%\).

In the cases where you want to show a survey to your user when you have the Intercom iframe on your website, the UserLeap web sdk will detect if Intercom is initialized \(by checking window.Intercom\) and if it is then we call Intercom's public API `hide_default_launcher` to hide Intercom's iframe. Once the survey has been completed or when a user closes the survey prompt, we will show Intercom again. This provides a seamless experience for your users.

## Do you offer CSAT/NPS?

We do. The "Measure Customer Satisfaction \(CSAT\)" survey template is available under the "Retention and Churn" template collection, located on the [Templates Page](https://app.userleap.com/collections). NPS is offered as one of our native question types, and can be added to any survey.

