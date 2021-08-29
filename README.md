# abap_oauthdemo
ABAP GitHub Demo

Accessing SuccessFactors OData APIs using the OAuth 2.0 Client 

With the sunset (planned retirement) of HTTP Basic Authentication for API Calls (SFAPI and OData), one of the recommended alternative approaches is to use OAuth2 SAML Bearer Assertion. 
OAuth 2.0 client handles the storing of OAuth 2.0 tokens and client secrets in the secure store.
During the authentication, OAuth 2.0 client passes the OAuth 2.0 scopes to the service provider which contains references to all the allowed resources.

This scenario involves accessing SuccessFactors OData APIs to create/update Employee and Employment details in the SuccessFactors Employee Central Instance by using the existing Employee and Employment details from SAP ERP HCM System using an ABAP Program that uses OAuth 2.0 Client APIs together with the OAuth 2.0 Authentication mechanisms.

We need to set up certain configurations on both Client (ABAP AS) and Server (SuccessFactors) side.

Below are the list of prerequisites:

* The system administrator needs to have authorizations to create certain configurations involving Certificates using STRUST tcode.
* The system administrator needs to have authorizations to create OAuth 2.0 Client Configurations. Make sure that User has the authorization S_OA2C_ADM with at least the activities 01, 02 and 03 in the AS ABAP system.
* Make sure that the end users who should be allowed to use the new OAuth 2.0 Client have the required authorizations assigned. During execution of OAuth 2.0 flows there is a check of the authorization object “S_OA2C_USE”. This authorization object has two fields “PROFILE” and “ACTVT”.One needs to set the authorization field values as follows: S_OA2C_USE PROFILE = OAuth 2.0 Client Profile name ACTVT = 16





