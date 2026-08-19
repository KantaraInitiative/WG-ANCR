# ANCR TS 27560:2023 Notice record extension

Anchored Notice and Consent Receipts for Operational Transparency, a consent receipt extension for TS 27560:2023 

**Revision:** No canonical version is fixed for this document. Cite this document by its Git commit hash until a canonical version is assigned by the ANCR Working Group. The revision history is recorded in CHANGELOG.md. Do not cite a bare version string, because version numbers are not interchangeable across artefacts.

## Foreword

This document specifies a notice receipt information structure that profiles and extends ISO/IEC TS 27560:2023 (consent record information structure). It is published by the Kantara Initiative and the Anchored Notice and Consent Receipt (ANCR) Working Group as a companion specification, and is intended to be cited as prior art and an implementation reference for SC 27/WG 5 work that depends on machine-readable notice and consent records (developed through contributions to ISO/IEC 27560 and ISO/IEC TS 27568 and FDIS 27091 Annex B.4, and informed by comments submitted to ISO/IEC WD 27566-2 for transparent age assurance).

IPR Note: This ANCR Record Specification is required to be open, as specified under a Patent & Copyright: Reciprocal Royalty Free with Opt-out to Reasonable and Non-discriminatory (RAND) license agreement at the Kantara Initiative chartered to contribute the completed consent receipt work to ISO/IEC SC 27 WG 5.

## Introduction

Governing ones own identity and being confident of privacy Online requires digital transparency, which means identifiers need to be notified, bound to a recorded artefact that can be referenced after the fact. Historically, such identifiers have been encapsulated in a record and provided in receipt of an event by context at a time and place. The notice receipt acts as a container not only for identifiers, but for the integrity of the claim that the identifiers represent and link to as real world objects.

An Online notice receipt (broadly refers to any notification, signal or disclosure digitally represented) it is generated through interaction (or a lack of interaction) with a physical sign, access point, a device or an online notification or statement using a device. A notice receipt can be generated independently by an individual, from the notice by scraping or accessing a controller identification record, in order to create a produce a proof of notice disclosure that can be exchanged between devices and across borders, with co-regulated digital id.

Co-regulated digital identification (CDRI). This profile is specified for co-regulated identification. Co-regulation means a standard public policy, with two rule sets that operate on the same identifier at the same time: the controller's own rules, expressed in service terms, technical design, and internal policy; and the public rules, expressed in treaty, law, and standards. Neither self-regulation nor state regulation alone governs identification at internet scale for a number of reasons. Self-regulation leaves the identifier privately defined. State regulation alone lacks operational artefacts that can be inspected at the time of interaction. This profile supplies the record structure through which the public rule set becomes machine readable, inspectable, and enforceable.

For online decentralised and human operated data governance Identity and identification must be technically distinct. Identity is self-expressed, requires self-identification, and is managed by the individual. Identification on the other hand is the technical and organizational process a controller uses to discover, link, or assert attributes (often called claims) about a person Online using identifiers. This process is called surveillance, which is human society requires privacy. Hence in CDRI, Consent is a human expression, an interaction managed by humans; Online processing permissions on the other hand are managed by organisations and systems. Where these are conflated, in an online interface, permission is presented as if consent is already implied. This profile keeps them separate by requiring controller identification, and the notice bound to it, before any demand for personal identification.

    Relationship to related instruments (informative):
    ISO/IEC 29100 Privacy framework
    ↓
    ISO/IEC 29184 Online privacy notices and consent
    ↓
    ISO/IEC TS 27560:2023 Consent record information structure
    ↓
    This profile (ISO/IEC TS 27560:2023 extension for Notice Record + Notice Receipt + Notice Event Log)
    ↓
    Applicable code of conduct / code of practice / privacy policy / law (jurisdiction-specific)

Authoritative sequence (informative). The authority for this work is stated once, in order: Convention 108+ and applicable legal authority; ISO/IEC 29100 privacy framework; ISO/IEC 29184 online privacy notice and consent; ISO/IEC TS 27560:2023 consent record information structure; the minimum notice disclosure and anonymity by default conditions specified in this document; and Transparency by Default as the operational implementation pattern that is conformant.  The key distinction being Online notice as a digital transparency gateway, for consent to be operational and portable online.

## 1 Scope

This document extends ISO/IEC TS 27560:2023 by specifying the notice evidence artefacts required for online notice to become inspectable and verifiable digital transparency. It specifies controller identification disclosure, versioned notice reference, Notice Receipt generation, anchored Notice Receipt, and notice event logging, so that notice can be evidenced before identification, consent, authorization, or other processing proceeds. It does not replace ISO/IEC 29184 or ISO/IEC TS 27560:2023, and it does not redefine consent.

This profile extends ISO/IEC TS 27560:2023 (consent record information structure), an ISO technical specification to which the Consent Receipt specification was contributed, and which this profile extends. It is used to specify a machine-readable online Notice Record and corresponding Notice Receipt that provide durable evidence of notice disclosure.

This profile specifies the record structure through which identification is co-regulated. Controller identification SHALL precede any demand for personal identification, and the artefacts specified in clause 7 SHALL be inspectable independently of any personal identifier. Where an implementation demands personal identification before a resolvable Controller Identification Record and its bound notice version are available, that implementation does not conform to this profile.

It supports layered and sequenced notices, notifications, and disclosures. Anchored Notice Receipt requirements are legal basis agnostic. When the lawful basis is consent, a corresponding authorization can be represented as a TS 27560:2023 consent receipt specialisation.

The base notice record extension defines a minimum interoperable set of notice artefacts for operational transparency:

- Controller Identification Record (CIR)
- Notice Event Record / Anchored Notice Receipt
- Notice Event Log
- Reference notice integrity and version binding, including notice_id and notice_version_reference

Interaction with an online notice record results in a notice receipt, which may be either:

- a full receipt, containing required record fields, or
- a reference receipt, with minimal fields plus stable references and rights payload.

Note: An online notice, notifications, disclosure, or statement sequences differ according to:

1. In person peer to peer using a device, where notice and identity are physically verifiable.
2. Remote, not in person, where identification is not physically verifiable. Controller identification is required.

Out of scope for the base extension, but may be handled by optional appendices or companion specifications:

- Authorization exchange protocol mechanics beyond the Anchored Notice Receipt
- Tokens, credentials, and wallet portability mechanisms
- Full RoPA / processing-record completeness requirements
- Cross-border security requirements beyond baseline notice disclosure
- AI lifecycle governance requirements beyond baseline notice disclosure

### 1.1 What this document enables others to standardize (informative)

The following are outside the scope of this document. This document provides the artefacts and vocabulary from which they can be standardized, and records them here only to state what it enables others to specify.

- Standardization of the online notice record and evidence of disclosure as a separate deliverable.
- Transparency profile and transparency policy as normative publication requirements.
- Conformance requirements placed on downstream work.

This subclause is informative. It creates no commitment, roadmap, or dependency, and it names no downstream document.

## 2 Normative references

- ISO/IEC TS 27560:2023 Privacy technologies: Consent record information structure
- ISO/IEC 29100, Privacy framework

### 2.1 Other references (informative)

- ISO/IEC 29184, Online privacy notices and consent
    - Note: free and open access to this standard is required for it to be listed as normative, or would block the use of 27568 directly, although it can be used for digital id controls and governance interoperability between 27560 TS Extension Profiles.

