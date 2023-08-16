**AuthC Scope**
*AuthC - Notice and Consent Receipt Exchange Protocol for authorisation from consent*

The objective of the AuthC proptocol is to maintain an active state of transparency between two parties with a concentric mirrored notice record proptocol, enabling the individual to manage their own digital consent.   

As a recult the AuthC protocol aims to achieve a synchronic transparency signal through the method of differential transparency, which is the pratice of comparing reciepts, as a notification receipt is pulled from a PII Controller Notice Credential each session.  If there is no change to the active state then a green light signal is provided and the PII Principal user experience is seemless.   

There are a number of well known challenges to digital security and privacy issues with decentralized digital identity management that are sovled for through the notarization of claims, to enable decentralised digital identity governance, with digital consent.  

**Challenges**
* System Notice and consent context is constantly different, systems are not able to manage consent for people. 
* Give up privacy to access privacy service 
* No personal record of digital identity relationship that people can trust
* People are not easily able to admin their own consent, in any meaningful way
* Digital transparency over the impact of choices/what people consent too 

**Currently in OAuth**
PAR - Push Authorisation Request
RAR - Rich Authoritsation Request

**Proposed**
PTR - Pull Transparency Request 
to begin the flow - generating a notice receipt from PII Controller credential generating a proof of notice claim. Using this digital credential to return claims, along with standardized digital notice and consent.  In this way enabling the PII Principle to be an issuer,  to enable trust, through control and the ability to dynamically provide and manage consent in and by context.   


**Solution Architecture**
1. Notice&Consent Token Generator in the wallet 
2. Consent Token Exchange Relying Party separate 
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




