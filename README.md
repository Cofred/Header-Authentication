# Header-Authentication Process for API Authentication

# Overview

This document describes how a third-party will request for an Cofred  Services. All our APIs require users to be authenticated before they can access any of our resources.


 We authenticate every call to our resources using a combination of HTTP headers. These HTTP Headers must be sent for every call in other to access Cofred resources. Note that all data formats and response definitions are in conformance with the REST standard.
Authentication

 In order to do authentication, you will be required to send the following HTTP headers parameters: Merchant ID, Secret Code, Terminal ID, Access Token and Timestamp. Also, you will be required to send an Authorization HTTP header parameter.

All fields are required except otherwise stated.

HTTP Headers for Authentication 

The following describes the important headers required to be sent.

#	Headers		Description

1	Merchant ID	Mandatory	You need to provide Merchant ID as                  shown in app details. Input merchant ID should be base64 Encoded.

2	Secret Code	Mandatory	You need to provide Secret Code as                  shown in app details. Secret Code should be 35 alphaNumeric characters.

3	Terminal ID	Mandatory	You need to provide Terminal ID shown in app details. Terminal ID should be 5 alphaNumeric characters.

4	Access Token	Mandatory	You need to provide Access Token as                  shown in app details. Input Access Token should be base64 Encoded.

5	Timestamp	Mandatory	Request timestamp in epoch (unix). It must be in seconds and NOT milliseconds.

e.g. 1505591640

Note: Timestamp should not old more than 5 Minutes.

6	Content-Type	Pre-Defined	The MIME type of the body of the request e.g. application/json

You can get your created App list visiting below url after logging to your Cofred website.

https://cofred.com/secure/app/merchant/apps

Sample Authentication Headers


merchant_id: VFdCMTY3WURPZUpJdkNnVWJWRXE=   // Base64 Encoded

secret_code: I8AtLUljNqcdS4F76OVy2Zf1bJvGwsP95rE

terminal_id: YINCU

access_token: dUp4dEtybVg0UmpmMEFT  // Base64 Encoded

timestamp: 1505628722