### 2.2 Use of normative keywords

The key words SHALL, SHOULD, and MAY in this document are to be interpreted as described in ISO/IEC Directives, Part 2.

NOTE: This draft avoids the use of "must" as a normative keyword. Where "must" appears in examples or explanatory text, it is not intended to introduce a normative requirement.

## 3 Terms and definitions

Terms and definitions from ISO/IEC TS 27560:2023 and ISO/IEC 29100 apply.

### 3.1 Controller Identification Record (CIR)

Publicly accessible controller accountability record used as an anchor for notice and receipt generation.

### 3.2 Notice Record

Controller-maintained record of notice content, versioned.

### 3.3 Anchored Notice Receipt

The **first notice receipt**: bilateral evidence artefact recording that a specific notice version was disclosed or presented. When the lawful basis is consent, the Anchored Notice Receipt provides the required proof of notice disclosure needed for valid legal consent and for linking any subsequent consent or authorization receipts to the anchored disclosure event.

### 3.4 Notice Event Log

Append-only record of lifecycle events related to notices and receipts, including issuance, material change, withdrawal, and objection hooks.

### 3.5 notice_version_reference

Immutable reference to the notice version in effect at the time of disclosure.

### 3.6 transparency statement

Versioned transparency disclosure artefact that expresses the standing terms of notice, including controller identification, processing context, and rights mechanisms, and is suitable for audit and stable referencing.

### 3.7 transparency notification

Event-bound message signaling that a transparency-relevant event has occurred, for example issuance, material change, or rights-related lifecycle event, typically referencing a specific transparency statement version.

### 3.8 reciprocal and proportionate transparency

Disclosure property in which the technology-mediated processing capabilities and the practical rights controls available to the individual are stated in a manner that is proportionate to the risk surface and reciprocal to the controller's technical capability, i.e., what the technology can do is matched by what the individual can see and control.

### 3.9 co-regulated identification

Use of digital identification mechanisms under two concurrent rule sets, the controller's own rules and the applicable public rules of treaty, law, and standards, implemented such that the public rules are expressed as inspectable record structure and are verifiable before identification occurs.

Note 1 to entry: Co-regulated identification does not restrict which identification technology is used. It constrains the sequence and the evidence: accountable controller identification, machine-readable notice, and durable receipt precede personal identification.

Note 2 to entry: Conformance to co-regulated identification is assessed through the artefacts in clause 7, not through claims made in prose policy documents.

### 3.10 identification

Technical and organizational process by which a controller recognises, links, or asserts claims about an individual, including assignment or inference of identifiers.

### 3.11 identity

Self-expression and self-identification managed by the individual, including the individual's own choice of which identifiers to bind to a given Controller Identification Record.

### 3.12 minimum notice disclosure

Smallest set of disclosures that are present, resolvable, and inspectable before identification or processing begins, comprising the Controller Identification Record, the notice version in effect, the asserted lawful basis, the scope of disclosure, and the privacy access point.

Note 1 to entry: The requirement that this set be resolvable and inspectable before identification or processing begins is normative and is stated in 5.1 C2, not in this definition.

### 3.13 anonymity by default

Property whereby notice disclosure and the resulting evidence artefacts are generable, retrievable, and verifiable without identification of the individual, and without an account_id or pii_principal_id.

Note 1 to entry: Anonymity by default applies to the notice and evidence layer. It does not restrict identification that is required by the lawful basis for the processing itself.

Note 2 to entry: Retrieval of a Controller Identification Record is not an identification event, see 7.1.

### 3.14 non-exclusion

Property whereby the minimum notice disclosure and the routes to recourse are reachable through at least one privacy_access_point modality that does not require the individual to hold, present, or authenticate a digital identification credential.

Note 1 to entry: Non-exclusion addresses accessibility needs, low or absent connectivity, delegated and assisted interaction, and in person contexts where notice and identity are physically verifiable.

### 3.15 notice

Disclosure made before processing, authorization, identification, or consent.

### 3.16 online notice

Notice presented, published, or made inspectable in an online environment.

### 3.17 digital transparency

Online notice made machine readable, versioned, inspectable, evidenced, and receipted.

### 3.18 consent

Human managed legal authorization given after sufficient notice and meaningful choice.

Note 1 to entry: This document does not redefine consent. Where consent is the legal basis, it references the prior notice disclosure event on which consent depends, as specified in 7.6.

### 3.19 online consent

Consent expressed online, where notice, choice, action, and the resulting evidence are represented by machine readable records of consensus driven interaction.

### 3.20 permission

Technical allow or deny control.

Note 1 to entry: Permission is not consent. Where interface permission is presented as consent, the two are conflated.

### 3.21 consent record

Controller retained evidence of consent, derived from a consent statement and linked to notice evidence where consent is the legal basis.

### 3.22 two-factor online notice (2FN)

Notice event in which presentation controls and evidence receipt generation are both present.

Note 1 to entry: The two factors are counted within one notice event. Two-factor online notice is not an assurance level, and it does not denote repeating notice, or rounds of a notification sequence or a second presentation of the notice commonly described as 'consent fatigue', but instead proof of the same notice event.

Note 2 to entry: The pre-authorization disclosure baseline in this document is expressed by minimum notice disclosure (3.12) and anonymity by default (3.13), not by a factor label. Adjacent usage of factor labels is described in the NOTE in 6.1.

## 4 Symbols and abbreviated terms

- 2FN  two-factor online notice
- ANCR  Anchored Notice and Consent Receipt
- CIR  Controller Identification Record
- CDRI  co-regulated digital identification
- MVCR  Minimum Viable Consent Receipt
- PII  personally identifiable information
- RoPA  record of processing activities
- TS  technical specification

## 5 Conformance

An implementation conforms to the Base extension if it satisfies all mandatory requirements in clause 8. Implementations MAY additionally claim conformance to optional extension profiles for PII and Personal records of processing activity profiles defined in Annex B.

### 5.1 Co-regulation conformance criteria

An implementation claiming conformance to co-regulated identification SHALL satisfy all of the following:

- **C1 Sequence.** A resolvable Controller Identification Record is available before any demand for personal identification.
- **C2 Minimum notice disclosure.** The elements in 3.12 are resolvable at the time of the disclosure event.
- **C3 Anonymous by default.** The Anchored Notice Receipt is generable and verifiable without an account_id or pii_principal_id.
- **C4 Public rule reference.** The Notice Record states the applicable public rule set by reference to the code of conduct, code of practice, or legal instrument relied upon.
- **C5 Evidence.** A Notice Event Log entry exists for issuance and for each material change, and each receipt binds to an immutable notice_version_reference.
- **C6 Reciprocal and proportionate disclosure.** The disclosure set in 7.2.1 is published and bound to the notice version in effect.
- **C7 Non-exclusion.** At least one privacy_access_point modality is operable without the individual holding, presenting, or authenticating a digital identification credential, and the minimum notice disclosure in 3.12 is retrievable through that modality.

An implementation that satisfies C1 to C7 for a given notice version MAY assert co-regulated identification conformance for the processing context covered by that version. Conformance is asserted per notice version, not per organization.

## 6 Overview of notice artefacts and reference integrity

### 6.1 Overview: two-factor online notice (2FN) and receipt evidence

