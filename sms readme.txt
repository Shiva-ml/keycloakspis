Name of the SPI
---------------------------
mobile-number-authenticator


Purpose of the SPI
-----------------------
Current keycloak architecture supports MFA using mobile authenticators like google authenticator, Microsoft authenticators etc. But it does not SMS based authentication. A custom SPI has been developed to meet this criteria.

Approach
------------------

1. Develop a custom mobile Authenticator SPI which will fetch mobile number from the user attributes, generates a OTP and sends it as a SMS to user's mobile number.

2. Provide a option to set Configurations like OTP length, time-to-live, api-url which will send SMS and other API details via UI in key cloak.  



Classes used
----------------------
Authenticator, Authenticator Factory


Setup
--------------------
1. create a realm
2.  go to realm settings >user profile and  add a user attribute "mobile" and set its display name to "${mobile}".
3. go to authentication tab and duplicate browser setting. 
4. go to browser form and add step "sms-authentication (2FA)" and set it to required.
5. make sure its right below username password form.
6. go to settings tab of the spi and provide a alias name for it and all other details related to api and sms. (enable simulation mode if you are testing the flow)
7. bind flow with the broswer flow and enable it. 


usage
---------------
1. login in the custom realm by providing username password.
2. keycloak sends sms to the stored mobile number and pops up a form asking to ente otp.
3. enter the correct otp to get authenticated. 


 

 