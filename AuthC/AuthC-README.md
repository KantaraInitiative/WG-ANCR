**AuthC**

Proposposed Scope (in draft)

There are a number of well known challenges to digital security and privacy issues with decentralized digital identity management that are sovled for by decentralizing digital identity governance.  

**Challenges**
* System Notice and consent context is constantly different, systems are not able to manage consent for people. 


**Currently in OAuth**
PAR - Push Authorisation Request
RAR - Rich Authoritsation Request

**Proposed**
Pull Authorization Request to start the flow


**Solution Architecture**
1. Notice&Consent Token Generator in the wallet 
2. Consent Token Relying Party which separate 
    1. Security architecture 
        1. Non National - Cloud Security Risks
            1. Data sovereignty - 
            2. Secure by design 
            3. Consent by design 

**References**
Currently in digital identity management the  Authorization Server Obtains End-User Consent/Authorization
Once the End-User is authenticated, 

*Authorization Server Obtains End-User Consent/Authorization*
Once the End-User is authenticated, the Authorization Server MUST obtain an authorization decision before releasing information to the Relying Party. When permitted by the request parameters used, this MAY be done through an interactive dialogue with the End-User that makes it clear what is being consented to or by establishing consent via conditions for processing the request or other means (for example, via previous administrative consent). Sections 2 and 5.3 describe information release mechanisms.
https://openid.net/specs/openid-connect-core-1_0.html#Consent

**Glossary**