This profile supports a two-factor online notice pattern (2FN) for establishing durable evidence of notice disclosure and, where applicable, consent.

- **Factor 1, presentation controls:** The notice is presented using ISO/IEC 29184-aligned online notice and consent presentation controls, e.g., layered notice presentation, timing, and interaction patterns, that are reusable across policy or notice types.
- **Factor 2, evidence receipt:** The notice receipt is anchored to provide durable (personal) evidence that a specific notice version was presented or available at a specific time and, when the lawful basis is consent, to support proof of informed consent by binding the authorization state to the disclosed notice version.

Implementations SHOULD treat 2FN as an interoperability pattern: the presentation controls establish consistent experience and meaningful choice, while the receipt provides verifiable, referenceable evidence for audit, later inquiry, and dispute resolution.

**Lineage note (informative).** The two-factor online notice pattern originates in the Minimum Viable Consent Receipt (MVCR), the specification from which the ANCR co-regulation perspective developed. In that lineage, 2FN denotes the mode in which the PII Principal initiates the interaction: the individual approaches a physical sign, an access point, a device, or an online notice, the notice is presented, and a bilateral receipt is returned. The two factors are counted within the notice event, presentation and evidence. They are not two rounds of a sequence, and 2FN does not denote a second presentation of the notice.

**Initiation modes.** A notice disclosure event is either principal initiated, where the individual seeks the notice in order to discover, or controller initiated, where the controller presents the notice in the course of offering or operating a service. Both modes produce the same artefact set specified in 6.2, and the requirements of this profile apply to both without variation. The initiation mode affects only the operational interpretation of the disclosure event, as specified in 7.2.2.

NOTE: Where this profile is read alongside work items that use one factor notice (1FN) and two factor notice to denote scope in rounds of a disclosure and authorization sequence, the two usages are counting different things. The equivalent in this profile of a controller-side pre-authorization disclosure minimum is the minimum notice disclosure in 3.12, together with the anonymity by default requirements in 3.13, 7.3.1, and 5.1 C3.

### 6.2 Notice Receipt Object set

1. CIR, controller accountability anchor
2. Notice Record, versioned notice content
3. Anchored Notice Receipt, proof of notice evidence
4. Notice Event Log, lifecycle

Together these four artefacts constitute the co-regulation evidence set. The CIR anchors public accountability, the Notice Record expresses the public rule set in operational form, the Anchored Notice Receipt evidences the disclosure event bilaterally, and the Notice Event Log evidences the lifecycle. Two-factor online notice is the mechanism by which the set is produced: presentation controls establish meaningful choice, and the receipt makes that choice inspectable after the fact.

### 6.3 Reference integrity and version binding

A Notice Receipt SHALL reference:

- notice_id, stable family identifier
- notice_version_reference, immutable version reference

A material change to a notice, including purposes, lawful basis, recipients/jurisdictions, retention, or rights mechanisms, SHALL:

- create a new notice version, and
- create a corresponding Notice Event Log entry.

Historic notice versions SHALL be retained as long as any processing or records depend on them, maintaining ongoing reference discipline.

## 7 Notice record specifications

### 7.1 Controller Identification Record (CIR)

### 7.1.1 CIR minimum field set

A CIR SHALL include at minimum:

- controller_public_id_uri
- controller_name
- jurisdiction
- privacy_access_point (structured)

A CIR SHOULD include:

- controller_address
- code_of_conduct_reference (if applicable)

A CIR MAY include:

- derogation_reference (lawful withholding)

### 7.1.1A CIR field specification table (normative)

| Field | Description | Required? | Value type / format | Constraints | Exposure | TS 27560:2023 anchor |
| --- | --- | --- | --- | --- | --- | --- |
| controller_identity_record_id | Stable identifier for the CIR | Yes | URI or string identifier | SHALL be stable; SHALL be suitable for referencing by receipts and event logs | Public | 6.3.6.2 party_id (controller party) |
| controller_public_id_uri | Public resolvable controller identifier | Yes | URI | SHALL be resolvable or dereferenceable by intended relying parties | Public | 6.3.6.5 party_url (closest anchor) |
| controller_name | Controller legal name | Yes | String | SHALL represent the accountable controller entity | Public | 6.3.6.7 party_name |
| jurisdiction | Applicable jurisdiction indicator or pointer | Yes | Code or string | SHALL be present; MAY be a pointer to a code of conduct reference | Public | 6.3.4.17 jurisdiction (PII processing) |
| privacy_access_point | Rights/contact access modalities | Yes | Array of objects | Each entry SHALL include type, value, label | Public | 6.3.6.9 party_contact (closest anchor) |
| notice_event_log_url | Pointer to the notice event log service or resource | No | URL/URI | When present, SHOULD be publicly discoverable | Public | N/A (extension field) |
| controller_address | Controller address (optional) | No | String or structured address | - | Public | 6.3.6.3 party_address (closest anchor) |
| code_of_conduct | Pointer to authoritative code of conduct / practice | No | URI | When present, SHOULD be versioned | Public | 6.3.4.21 codes_of_conduct (closest anchor) |
| derogation_reference | Lawful withholding / derogation metadata (optional) | No | Object | When present, SHOULD include reference_uri, authority, valid_until | Public or restricted | N/A (extension field) |

NOTE: The referenced artefact is the Controller Identification Record (CIR). The field name `controller_identity_record_id` retains "identity". In the context of the controller and the "identification" label of the record, this is permissible for the current version. The field name will be updated to align with "identification" in a future version.

### 7.1.2 privacy_access_point

privacy_access_point SHALL support multiple modalities.
Each modality entry SHALL include: type, value, label.

### 7.1.3 derogation_reference

When lawful derogations apply, derogation_reference SHOULD include: reference_uri, authority, valid_until. (optional)

### 7.2 Notice Record

A Notice Record SHALL be versioned and resolvable such that an Anchored Notice Receipt can reference an immutable version.
This profile uses Anchored Notice Receipts to reference immutable notice versions.
Relationship note (interoperability): A Notice Record functions as the machine-readable transparency statement (standing, versioned disclosure artefact). A notification about issuance or change is represented as a transparency notification via the Notice Event Log and/or notice_type = notification, and SHOULD reference the relevant notice_version_reference.

#### 7.2.1 Reciprocal and proportionate transparency disclosure set

For each Notice Record version relied upon by a receipt, the controller SHALL publish a **technology + controls disclosure set** that is:

- bound to the exact notice_version_reference in effect at disclosure time; and
- publicly retrievable either inline in the Notice Record or by stable reference.

The disclosure set SHALL include, at minimum, the following elements:

- technology_in_use;
- controls_available_primary;
- associated_or_derivative_controls (when applicable);
- secondary_purposes_of_use (when present); and
- limitations_or_derogations_on_controls (when applicable).

The Notice Record SHALL include a stable pointer to this disclosure set using `transparency_disclosure_reference` (URL/URI), unless the full disclosure set is embedded inline in the Notice Record itself.

Changes to the disclosure set that affect technology class(es) in use, the availability/scope/effect of practical rights controls, or secondary purposes SHALL be treated as material changes and SHALL trigger a new notice version and a corresponding Notice Event Log entry.

#### 7.2.2 Lawful basis interoperability

