**ANCR-WG - Reference Draft v0.5 (TPIs)**

Editors: Sharon Polsky, Mark Lizar

Chair: Sal D'Agostino

Contributors:

**IPR Option:**

This ANCR Record Specification is available for use for public benefit licensing @0PN C.I.C and the open schema available @Human Colossus, and is specified under a Reasonable and Non‑Discriminatory (RAND) agreement at the Kantara Initiative for submission to ISO/IEC SC 27 WG 5

Published for use as public infrastructure through code of conduct and practice in industry and trade certification bodies.

Patent & Copyright: Reciprocal Royalty Free with Opt-out to Reasonable and Nondiscriminatory (RAND)

**Suggested Citation: (upon WG approval)**

ANCR Specification v0.5

# NOTICE

This document has been prepared by participants of Kantara Initiative Inc. Permission is hereby granted to use the document solely for the purpose of implementing the Specification. No rights are granted to prepare derivative works of this Specification. Entities seeking permission to reproduce this document, in whole or in part, for other uses must contact the Kantara Initiative to determine whether an appropriate license for such use is available.

Implementation or use of certain elements of this document may require licenses under third party intellectual property rights, including without limitation, patent rights. The Participants and any other contributors to the Specification are not and shall not be held responsible in any manner for identifying or failing to identify any or all such third-party intellectual property rights. This Specification is provided "AS IS," and no Participant in Kantara Initiative makes any warranty of any kind, expressed or implied, including any implied warranties of merchantability, non-infringement of third-party intellectual property rights, or fitness for a particular purpose. Implementers of this Specification are advised to review Kantara Initiative's website ( ![](RackMultipart20230814-1-ayl9sl_html_3a12e50f4396a04.png)[Kantara Initiative: Trust through ID Assurance](http://www.kantarainitiative.org/) ) for information concerning any Necessary Claims Disclosure Notices that have been received by the Kantara Initiative Board of Directors.

# Dear reader,

Thank you for downloading this publication prepared by the international community of experts that comprise the Kantara Initiative. Kantara is a global non-profit 'commons' dedicated to improving trustworthy use of digital identity and personal data through innovation, standardization and good practice.

Kantara is known around the world for incubating innovative concepts, operating Trust Frameworks to assure digital identity and privacy service providers, and developing community-led best practices and specifications. Its efforts are acknowledged by OECD ITAC, UNCITRAL, ISO SC27, other consortia and governments around the world. 'Nurture, Develop, Operate' captures the rhythm of Kantara in consolidating an inclusive, equitable digital economy offering value and benefit to all.

