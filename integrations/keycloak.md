# KeyCloak

1\) Contact [sso@userleap.com](mailto:sso@userleap.com) to claim the email domain\(s\) that your SSO users will use to sign in.

2\) Log into your UserLeap account and navigate to the [SSO Settings Page](https://app.userleap.com/settings/sso).

3\) Select the “SSO Enabled” option, and click “Save”.

4\) An “Important Values” section should appear. Copy the value of the Entity URI field into the Issuer URL field in the “Your Identity Provider”, and click the “Save” button for both sections. Take note of both values provided by the “Important Values” section, as you will use it in your KeyCloak client configuration in the next step.

5\) Log into your KeyCloak administration console. Navigate to the Clients page. Click the “Create” button and an “Add Client” page should appear. In the “Add Client” page enter the Entity URI from step 4 into the Client ID field, and select “saml” for the Client Protocol.  Click “Save”.

6\) A new configuration page for the newly created UserLeap client should appear. Click on the Settings tab. Switch the Enabled and Sign Document toggles to the “ON” position. All other toggles should be “OFF”. Select “RSA\_256” for the Signature Algorithm, and enter the ACS URL from step 4 into the Valid Redirect URIs field. The values of all other fields can be as the default value or blank. Click the “Save” button at the bottom.

7\) Click on the Mappers tab for the UserLeap client you created. Add two mappers that will evaluate to the values that will be used by the UserLeap application for each user’s name and role. The SAML attribute names must be “name” and “role”, respectively.  Name values must be less than 255 characters, and valid values for role are “admin”, “developer”, or “viewer”. UserLeap roles are described [here](https://help.userleap.com/invite-teammates).

8\) Click on the Realm Settings tab on the left. Click on the Keys tab in the Realm page under which your UserLeap client was created. In that page under the Active tab you should see a set of rows for each key. Find the one that has type “RSA” and click on the “Certificate” button on the right side of the row. A long string value should appear. Enter this value into the X.509 Certificate field in the “Your Identity Provider” section of the UserLeap [SSO Settings Page](https://app-staging.userleap.com/settings/sso). Click “Save”.

Users properly configured to use the UserLeap client you configured in KeyCloak should now be able to sign in using the UserLeap [SSO login page](https://app.userleap.com/login/sso).