This profile is lawful-basis interoperable: the Notice Receipt structure SHALL support all lawful bases under applicable law. Each lawful basis has distinct rights, obligations, and dispute triggers.
Implementations SHALL communicate the asserted lawful basis in the receipt header, and SHALL publish the applicable rights/obligations variant using the Annex C table structure.
The `lawful_basis` value records the basis asserted by the controller at the time the notice version was presented. It SHALL NOT be interpreted as evidence that the asserted basis was validly established.
Where a two-factor online notice returns a bilateral Anchored Notice Receipt, the receipt is evidence that the notice version was presented and that presentation was acknowledged. The receipt SHALL NOT by itself be treated as evidence that consent was obtained, and no lawful basis SHALL be inferred by default from the presence of a receipt.
Where the asserted `lawful_basis` is `consent`, conformance SHOULD additionally require an authorization record that is distinct from the Anchored Notice Receipt and separately bound to the same `notice_id` and `notice_version_reference`. The receipt records disclosure. The authorization record records permission.
Where no authorization record exists and no basis other than consent is asserted, the exchange SHALL be recorded with the lawful basis unresolved. An unresolved lawful basis SHALL NOT be defaulted to `consent`.
If a lawful basis other than consent is asserted, the receipt header SHALL state that lawful basis explicitly (e.g., contract, legal obligation, legitimate interest, vital interest, public interest) and SHALL reference the corresponding Annex C row (rights/obligations variant).
Receipts are designed to be detectable and reusable to reduce repetitive notice and consent demands on the individual. The profile is designed to complement existing physical signs and privacy policy pages by providing a standardized notice record that can be extended by context and external codes of conduct to support transparency by default codes of practice.
By standardizing notice version references and receipt exchange, the profile supports cross border transparency and dispute resolution, including material change signalling through the notice event log.

NOTE: Separating disclosure evidence from authorization evidence keeps the notice record usable under every basis in Annex C, and prevents a transparency artefact from being read as a permission artefact.

### 7.3 Anchored Notice Receipt

This profile treats “Anchored Notice Receipt” as a **receipt classification**, not a separate primary artefact type. A receipt MAY be marked as an Anchored Notice Receipt using the optional indicator field `anchored_notice_receipt`.
Where `anchored_notice_receipt` is not asserted (or is false), the receipt SHALL link to the applicable Anchored Notice Receipt via `anchored_notice_receipt_id` so that subsequent receipts are traceable to the initial notice disclosure event.

### 7.3.1 Anonymous-by-default (Anchored Notice Receipt)

Anchored Notice Receipts SHALL NOT require an account_id or pii_principal_id

### 7.3.2  Notice Receipt field specification table

The following fields define the minimum interoperable Anchored Notice Receipt.

| Field | Description | Required? | Value type / format | Constraints | Exposure |
| --- | --- | --- | --- | --- | --- |
| schema_version | Schema reference for technical interpretation of the receipt structure | Yes | String identifier | SHALL reference the implementation documentation (receipt schema) in effect at issuance | Holder issuer |
| anchored_notice_receipt | Indicator that the receipt instance is the Anchored Notice Receipt (first notice receipt) for the applicable notice version disclosure event | No | Boolean | When present and true, the receipt is classified as an Anchored Notice Receipt; when false or absent, the receipt SHALL reference the applicable Anchored Notice Receipt using anchored_notice_receipt_id | Holder issuer |
| receipt_id | First Notice Receipt instance identifier | Yes | URI or string identifier | SHALL be unique within the issuer domain or as defined by the implementation | Holder issuer |
| anchored_notice_receipt_id | Reference to the applicable Anchored Notice Receipt instance identifier | No | URI or string identifier | When anchored_notice_receipt is true, this field SHOULD be absent or equal to receipt_id; when anchored_notice_receipt is false or absent, this field SHALL reference the applicable Anchored Notice Receipt | Holder issuer |
| account_id | Identifier or reference to the account or relationship context (pseudonymous where applicable) | No | URI or string identifier | When present, SHOULD be unlinkable and data-minimizing; SHALL NOT be required for anonymous-by-default operation | Holder issuer |
| notice_id | Stable notice family identifier | Yes | URI or string identifier | SHALL remain stable across notice versions | Holder issuer |
| notice_version_reference | Immutable reference to the disclosed notice version | Yes | URI and/or hash reference | SHALL reference the exact notice version in effect at disclosure time | Holder issuer |
| transparency_disclosure_reference | Stable pointer to the Notice Record’s technology + controls disclosure set | No | URL/URI | When the disclosure set is not embedded inline in the Notice Record, this field SHOULD be present so relying parties can retrieve the clause 7.2.1 disclosure elements bound to notice_version_reference | Holder issuer |
| controller_identity_record_id | Reference to the CIR | Yes | URI or string identifier | SHALL reference a resolvable CIR | Holder issuer |
| presented_at | Time of disclosure/presentation | Yes | Date-time | SHALL be recorded with sufficient precision for dispute resolution | Holder issuer |
| lawful_basis | Asserted lawful basis for the processing context covered by the notice version | Yes | Controlled vocabulary | SHALL use the vocabulary in Annex C; SHALL be present in the receipt header for lawfulbasis interoperability | Holder issuer |
| purpose | Recorded purpose relied upon for the processing context | Yes | Text or structured reference | SHALL be recorded and bound to notice_version_reference and controller_identity_record_id; MAY be carried by reference to the Notice Record for the applicable version, as specified in 7.5 | Holder issuer |
| two_factor_notice | Indicates whether this disclosure event was a two-factor online notice (2FN) producing a bilateral receipt | No | Boolean | If true, the receipt records presentation and acknowledgement only; no lawful basis is inferred by default from the presence of the receipt (see 7.2.2) | Holder issuer |
| notice_type | Notice classification | Yes | Controlled vocabulary | SHALL use the vocabulary in 7.3.1A | Holder issuer |
| recipient_jurisdictions | Destination jurisdiction(s) for cross-border transfer/disclosure | No | Array of country codes | When cross-border transfer/disclosure applies, this field SHALL be present; values SHOULD use ISO 3166-1 alpha-2 | Holder issuer |
| transfer_mechanism | High-level transfer mechanism / safeguard class | No | Controlled vocabulary | When cross-border transfer/disclosure applies, this field SHALL be present; vocabulary MAY be profiled by jurisdiction | Holder issuer |
| surveillance_risks | Material risk disclosure hook for state access/surveillance exposure | No | Text or structured reference | When applicable, SHOULD be present; if present, SHALL be version-bound via notice_version_reference | Holder issuer |
| rights_derogations | Disclosure of rights limitations/derogations in the applicable context | No | Text or structured reference | When applicable, SHOULD be present; changes SHALL be treated as material change | Holder issuer |

### 7.3.1A notice_type vocabulary (normative)

notice_type SHALL use one of the following values:

- Statement
- notification
- risk disclosure
- policy
- signal

Implementations MAY define additional notice types, but SHALL map them to one of the values above for interoperability.

### 7.3.3 Required identifiers

An Anchored Notice Receipt SHALL include at minimum:

- receipt_id
- notice_id
- notice_version_reference
- controller_identity_record_id (or resolvable pointer to the CIR)
- presented_at (event_time)
- notice_type

### 7.4 Notice Event Log

### 7.4.1 Minimum event types

The Notice Event Log SHALL support, at minimum:

- notice_issued
- notice_material_change

### 7.4.2 Event record minimum fields (normative)