Every publication, in every domain, is capable of improvement. Kantara welcomes and values your contribution through [membership, sponsorship](https://kantarainitiative.org/membership/) and active participation in the [working group](https://kantarainitiative.org/groups/isi-work-group/) that produced this and participation in all our endeavors so that Kantara can reflect its value back to you and your organization.

![Rectangle 2](RackMultipart20230814-1-ayl9sl_html_49ac0cb03196381.gif)

Copyright: The content of this document is copyright of Kantara Initiative, Inc.
 © 2023 Kantara Initiative, Inc.

# Introduction

Trust Performance Indicators (TPIs), also referred to here as Transparency Performance Indicators, are used to capture the performance of digital transparency measuring how dynamic the performance of transparency is for digital services.

These TPIs are designed to quickly assess the operational capacity by measuring the performance of publicly required digital service information. The TPIs assess the digital components of authority and security to assure the access, validity, and availability of privacy.

Work at Kantara preceding these TPIs developed a consent receipt. It is a record that can be used to capture the state of trust before a session, to capture surveillance context, and capture whether notice was provided before the technical session is established, at the time, or after, and to capture the whether the providence of consent is implied or expressed dynamically.

There is no assessment that accounts for the capability in the use of consent receipts, in particular for the service user to record source, and session history. But there is in law, implied and expressed, consent states, which are commonly inferred in digital privacy and security contexts.

Most assessment for conformance of privacy information or services are mapped to analogue legal requirements which measure response times in days, out of technical context.  TPIs measure how dynamic privacy service information is, and include in the rating system a value which is indicated as a +1. The result is a dynamic, in context performance indicator, that facilitates an active state notice and privacy controls.

TPIs are recorded with a Notice Record, fully filled in, useable as a Controller Credential, which is used to generate a Consent Receipt.[1] This specification introduces a standardized record format for the capture of attributes that are required by law for the legal and trustworthy processing of personal identifiers.

The format is defined with the [ISO/IEC 29100](https://standards.iso.org/ittf/PubliclyAvailableStandards/c073722_ISO_IEC%2029100_2011_Amd%201_2018%20(EN).zip) security and privacy techniques framework. This format is used to collect identifier and session based attributes, notice, notification, and disclosure text mapped directly to the analogue (brick and mortar) legal requirements. We present here the standardized TPI creation process and how it can be used to complement, in fact necessarilly precede, (any) identifier creation workflow.

The Notice Record format can also be used to measure conformance with the ISO/IEC 29184 Online privacy notice and consent standard (2020), in which, the [Consent Notice Receipt](https://kantarainitiative.org/download/7902/) is provided in Annex B.

The use of the associated notices, receipts and records dramatically improve the security of personal data control, significantly increasing transparency, including importantly for the individual. It also greatly improves the scale and effectiveness of cyber physical security and digital privacy through the decentralized authority inherent in the Notice Record.

This specification is offered as a contribution to the ISO/IEC SC27 WG5 body of work, as it extends the ISO/IEC 29100 privacy and security framework into operational trust applications.

The Notice Record, generated from TPIs, enables operational 'online' transparency by the use of the controls in ISO/IEC 29184. This can be further evidenced with an anchored notice and mirrored (digitally twinned) notice consent receipts [again ISO/IEC 29184, Appendix B], again generated from a TPI Notice Record.

# Why was this specification written?

TPIs aim to help standardize digital transparency and dramatically improve the safety, security, and usability of digital transparency for people. It does so by providing a set of metrics to quickly assess if and how digital privacy is operating at the moment.

Currently, there is no way for people to see who is tracking them and how digitally exposed people are in context. Data control, access, and privacy rights requests and response time, TPIs indicate if the digital information provided upon contact with a digital service is capable of meeting this basic requirement and capable of dynamic data access and controls.

Digital transparency around why, who, and where behind a data request is as important as security and privacy of identifiers and attributes. Without standardized digital transparency it is difficult if not impossible to make decisions about the creation and subsequent necessary, tracking and monitoring of personal data and digital identifiers.

The TPIs are a step to where people have the insights to exercise access controls, and to use rights to create and control their own records of digital of identity relationships, in a meaningful or operational manner.

# Why Transparency Performance Indicator's?

TPIs provide a way to quickly see what digital privacy and/or security measures are in place, and in line with human, legal and analogue requirements for the human in context of operating a digital service.

TPIs capture digital identifiers and meta data to measure the performance of digital transparency for conformance to standards, compliance to regulations, and for self-sovereign assessment, business, operational, legal, technical, and social dimensions and considerations. Through the implementation and capture of records for legal proof of notice (shared knowledge and understanding), the TPIs set the stage (allow to follow in the workflow) for digital consent with a receipts. These receipts can then be used by people to provide their own evidence of notice and records.

4 TPIs in this document specify the capture of notification meta-data and measure its performance for digital consent. The TPIs provide human readable digital representations for digital transparency, and when required digital consent as well as other justifications or requirements for processing.

The TPIs presented are captured in a Notice Record, then assessed for conformance.

{note: this is out of scope} Use the notice receipt to create a personal data record, that can then be used to "anchor" the digital identity relationship with the organization, creating a basis and foundation for higher levels of digital transparency assurance and values of interactions. [2]

# What should you expect to find in this document?

The 4 TPIs specified here focus on the first/initial point of contact, and the transparency for public accessible digital services. This is publicly required set of information that MUST be provided, without requiring identification, authentication or authorization of the person.

TPI Indicators here are for Digital Transparency, Level of Trust Assurance 0. [Ref-DTL's] (self service and public (though legally required) without verification or validation).

The TPIs here are used to assess session based data capture and self asserted information by organizations.

TPI 1 - Measuring the Timing of Notice:

This TPI captures when the Controller's legal entity and accountable Privacy Officer (digital identifiers) provide notice; Before, At the time of, or After personal data is captured. This captures if dynamic transparency is available systematically and when. It provides a way for an individual to assess if they can trust a service or not.

Note: This is the most common legislated privacy element in the world, required in all privacy legislation and instruments. [(ISTPA 2007)](https://kantara.atlassian.net/wiki/spaces/WA/pages/2916489/Auxiliary+Reference+Documents?search_id=d979240f-f5c8-42e3-8c8c-5dbd2dd748d0)

TPI 2 - Measures Required Data Elements

This TPI capatures (or not) the data elements required for data processing (except when legally regulated otherwise [3] derogation). In "all" cases a Notice of who is processing your data, who is a accountable and the privacy contact information for access to personal information MUST be provided.

Notice of who is processing your data is required for all legal justifications for processing personal data in privacy law. It is also a fundamental security requirement, namely to identify the legal entity, and in some cases all beneficial owners, and the accountable person(s) involved in an interaction.

TPI 3 - Measure of Transparency Accessibility

This TPI measures the availability and access to the required information in TPI 2. For example, is the information presented in a pop-up notice, or is it required to click a link, e.g. to a standard transparency/privacy policy, is it the first screen or is it at a the bottom of a multi-screen display (e.g., with "dark patterns" such as links not highlighted).

TPI 4 - Measures security information integrity

This TPI captures the (Secure Socket Layer/Transport Layer Security) SSL/TLS ([e.g. 1.3](https://datatracker.ietf.org/doc/rfc8446/)) certificate or security keys ([e.g. JOSE](https://datatracker.ietf.org/group/jose/about/)) to compare its meta-data against the required information in TPI 2. This is very much along the lines of [Certificate Transparency](https://certificate.transparency.dev/) but looking specifically at whether the policies cover the Notice, e.g. does the SSL certificate Organization Unit field and Jurisdiction fields match the captured legal entity information, how does the policy and jurisdiction here relate to other beneficial entities. Importantly does this align with the policy expectations of the person.

# TPI Metrics and Use

Each of the TPIs can be measured to determine the level of performance for each of the indicators. 

TPIs are captured in sequence;

1. TPI measuring the point when the individual is notified versus when personal information/digital identifiers are collected and processed. Capturing the timing of notice presentation in relation to first data capture

2. TPI measuring the contents of the notification for required PII Controller digital attributes that correspond to the physical brick and mortar attributes specified in privacy, security, safety and surveillance legislation. This is the Controller identity and entity information and access point

3.TPI for how accessible the transparency is (transparency of digital transparency)and the accessibility of the notice access for use

4.TPI validating the cybersecurity information versus the digital transparency information capturing the SSL certificate or keys and its associated meta-data.

Combined, these TPIs provide an overall Indication of the operational state of digital privacy.

# TPI Methodologies

Timing of Notice vs Data Collection Transparency

TP1 requires monitoring the technical end point to see if PII is captured in relation to when a notice is provided. This measures the notice regulatory performance against legal and human usability requirements.

PII Controller Digital Attribute Transparency

Assess if the required information for transparency over who is in control of notice is 'provided'

The MUST fields identify elements that are required in legislation that MUST be present.

# Transparency Accessibility

How accessible is the PII Controller and Privacy Contact information?

For example, in the context of a website or a mobile device, how difficult was it to access the 'provided' information. How many clicks, or screens, away is the required information?

**Example — Accessibility Measurement Rating**

This transparency accessibility rating score of [1,0, -1 or –3] reflects the number of steps, screens, or clicks required to find the 'provided' information within a mobile application or webpage providing the client user interface.

# Security Validation Certificate (and/or Key) Security Transparency

This security performance indicator requires that the session security layer certificate or key information to be collected and then compared against the information in the Notice Record to validate the integrity of the security necessary for digital privacy.

This checks if the PII Controller identity information is the same or linked to the controlling entity in the associated security certificate. For example, does the SSL certificate identify the Controller, and is it secured for the DNS and localization expectation and corresponding jurisdictional information. This provides required digital security for privacy, measured for governance accountability and interoperability with legal adequacy with for eConsent (electronic or digital consent).

Certificate status, and transparency performance, are used to establish session security prior to the collection, use and processing of PII. The security TPI also measures the certificate and or cryptographic keys for a specified organizational unit to corroborate and validate the PII Controller's digital integrity.

Table 1: Transparency Performance Rating

The TPI Rating system is designed to measure the operational performance of the information. This rating is unique as it allows for an assurance levels that account for pre-assured, dynamically assured metric.

+1 refers to a technical framework and PII Controller transparency prior to the initiation of a session providing security based trust assurances.

0 refers to dynamic a measure of providing dynamic transparency in the context of once a technical session starts (which is at the time of collection), in context transparency over purpose and disclosures,

-1 provides for analogue legal expectations, represented by legal requirements not specific to a digital context.

-2 provides for low quality provision

-3 provides a metric for non-operable transparency and digital privacy.

| **Rating** | **TPI 1 - Timing (wrt to processing)** | **TP2** | **TPI3 Accessibility (trans performance)** | **TPI4 - digital security** |
| --- | --- | --- | --- | --- |
| +1 (assured) | Before [Transparency of control/governance - Before, during or after processing]   | +1 - credential is registered and present | Controller identity is presented prior to data collection - e | Security is required prior to collection (digital wallet based)   |
| 0(dynamic assurance) | Just In time | 0 credential is presented just in time (automated check and first time notice) | Embedded as a credential linked to authoritative registries.   | is assured -e.g. certificate is specific to and matches controller and context |
| -1 (analogue assurance - online) | During | controller information is accessible during collection | PII Controller Identity prominently displayed on first view – prior to processing first page of viewing, the assessment question would be   | not-specific to controller - does not match jurisdiction |
| -2 - (not mandatory in flow) | Available | Controller information is linked | is linked not presented | does not match ou |
| - 3 ( non operative) | After | Controller information not present | Identity or credential is not accessible in context - e.g. two or more screens of view away, or privacy contact is mailing g address and non operative in context of data collection. | is not valid or secure provider |

# TPI Instruction and Guidance

The TPI Rating system is designed to measure the operational performance of the information, for example if only a mailing address is provided for a privacy contact, on a website, this is considered non-operable according to the context. This means that privacy access and specific information is not retrievable in the context of data collection. Demonstrating a non-performant form of data governance.

| **Rating - Instruction** | **TPI 1 - Timing (wrt to processing)** | **TP2 - Required Info Presentation** | **TPI3 Accessibility (trans performance)** | **TPI4 - Digital Security** |
| --- | --- | --- | --- | --- |
| +1 (assured) | PII Controller credential is displayed, using a standard format with machine readable language and linked, for example, in an http header in a browser | Controller is discoverable automatically prior to session (out of band) in a machine readable format. Number of ways
 1. is a Controller Identity Trust registry
 2. is client side record of processing (via a wallet or browser) | Controller identity is presented prior to data collection | Security is required prior to collection (digital wallet based)   |
| 0(dynamic assurance) | PII Controller Identity or credential is provided in first notice | 0 credential is presented just in time (automated check and first time notice) | Embedded as a credential and dynamically available upon access (almost just in time)   | is assured -e.g. certificate is specific to and matches controller and context |
| -1 (analogue assurance - online) | The Controller Identity, or screen with the Controller Identity is one screen and click away. For example, the privacy policy link in the footer of a webpage | controller information is accessible (not presented) during collection | PII Controller Identity prominently displayed on first view – prior to processing first page of viewing, the assessment question would be   | not-specific to controller - does not match jurisdiction |
| -2 - (not mandatory in flow) |   | Controller Credential information is linked during collection | is linked not presented | does not match ou |
| -3 ( non operative) | PII Controller Identity is not accessible enough to be considered 'provided' | Controller information not present | Identity or credential is not accessible in context - e.g. two or more screens of view away, or privacy contact is mailing g address and non operative in context of data collection. | is not valid, secure, or recognized provider.
 Not security operational (proving non reciprocal security assurance) |

Table 2: TPI Schema

| TPI 1 |   |   |
| --- | --- | --- |
| Notification Timing |   |   |
| Timing of Data Collection |   |   |

Table 3 : Transparency Performance Indicator Record Rating Example

| **Field Name** | **Field Description** | **Requirement: Must**
**Shall**
**May** | **TPI 1**
 before (out of band), just in time (before), at the start - or time of collection, during collection and after collection | **TPI 2**

**Available**** Not Available **|** TPI 3 ****Rate: +1, 0, -1, -3,** | **TPI 4**
**Certificate or Key**

**CN-Matches**
**OU – Match**
**Jurisdiction – Match (optional)** |
| --- | --- | --- | --- | --- | --- | --- |
| Notice Location | Location the notice was read/observed | MUST | before, during, after | Present | +1 | found |
| PII Controller Name | Name of presented organization | MUST |   | Present | 0 | Match |
| PII Controller Address | Physical organization Address | MUST |   | Present | 0 | Not match |
| Privacy Contact Point | Location/address of Contact Point | MUST |   | Present | 1 | Not match |
| Privacy Contact Method | Contact method for correspondence with PII Controller | MUST |   | Present | -1 | No Match |
| Session key or Certificate | A certificate for monitored practice | MUST |   | Present (or Not-found) | 1 (or –3 ) | Present (or No Security Detected) |

# Summary

In summary, Transparency Performance Indicators, TPIs are specified here for people to use depending on context, location, security, and other out of session elements. TPIs are used to determine with one's own soverign reasoning whether to trust a service, not an external framing, opinion or forced default.

These TPIs use open standards, with an open license specified for people to be able to use and create records they can own and keep across and independently of service providers.

TPI 1 is a measure of trust, so that when asked, "Do you trust (accept) a service", you necessarily know who is processing your data before, during or after." Overwhelimingly people indicate trust would be higher. if notified prior to data capture, which only makes sense.

TPI 2 is the legally required information, is it present, and then used as a, generally available, standardized, and open metric for compliance.

TPI 3 is an indicator for how accessible and inclusive is digital transparency.

TPI 4 validates for the individual if security "adds up" for the them and in doing so addresses a critical security gap widely overlooked today.

# Roadmap

# References

# Appendix A: Notice Record Schema

In this appendix, here is a notice record template to fill out when recording a rating, along with a rating template, and analysis results format.

Notice Record Schema & , Notice Record and Report - Template and Example

1.2.    TABLE1: NOTICE RECORD SCHEMA

| FIELD NAME | FIELD DESCRIPTION | REQUIREMENT: MUST, SHALL, MAY | FIELD DATA EXAMPLE |
| --- | --- | --- | --- |
| Notice Location | Location the notice was read/observed | MUST | ![Rectangle 1](RackMultipart20230814-1-ayl9sl_html_49ac0cb03196381.gif)[Walmart.com | Save Money. Live Better](http://www.walmart.com/) |
| PII Controller Name | Name of presented business | MUST | Walmart |
| Controller Address | The physical address of controller and/or accountable person | MUST | 1940 Argentina Road Mississauga, Ontario L5N 1P9 |
| PII Controller Contact Type | Contact method for correspondence with PII Controller | MUST | Email, phone |
| PII Controller-Correspondence Contact | General contact point | SHALL | [Privacy@org.com](mailto:Privacy@org.com) |
| Privacy Contact Type |  The Contact method provided for access to privacy contact | MUST | email |
| Privacy Contact Point | Location/address of Contact Point | MUST | [Org.com/privacy.html](http://org.com/privacy.html) |
| Session Certificate | A certificate for monitored practice | Optional | SSL Certificate Security (TLS) and Transparency |

# Endnotes



1 Lizar, M, Pandit, H, Jesus, V, "Privacy as expected Consent Gateway", Next Generation Internet (NGI) Grant [Access July 4] privacy-as-expected.org/
