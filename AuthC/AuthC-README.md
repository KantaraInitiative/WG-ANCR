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
* PAR - Push Authorisation Request
* RAR - Rich Authoritsation Request

**Proposed**
* PTR - Pull Transparency Request 

PTR to start the authorization flow, generating a notice receipt from PII Controller credential generating a proof of notice claim. Using this digital credential to return claims, along with standardized digital notice and consent.  In this way enabling the PII Principle to be an issuer,  to enable trust, through control and the ability to dynamically provide and manage consent in and by context.   

**Method**
- make a baseline profile for adequacy,  CoE 108+ Art 14 as Code of Conduct
- compare trasnaprency profiles against what is adequate for compliance assessments framework

**Solution Architecture**
1. Notice&Consent Token Generator in the wallet 
2. Regulated, Consent Token Exchange &  Relying Party  
    1. Security architecture 
        1. Non National - Cloud Security Risks
            1. Data sovereignty - 
            2. Secure by design 
            3. Consent by design
          
OPEN ID using TS-116 Can Digital Credential (being piloted by the SCC this summer)  to publish/produce an example

**References**
DIACC SiG, digital governance interoperabilty for wallets, produced - "[adequacy-of-identity-governance-transparency](adequacy-of-identity-governance-transparency)" AuthC: Transparency and Consent, notice, notification and disclosure requirements, reviewed against frameworks.  

Currently in digital identity management the  Authorization Server Obtains End-User Consent/Authorization
Once the End-User is authenticated, this proposes an extension for these notice points, for


OpenID Reference for extension: *Authorization Server Obtains End-User Consent/Authorization*
Once the End-User is authenticated, the Authorization Server MUST obtain an authorization decision before releasing information to the Relying Party. When permitted by the request parameters used, this MAY be done through an interactive dialogue with the End-User that makes it clear what is being consented to or by establishing consent via conditions for processing the request or other means (for example, via previous administrative consent). Sections 2 and 5.3 describe information release mechanisms.
https://openid.net/specs/openid-connect-core-1_0.html#Consent

Background Research Reference
[Towards A Framework Of Contextual Integrity
Legality, trust and compliance of CCTV signage]([url](https://www.taylorfrancis.com/chapters/edit/10.4324/9780203141625-23/towards-framework-contextual-integrity-mark-lizar-gary-potter))
By Mark Lizar, Gary Potter  Book Eyes Everywhere Edition1st Edition, First Published2011 Imprint Routledge, Pages14 eBook ISBN9780203141625


**Glossary**