Each Notice Event Log entry SHALL include at minimum:

- event_id
- event_time
- event_type
- notice_id and/or notice_version_reference
- receipt_id (when applicable)

### 7.4.3 Event type registry (normative)

Implementations SHALL support at minimum the following event types. Additive event types MAY be defined by companion specifications.

| event_type | Trigger | Required linkages | Notes |
| --- | --- | --- | --- |
| notice_issued | On issuance/publication of a new notice version | SHALL include notice_version_reference; SHOULD include notice_id | Supports discovery of current and historic notice versions |
| notice_material_change | On any material change (purposes, lawful basis, recipients/jurisdictions, retention, rights mechanisms) | SHALL include prior and new notice_version_reference OR an implementationdefined diff pointer | Used to enforce version binding and ongoing reference discipline |

The Notice Event Log SHOULD support hooks for:

- withdrawal/objection events
- rights exercise events

NOTE: Implementations MAY tier event-log requirements by assurance level; where tiered, the implementation SHALL state the tier.

### 7.4.4 Processing events (distinct from notice lifecycle events)

The Notice Event Log records notice lifecycle events. Processing events are distinct from notice lifecycle events and SHALL be recorded separately, so that governed processing is testable against the notice version relied upon.

A processing event record SHALL include at minimum:

- processing_event_id
- event_time
- processing_event_type
- notice_version_reference (the notice version relied upon for the processing)
- controller_identity_record_id (the accountable controller)
- purpose (the recorded purpose relied upon, as specified in 7.5)

Note 1 to entry: Separating processing events from notice lifecycle events allows an implementation to demonstrate that recorded processing was governed by a disclosed notice version, and to detect processing that is bound to no notice version or no recorded purpose.

### 7.5 Purpose as a recorded artefact

Purpose SHALL be recorded, and SHALL be specified before identification or transfer. Each recorded purpose SHALL be bound to:

- the legal authority relied upon;
- the controller_identity_record_id of the accountable controller; and
- the notice_version_reference in effect at the time the purpose is disclosed.

NOTE 1: Unrecorded purpose is a security defect, not a documentation omission. Transparency evidence that cannot be inspected after the fact cannot support accountability or enforcement, so the absence of a recorded, bound purpose is a defect in the evidence rather than a missing document. The conformance consequence of failing to record purpose is stated in Clause 8.

NOTE 2: Purpose is carried in the Notice Record for the applicable notice version and is bound to receipts and processing events through notice_version_reference. Recording purpose as an artefact, rather than as narrative, allows a relying party to test whether processing was bound to a disclosed purpose, controller, and notice version.

### 7.6 Relationship to consent records

Where consent is the legal basis, the consent statement and the consent record SHALL reference the prior notice disclosure event, by notice_version_reference and the applicable Anchored Notice Receipt. This document specifies that reference only. It does not specify consent, the consent statement, or the consent record, which remain governed by ISO/IEC TS 27560:2023 and ISO/IEC 29184.

## 8 Mandatory requirements

1. CIR publication (publicly accessible)
2. Anonymous Anchored Notice Receipt-by-default (no pii_principal_id required), aligned with §7.3.1
3. Version binding and ongoing reference retention
4. Material change rule + notice event log entry
5. Anchored Notice Receipt SHALL populate notice_type using the vocabulary in 7.3.1A.
6. Reciprocal and proportionate technology and rights-controls disclosure, aligned with the rule in “Lawful basis interoperability”.
7. Purpose recorded and bound to legal authority, controller, and notice version in effect, as specified in 7.5.
8. Processing events recorded distinctly from notice lifecycle events, as specified in 7.4.4.

## Annex A - Informative Mapping to ISO/IEC TS 27560:2023

This annex provides an initial interoperability mapping between the base extension artefacts and ISO/IEC TS 27560:2023 anchors. It is intentionally a starter mapping suitable for committee review; field-level clause alignment can be expanded as the 27560:2023-1 text is stabilized.

- TS clause references refer to ISO/IEC TS 27560:2023 (not drafts).
- “Profile field” names refer to fields defined in this document’s receipt and record tables.
- “Action” is the recommended migration or interpretation rule for implementers exchanging records across the TS and this profile.

## A.1 TS 27560:2023 record + receipt header alignment

This profile supports TS-style schema governance and identifiers by carrying forward `schema_version` and receipt/record identifiers. Where TS uses `pii_principal_id` as required in the consent record header, this profile uses `account_id` as an optional identifier for relationship context (pseudonymous where applicable).

## A.1.1 New vs updated fields

This section classifies profile fields relative to TS 27560:2023:

- **New fields**: not present in TS 27560:2023.
- **Updated TS fields**: a TS field is renamed, constrained, or its semantics are adapted.

## A.1.1A New fields introduced by this profile

| Profile field | Status | Closest TS anchor | Notes |
| --- | --- | --- | --- |
| anchored_notice_receipt | New | N/A | Indicator that a receipt instance is classified as the First Notice Receipt for the applicable notice disclosure event. |
| anchored_notice_receipt_id | New | N/A | Linkage field; when anchored_notice_receipt is false/absent, this field references the applicable First Notice Receipt. |
| notice_id | New | privacy_notice (reference) | Stable notice family identifier; complements the TS privacy_notice URL/version reference by providing a stable family identifier across versions. |
| notice_version_reference | New | privacy_notice (reference) | Immutable reference to the disclosed notice version; supports version binding beyond a mutable URL. |
| controller_identity_record_id | New | party_id | Specializes controller party identification as a resolvable CIR identifier. |
| presented_at | New | event_time | Time of disclosure/presentation; aligned to TS event_time semantics for the notice disclosure event. |
| notice_type | New | N/A | Classification vocabulary (notification/disclosure/policy/signal). |
| two_factor_notice | New | N/A | Optional indicator for the 2FN pattern producing a bilateral receipt. |
| recipient_jurisdictions | New | recipient_third_parties / jurisdiction | Optional explicit cross-border destination jurisdictions (simplified hook for transfer disclosure). |
| transfer_mechanism | New | N/A | Optional safeguard/transfer mechanism class for cross-border transfers. |
| surveillance_risks | New | impact_assessment (optional) | Optional risk disclosure hook for surveillance/state access exposure. |
| rights_derogations | New | N/A | Optional disclosure of rights limitations/derogations in the applicable context. |

## A.1.1B Updated TS fields (rename / relax / specialize)

| TS 27560:2023 field | Profile field | Change type | Notes |
| --- | --- | --- | --- |
| pii_principal_id | account_id | Renamed + relaxed | TS requires pii_principal_id in the consent record header; this profile replaces it with optional account_id to support anonymous-by-default operation (pseudonymous where applicable). |
| party_id (controller) | controller_identity_record_id | Specialized | Controller party identifier is specialized as a CIR reference rather than an opaque party_id. |

## A.1A Field mapping table

