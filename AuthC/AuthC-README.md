
** AuthC Charter** 
* As stated in the [ANCR WG Charter ]([url](https://kantara.atlassian.net/wiki/spaces/WA/pages/2916522/Charter)) "Specify and Contribute:  AuthC Transparency Protocol for signalling authorisation with consent"

* Objective: specify the authC protocol so that it can be used as an extension to enable digital identity governance imteroperability, with regulated transparency and consent frameworks and architectures. 

**AuthC ANCR-SIG Scope of Works**
* Detail and specify - AuthC - Signaling Protocol 
* AuthC (standing for Authorisation from Consent)  is a Notice and Consent Receipt Exchange Signaling Protocol to enable transparency over digital privacy

**Deliverables**
Deliver core / generic authc flow for authorisation from consent covering 
* the core policy, the presentation, the lifecycle and the signaling for notice, notifications and disclosures
* the core technical protocold and flow
* project kit for extension
* Use Case :  OAuth Extension for Parental Consent Token Use Case - coon

**Outcomes Desired** 
* Active state transparency, security and data control
* enable dynamic data control 
The use of the AuthC proptocol to maintain a shared and active state of transparency between two parties (peer to peer) with a concentric mirrored notice record proptocol, enabling the individual to manage their own digital consent.   

Working to demonstate  a synchronic transparency signal through the method of differential transparency, which is the pratice of comparing reciepts, as a notification receipt is pulled from a PII Controller Notice Credential each session.  If there is no change to the active state then a green light signal is provided and the PII Principal user experience is seemless.   

**Challenges**
There are a number of well known challenges to digital security and privacy issues with decentralized digital identity management that are sovled for through the notarization of claims, to enable decentralised digital identity governance, with digital consent

* System Notice and consent context is constantly different, systems are not able to manage consent for people. 
* Give up privacy to access privacy service 
* No personal record of digital identity relationship that people can trust
* People are not easily able to admin their own consent, in any meaningful way
* Digital transparency over the impact of choices/what people consent too
* scalable delegation framework - as delegation is limited and cannot scale beyond scope of its own authority with out standard 

**components**
* Two Factor Consentric Notice
* Cntrl'r  Cred Registry for 4 types of credentials for 4 levels of assurance
* Cyber Notary - provding 2 roles - a) AUthenticate individual, and Controller, b)  Annotate the public ledger for a Service, 

***AuthC Identity Protocol Extension Use Case***
* applying the extension project kit to an identity management protocol

**OAuth**
* PAR - Push Authorisation Request
* RAR - Rich Authoritsation Request

**Proposed**
* PTR - Pull Transparency Credential Request, using 2FCN (Two Factor Concentric Notice) (sequence) as opposed to MFA, discover is through engagements, in which notice, notifications, are reqjuired, 

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
          
OPEN ID using TS-116 Can Digital Credential (being piloted by the SCC 2023/24)  to publish/produce an example

**References**
[Transparency Peformance Indicators v0.6](TPI/ANCR-TPI-Conformity Specefication v0.6.docx)  - ANCR GIT 

DIACC SiG, digital governance interoperabilty for wallets, produced - [Adequacy]([url](https://diacc.ca/2022/03/31/adequacy-of-identity-governance-transparency/)) "[adequacy-of-identity-governance-transparency](adequacy-of-identity-governance-transparency)" AuthC: Transparency and Consent, notice, notification and disclosure requirements, reviewed against frameworks.   Proposed as notice elemenets that can be  notarized with a certified Digital Privacy/Surveillance Officer/Operator Credential, 

"Editorial Note: Currently in digital identity management the  Authorization Server Obtains End-User Consent/Authorization
Once the End-User is authenticated. As an alternative AuthC presents a notice signalling protocol  extension for the notice points references in the DIACC paper, according to context, and levels of Transparency Risk Assurance required to manage liability to mitigate risks, and enable a much more robust and dynamic trust between parties, not possible to scale without an internatioanlly decentralized digital governance, co-regulatory model (suitable to scale consent online)." 

*Extendsion References* OpenID Reference for extension: *Authorization Server Obtains End-User Consent/Authorization*
Once the End-User is authenticated, the Authorization Server MUST obtain an authorization decision before releasing information to the Relying Party. When permitted by the request parameters used, this MAY be done through an interactive dialogue with the End-User that makes it clear what is being consented to or by establishing consent via conditions for processing the request or other means (for example, via previous administrative consent). Sections 2 and 5.3 describe information release mechanisms.
https://openid.net/specs/openid-connect-core-1_0.html#Consent

**Background Reference Surveillance Trust Use Case**
[Towards A Framework Of Contextual Integrity
Legality, trust and compliance of CCTV signage]([url](https://www.taylorfrancis.com/chapters/edit/10.4324/9780203141625-23/towards-framework-contextual-integrity-mark-lizar-gary-potter))
By Mark Lizar, Gary Potter  Book Eyes Everywhere Edition1st Edition, First Published2011 Imprint Routledge, Pages14 eBook ISBN9780203141625 https://www.taylorfrancis.com/chapters/edit/10.4324/9780203141625-23/towards-framework-contextual-integrity-mark-lizar-gary-potter


**Glossary**
[ANCR Record Framework Specification]([url](https://kantara.atlassian.net/wiki/spaces/WA/pages/114098237/ANCR+Record+Framework+for+PII+Credentials)) references, inlclude 3 cross referenced mappings for those terms, via CoE 108+, GDPR, and ISO/IEC 29100,  



