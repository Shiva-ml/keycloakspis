Name of the SPI
---------------------------
pin-val-authenticator

Purpose of the SPI
-----------------------
 A custom SPI has been developed to validate user entered PIN with a mock service.

Approach
------------------

1. Develop a custom pin validator SPI which will validate user entered pin during authentication with mock service.



Classes used
----------------------
Authenticator, Authenticator Factory


Setup
--------------------
1. create a realm
2. go to authentication tab and duplicate browser setting. 
3. go to browser form and add step "PIN based authenticator" and set it to required.
5. make sure its below username password form.
7. bind flow with the browser flow and enable it.
6. run the mock service.


usage
---------------
1. login in the custom realm by providing username password.
2. keycloak pops up a form asking to enter pin.
3. the entered pin is validated with mock service. access is provided if details are correct.


 

 