| TS 27560:2023 field | TS clause | Profile field | Action | Notes |
| --- | --- | --- | --- | --- |
| schema_version | 6.3.3.2 / 6.4.5.2 | schema_version | Same | Required in TS record and TS receipt metadata; required in this profile’s receipt header. |
| record_id | 6.3.3.3 | receipt_id (for receipt artefacts) | Map / rename | TS distinguishes record_id (record) and receipt_id (receipt). This profile uses receipt_id for receipt instances; implementations MAY also persist a TS-style record_id in controller-side records. |
| receipt_id | 6.4.5.3 | receipt_id | Same | Unique receipt instance identifier. |
| pii_principal_id | 6.3.3.4 | account_id | Map / relax | TS requires pii_principal_id in the record header. This profile makes account_id optional to support anonymous-by-default operation; when present it SHOULD be data-minimizing and unlinkable. |
| event_time | 6.3.7.2 | presented_at | Map | For First Notice Receipt classification, presented_at captures the time of disclosure/presentation (TS event_time equivalent). |
| party_id (controller) | 6.3.6.2 | controller_identity_record_id | Map / specialize | Controller party identifier is specialized as a reference to the CIR identifier. |
| party_name (controller) | 6.3.6.7 | controller_name (CIR) | Map | Carried in the CIR rather than repeated per receipt where a reference receipt pattern is used. |
| party_contact (controller) | 6.3.6.9 | privacy_access_point (CIR) | Map | Rights and contact modalities are carried as structured entries in CIR privacy_access_point. |
| privacy_notice | 6.3.4.2 | notice_version_reference | Map / extend | TS uses a notice reference (typically URL/version). This profile uses an immutable notice_version_reference (URL and/or content hash) and MAY also carry a notice URL in a Notice Record. |
| language | 6.3.4.3 | (Notice Record disclosure set) | Map | Language remains applicable to Notice Record rendering; include in the Notice Record and/or referenced transparency statement where multilingual delivery is supported. |
| purposes | 6.3.4.4 | (Notice Record disclosure set) | Map | TS purposes are carried in the Notice Record and SHOULD be bindable to notice_version_reference; secondary purposes are disclosed via secondary_purposes_of_use (clause 7.2.1) when present. |
| purpose | 6.3.4.5 | (Notice Record disclosure set) | Map | Purpose labels/identifiers are disclosed in the Notice Record for the applicable notice version. |
| lawful_basis | 6.3.4.7 | lawful_basis | Map / generalize | TS lawful_basis is consent-scoped; this profile generalizes lawful basis for interoperability across lawful bases (Annex C vocabulary). |
| pii_information | 6.3.4.8 | (Optional Profile B1) | Map | PII attribute/category inventories are profile-extension scope (B1 processing record). A Stage 1 reference receipt MAY omit inventories. |
| pii_controllers | 6.3.4.9 | controller_identity_record_id | Map / specialize | Controller identification is anchored in CIR via controller_identity_record_id; joint controllers MAY be represented as multiple CIR references. |
| storage_locations | 6.3.4.12 | (Optional Profile B1) | Map | Storage location disclosure is processing-record scope (B1) and MAY be referenced from notice versions where required. |
| retention_period | 6.3.4.13 | (Optional Profile B1) | Map | Retention disclosure is processing-record scope (B1) and MAY be referenced from notice versions where required. |
| jurisdiction | 6.3.4.17 | jurisdiction (CIR) | Map | TS jurisdiction is a PII processing field; this profile additionally requires a controller-asserted jurisdiction in CIR for controller-id-first inspection. |
| recipient_third_parties | 6.3.4.18 | (Optional Profile B1) / recipient_jurisdictions | Map / extend | Recipient inventory may be carried in B1; cross-border destinations are disclosed using recipient_jurisdictions when applicable. |
| withdrawal_method | 6.3.4.19 | privacy_access_point (CIR) | Map / refactor | Withdrawal and other rights controls are represented as structured modalities via privacy_access_point and the clause 7.2.1 controls disclosure set. |
| privacy_rights | 6.3.4.20 | privacy_access_point (CIR) | Map / refactor | Rights exercise is represented via structured privacy_access_point modalities and the clause 7.2.1 controls disclosure set. |
| codes_of_conduct | 6.3.4.21 | code_of_conduct_reference (CIR) | Map | Code-of-conduct reference is carried in the CIR where applicable. |
| impact_assessment | 6.3.4.22 | surveillance_risks (when applicable) | Map / specialize | Profile introduces surveillance_risks as a targeted risk disclosure hook; broader impact assessment remains optional processing-record scope. |
| authority_party | 6.3.4.23 | privacy_access_point (CIR) | Map / refactor | Complaint/appeal access points are represented as privacy_access_point modalities and/or referenced authorities. |
| event_time | 6.3.7.2 | presented_at | Map | Time of disclosure/presentation is recorded in presented_at for notice disclosure events. |
| validity_duration | 6.3.7.3 | (Optional; basis-dependent) | Map | Validity duration MAY be represented for time-bounded authorizations; when used it SHOULD be bound to the applicable lawful basis and scope. |
| entity_id | 6.3.7.4 | controller_identity_record_id | Map / constrain | For controller-issued notice events, the acting entity can be represented by the controller_identity_record_id (CIR reference). |
| event_type | 6.3.7.5 | notice_type | Map / extend | TS event_type supports consent-type examples; this profile uses notice_type to classify notice context and supports Notice Event Log event_type for lifecycle events. |
| event_state | 6.3.7.6 | (Notice Event Log event_type) | Map | Lifecycle state transitions are represented as Notice Event Log entries (notice_issued, notice_material_change, etc.). |
| collection_method | 6.3.4.10 | (Optional Profile B1) | Map | Collection method disclosure is processing-record scope (B1) and MAY be referenced from notice versions where required. |
| processing_method | 6.3.4.11 | technology_in_use | Map / refactor | Where processing methods imply technology-mediated capabilities (e.g., profiling, automated decision), represent them in technology_in_use (clause 7.2.1) and disclose corresponding controls. |
| processing_locations | 6.3.4.14 | (Optional Profile B1) / recipient_jurisdictions | Map / extend | Processing locations may be captured in B1; cross-border destinations are disclosed via recipient_jurisdictions when applicable. |
| geographic_restrictions | 6.3.4.15 | (Optional Profile B1) | Map | Geographic restrictions are processing-record scope (B1) and MAY be referenced from notice versions where required. |
| services | 6.3.4.16 | (Notice Record disclosure set) | Map | Service/business-process labels may be disclosed in the Notice Record to contextualize purposes; keep consistent with notice_version_reference. |
| pii_type | 6.3.5.2 | (Optional Profile B1) | Map | PII category listing is processing-record scope (B1). Where disclosed in notices, it SHOULD be aligned to the same PII categories used in B1 records. |
| pii_attribute_id | 6.3.5.3 | (Optional Profile B1) | Map | Attribute identifiers are an implementation detail within B1 schemas; maintain stable identifiers where possible. |
| pii_optional | 6.3.5.4 | (Optional Profile B1) | Map | Optionality of PII disclosure is captured in B1 inventories and MAY be disclosed in the Notice Record where required for meaningful choice. |
| sensitive_pii_category | 6.3.5.5 | (Optional Profile B1) | Map | Sensitivity classification is processing-record scope (B1) and MAY be disclosed in the Notice Record where required by jurisdiction/sector. |
| special_pii_category | 6.3.5.6 | (Optional Profile B1) | Map | Special-category classification is processing-record scope (B1) and MAY be disclosed in the Notice Record where required by jurisdiction. |
| party_address | 6.3.6.3 | controller_address (CIR) | Map | Controller address may be carried in CIR; for other parties, use TS party identification where B1 requires inventories. |
| party_email | 6.3.6.4 | privacy_access_point (CIR) | Map / refactor | Email is represented as a modality entry in privacy_access_point. |
| party_url | 6.3.6.5 | controller_public_id_uri | Map / specialize | Profile distinguishes a public controller identifier URI (controller_public_id_uri) and may also include general web URLs in CIR extensions. |
| party_phone | 6.3.6.6 | privacy_access_point (CIR) | Map / refactor | Phone is represented as a modality entry in privacy_access_point. |
| party_role | 6.3.6.8 | (CIR scoping) | Constrain | CIR represents the controller role; other roles MAY be represented in B1 party inventories using TS party_role values. |
| party_type | 6.3.6.10 | (Optional CIR extension) | Map | Party type may be carried as an optional CIR extension where useful for accountability classification. |

