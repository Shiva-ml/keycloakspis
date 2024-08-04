Name of the SPI
---------------------------
otp-grant-spi



Purpose of the SPI
-----------------------
Current architecture in key cloak does not support generating access tokens for users who have not registered in key cloak or LDAP. A custom spi has been developed to meet this criteria while making sure that sessions are registered,visible and audited.

Approach
------------------

Develop a custom user storage provider SPI which will take mobile number and OTP in place of username and password and validate it against a mock service to provide access tokens.


Classes used
----------------------
UserStorageProvider, UserLookupProvider, UserQueryProvider, CredentialInputValidator, AbstractUserAdapter


Setup
--------------------
1. create a realm
2. add the custom provider in user federation section
3. run the mock service

usage
---------------
login in the custom realm by providing mobile number and otp in place of username and password to authenticate and get access token .


 

 