## A.2 Artefact-to-27560 TS mapping

| Base extension record | Primary purpose | ISO/IEC TS 27560:2023 anchor | Notes / deltas |
| --- | --- | --- | --- |
| Controller Identification Record (CIR) | Controller accountability anchor (controller-id-first) | Party identification (controller role) | Profiled subset of party fields + required pointers (rights access, event log, publication) |
| Notice Record (versioned) | Machine-readable notice content + version binding | Consent record context (notice/policy content reference) | Adds explicit immutable notice version reference (notice_version_reference) |
| First Notice Receipt | Evidence of disclosure (anonymous-bydefault) | Consent receipt / record header + context | First notice receipt explicitly removes pii_principal_id requirement; receipt is initially versionbound |
| Notice Event Log | Lifecycle and material change events | Event / lifecycle elements (event log / change record) | Adds minimum event type expectations + tiering note |

## A.3 CIR mapping

| CIR field (base extension) | TS 27560:2023 anchor (exact) | Change type | Notes |
| --- | --- | --- | --- |
| controller_public_id_uri | TBD (Party identification fields) | Constrained | Public resolvable controller identifier (URI form); profiled as required |
| controller_name | TBD (Party name fields) | Constrained | Controller legal name; profiled as required |
| jurisdiction | 6.3.4.17 jurisdiction (PII processing) | New | Controller-asserted applicable jurisdiction (or pointer). Closest TS anchor is the PII processing jurisdiction field. |
| privacy_access_point | TBD (Contact / rights contact fields) | Constrained | Structured modalities (web/email/phone/etc.); profiled as required and structured |
| notice_event_log_url | TBD (Event / lifecycle reference) | New | Pointer to the append-only Notice Event Log |

## A.4 Notice Receipt mapping

| Notice Receipt field (base extension) | 27560:2023 anchor | Notes |
| --- | --- | --- |
| schema_version | schema_version | Required in TS receipt metadata; required in this profile’s receipt header. |
| receipt_id | Record identifier | Receipt instance identifier |
| anchored_notice_receipt (indicator) | N/A | New indicator field to classify a receipt instance as the First Notice Receipt. |
| anchored_notice_receipt_id (reference) | N/A | New linkage field; subsequent receipts reference the applicable First Notice Receipt. |
| notice_id | Notice/receipt linkage | Stable notice family identifier |
| notice_version_reference | Notice reference | Immutable reference to disclosed notice version |
| controller_identity_record_id | Party identification | Links receipt to CIR |
| presented_at (event_time) | Event / record time | Time of disclosure/presentation |
| notice_type | Context | Notification/disclosure/policy/signal (vocabulary defined by the extension) |
| account_id (optional) | pii_principal_id | Profile replaces TS-required pii_principal_id with optional account_id for relationship context (pseudonymous where applicable). |

## A.5 Notice Event Log mapping

| Event Log element (base extension) | 27560:2023 anchor | Notes |
| --- | --- | --- |
| notice_issued | Event type | Stage 1 disclosure issuance event |
| notice_material_change | Event type | Material change triggers new notice version and new receipt issuance |
| tiering note | Conformance guidance | Allows assurance-tiered event-log requirements with explicit tier declaration |

## Annex B - Optional profile extensions

This annex defines two optional profile extensions that build on ISO/IEC TS 27560:2023 while preserving the base extension’s reference integrity and “reciprocal and proportionate” transparency requirements.

### B.0 Extension discipline

Any record created under the optional profiles in this annex:

- SHALL preserve base identifiers and version binding (notice_id + notice_version_reference).
- SHALL NOT redefine Stage 1 (first) notice/receipt semantics.
- SHALL reference the Controller Identification Record (CIR) via controller_identity_record_id.

### B.1 Optional Profile B1: PII Processing Record structure (controller/processor governance)

**Purpose:** Add a RoPA-aligned, controller/processor-side processing record structure that is traceable to the disclosed notice version(s).

#### B.1.1 Minimum conformance requirements (normative)

A conforming B1 processing record:

- SHALL include a unique processing_record_id.
- SHALL include controller_identity_record_id (CIR reference).
- SHALL include notice_id + notice_version_reference for every disclosed processing fact relied upon.
- SHALL include lawful_basis and SHALL use the Annex C vocabulary.
- SHOULD reference Notice Event Log entries where material change, withdrawal/objection, or scope escalation is relevant.

#### B.1.2 How to extend ISO/IEC TS 27560:2023 with B1

Use TS 27560:2023 as the baseline for:

- party identification (controller role): profile it into CIR and reference it by controller_identity_record_id;
- event_time semantics: align record creation/update events with the Notice Event Log;
- processing purposes, recipients, and retention: reuse TS-style field naming where practical, but ensure each processing claim is bound to notice_version_reference.

### B.2 Optional Profile B2: Personal Processing Record structure (individual-held)

**Purpose:** Add an individual-held, data-minimizing personal evidence record that is portable and supports rights exercise.

#### B.2.1 Minimum conformance requirements (normative)

A conforming B2 personal record:

- SHALL include a unique personal_record_id.
- SHALL include notice_id and notice_version_reference (the evidence model).
- SHALL include controller_identity_record_id (CIR reference).
- SHALL include privacy_access_point (or a reference to it via CIR) sufficient to exercise rights.
- SHALL support anonymous or pseudonymous operation by default.
- MAY include receipt_id as a pointer to a specific receipt instance; when present it SHOULD be accompanied by notice_version_reference.

#### B.2.2 How to extend ISO/IEC TS 27560:2023 with B2 Personal processing record

Treat the TS receipt as the exchange artefact and the B2 record as the individual-held record or “wallet architecture”:

- Keep B2 minimal (references first; no replication of full processing inventories).
- When B2 stores additional details, they SHOULD be derived from the TS receipt fields (or TS-compatible receipt extensions) and remain unlinkable unless the individual chooses otherwise.

## B.4 Relationship to companion specifications

Cross-border security and AI lifecycle governance requirements SHOULD be specified in the companion documents, not in this annex:

- [Cross-border transfer mechanisms: alignment to be tracked against ISO/IEC 27091 Annex B.4 (operational transparency) and 27566-2 Annex F practice statements]
- [AI lifecycle governance: alignment to be tracked against ISO/IEC FDIS 27091 (AI cybersecurity and privacy) and ISO/IEC 42001]

## Annex C - Lawful basis variants: rights and obligations table (normative)

This annex defines the lawful basis vocabulary and a minimum rights/obligations disclosure table for lawful-basis interoperability. Implementations SHALL reference the applicable row via lawful_basis in the First Notice Receipt header.

| lawful_basis (value) | Meaning (high level) | Rights commonly triggered | Controller obligations commonly triggered | Receipt/header requirements (minimum) |
| --- | --- | --- | --- | --- |
| consent | Processing based on meaningful choice by the individual | Withdrawal; access; rectification; erasure (where applicable); objection (where applicable) | Record evidence of consent; enable withdrawal; ensure freely given/specific/informed/unambiguous; avoid coercion; demonstrate proof | 2FN MAY be used; a bilateral receipt does not by itself evidence consent (see 7.2.2) |
| contract | Processing necessary for contract performance or steps at request of the individual | Access; rectification; objection/complaint pathways; portability where applicable | Disclose necessity scope; limit processing to contract purposes; document retention aligned to contract | Header SHALL assert contract and identify the contractpurpose scope covered by the notice version |
| legal_obligation | Processing necessary to comply with a legal obligation | Access and explanation; complaint/appeal pathways; restrictions where lawful | Identify the obligation authority; document statutory basis; apply minimization; disclose retention mandates | Header SHALL assert legal obligation and provide authority reference (law/regulation/court order) or pointer |
| legitimate_interest | Processing necessary for legitimate interests balanced against the individual’s rights | Right to object; access; explanation; complaint/appeal pathways | Document balancing/necessity; provide objection mechanism; apply safeguards and minimization | Header SHALL assert legitimate interest and provide a pointer to the balancing rationale or summary |
| vital_interest | Processing necessary to protect vital interests | Access and explanation after the fact (where applicable) | Document emergency necessity; limit scope and duration; later notice and accountability | Header SHALL assert vital interest and record emergency context constraints |
| public_interest | Processing necessary for a task carried out in the public interest or under official authority | Access; explanation; objection/appeal pathways as applicable | Identify authority; define task scope; apply proportionality; enable oversight mechanisms | Header SHALL assert public interest and provide authority/task reference or pointer |

## Annex D - Use of the receipt in a four-stage exchange (informative)

This annex describes a staged exchange pattern (commonly referred to as an ANCR-style exchange) in which a Notice Receipt is used as the evidence architecture across multiple stages. This annex is informative; it does not define protocol mechanics.

### D.1 Stage 1: Anchored Notice Receipt (notice disclosure proof)

Purpose: establish bilateral evidence that a specific notice version was disclosed/presented, suitable for dispute resolution and (when the lawful basis is consent) valid legal consent proof-of-notice.

Minimum binding identifiers:

- `receipt_id`
- `notice_id`
- `notice_version_reference`
- `controller_identity_record_id`
- `presented_at`

Optional linkage fields:

- `anchored_notice_receipt` (true)

### D.2 Stage 2: Authorization receipt (basis-dependent)

Purpose: express an authorization state (e.g., consent, contract acknowledgement, legal obligation acknowledgement) that is explicitly linked to the Stage 1 Anchored Notice Receipt.

Interoperability rule: a Stage 2 receipt SHOULD reference the Stage 1 Anchored Notice Receipt using `anchored_notice_receipt_id` (or by reusing `receipt_id` where a single receipt instance is updated in-place by the implementation).

### D.3 Stage 3: Micro credential (protocol-facing)

Purpose: represent Stage 2 authorization as a credential or signed assertion suitable for protocol enforcement (e.g., API/device authorization) without resharing full receipt content.

Interoperability rule: any Stage 3 credential SHOULD carry (or be derivable from) the binding identifiers of Stage 1 (`controller_identity_record_id` + `notice_version_reference` + `receipt_id`) to prevent ambiguity and replay across relying parties.

### D.4 Stage 4: Portable token (portability)

Purpose: enable portability and re-use of authorization state across controllers and jurisdictions, subject to scope limits and revocation/withdrawal controls.

Interoperability rule: any Stage 4 token SHOULD be traceable to Stage 1 via the binding identifiers and SHOULD include (or reference) a status pointer that enables relying parties to verify whether the Stage 1 notice version and the Stage 2 authorization remain active.

### D.5 Lifecycle and invalidation

Where staged exchanges are used, implementations SHOULD record lifecycle events (issuance, material change, withdrawal/objection, expiry, supersession) in the Notice Event Log so that credentials/tokens derived in Stages 3 and 4 can be invalidated or superseded when the underlying notice or authorization state changes.

## Annex E - TPI-R conformance and compliance profile (informative)

This annex maps the normative artefacts of this document to the Transparency Performance Indicator Report (TPI-R) methodology, for use by an implementer, auditor, or regulator assessing a deployed implementation. TPI-R is a measurement tool applied to this specification. It is not a requirement of this document.

### E.1 Purpose

TPI-R is an external assessment methodology that scores how well a live deployment realises the transparency artefacts a standard such as this one specifies. It evaluates four indicators, each independently testable against observable evidence, combined into a composite score:

TPI-R = (TPI-1 x 0.30) + (TPI-2 x 0.25) + (TPI-3 x 0.25) + (TPI-4 x 0.20)

The composite produces a rating from Glass-Box (full transparency) to Blackbox (severe non-compliance). A second variant, ANCR TPI-R, extends the four indicators with conformance indicators that test the presence and integrity of the artefacts this document specifies: the Controller Identification Record, the Notice Receipt, the Anchored Notice Receipt, and the Notice Event Log.

Which variant, Kantara TPI-R or ANCR TPI-R, becomes canonical for this extension is a working group decision to be recorded here. This annex does not settle TPI-R versions.

### E.2 Indicator mapping

| Indicator | What it measures | Evidence in this document |
| --- | --- | --- |
| TPI-1 Timing | When notice is available relative to identification and processing | Sequence condition (1 Scope; 5.1 C1); minimum notice disclosure (3.12); presented_at (7.3.2) |
| TPI-2 Required elements | Whether the required disclosure elements are present | Minimum notice disclosure (3.12); CIR field set (7.1.1, 7.1.1A); Notice Receipt fields (7.3.2); purpose (7.5) |
| TPI-3 Accessibility | Whether the required information is reachable without obstruction | privacy_access_point (7.1.2); non-exclusion (3.14, 5.1 C7); publicly retrievable disclosure set (7.2.1) |
| TPI-4 Security integrity | Whether session security metadata is consistent with the disclosed notice | notice_version_reference immutability (6.3); Anchored Notice Receipt binding (3.3, 7.3); Notice Event Log (7.4) |
| ANCR: CIR | Presence and resolvability of the CIR | 7.1, 7.1.1A |
| ANCR: Notice Receipt | Presence of a conforming Notice Receipt | 7.3.2 |
| ANCR: Anchored Notice Receipt | Presence and binding of the Anchored Notice Receipt | 7.3, 3.3 |
| ANCR: Notice Event Log | Presence of lifecycle event records | 7.4 |

### E.3 Scope boundary

A TPI-R score is a compliance and conformance signal. It is not a conformance claim under this document. A conforming implementation is defined by the mandatory requirements in Clause 8 and the conformance criteria in 5.1. TPI-R measures how well a live deployment realises that conformance in practice, which can diverge from the specification text.

### E.4 Attribution

TPI-R is cited by its published methodology name, Transparency Performance Indicator Report, of Kantara Initiative and Digital Transparency Lab origin. The ANCR TPI-R variant referenced here is the Anchored Notice and Consent Receipt profile of that methodology.


