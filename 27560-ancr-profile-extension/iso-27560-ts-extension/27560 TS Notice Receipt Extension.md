# ANCR Extension for ISO/IEC TS 27560:2023

Anchored Notice and Consent Receipts for Operational Transparency, a consent receipt extension for TS 27560:2023 - [Posted](https://github.com/KantaraInitiative/ancr-wg/blob/d1a92ce689243708083e5723f02728b0cc00d810/27560%20ancr%20profile%20extension/ISO-27560%20TS%20Extension%20/27560%20TS%20Notice%20Receipt%20Extension.md)

**Revision:** v0.3. Complete text revised to the co-regulated identification frame, with the editorial and structural corrections recorded in CHANGELOG.md.

## Foreword

This document specifies a notice receipt information structure that profiles and extends ISO/IEC TS 27560:2023 (consent record information structure). It is published by the Kantara Initiative and the Anchored Notice and Consent Receipt (ANCR) Working Group as a companion specification, and is intended to be cited as prior art and an implementation reference for SC 27/WG 5 work that depends on machine-readable notice and consent records (notably developed through contributions to ISO/IEC 27560, ISO/IEC TS 27568, FDIS 27091 Annex B.4, and ISO/IEC WD 27566-2 Annex F).

IPR Note: This ANCR Record Specification is required to be open, as specified under a Patent & Copyright: Reciprocal Royalty Free with Opt-out to Reasonable and Non-discriminatory (RAND) license agreement at the Kantara Initiative chartered to contribute the completed consent receipt work to ISO/IEC SC 27 WG 5.

## Introduction

Governing ones own identity digitally confident of privacy requires identifiers to be transparent, bound to a recorded artefact that can be referenced after the fact. Historically, such identifiers have been encapsulated in a record and provided in receipt of an event by context at a time and place. The notice receipt acts as a container not only for identifiers, but for the integrity of the claim that the identifiers represent and link to as real world objects.

A notice receipt is generated through interaction (or a lack of interaction) with a physical sign, access point, a device or an online notification or statement. A notice receipt can be generated independently by an individual, from the notice by creating or accessing a controller identification record to produce a proof of notice disclosure that can be exchanged between devices and across borders.

Co-regulated digital identification (CDRI). This profile is specified for co-regulated identification. Co-regulation means a standard public policy, with two rule sets that operate on the same identifier at the same time: the controller's own rules, expressed in service terms, technical design, and internal policy; and the public rules, expressed in treaty, law, and standards. Neither self-regulation nor state regulation alone governs identification at internet scale for a number of reasons. Self-regulation leaves the identifier privately defined. State regulation alone lacks operational artefacts that can be inspected at the time of interaction. This profile supplies the record structure through which the public rule set becomes machine readable, inspectable, and enforceable.

For online decentralised and human operated data governance Identity and identification must be technically distinct. Identity is self-expression and self-identification, and is managed by the individual. Identification on the other hand is the technical and organizational process a controller uses to discover, link, or assert claims about a person is called surveillance. Hence in CRDI, Consent is a human expression, an interaction managed by humans; permissions on the other hand are managed by organisations and systems. Where these are conflated, interface permission is presented as consent. This profile keeps them separate by requiring controller identification, and the notice bound to it, before any demand for personal identification.

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

## 1 Scope

This profile extends ISO/IEC TS 27560:2023 (consent record information structure), which is an ISO technical specification that adopted the Consent Receipt specification, which is completed here. It is used to specify a machine-readable online Notice Record and corresponding Notice Receipt that provide durable evidence of notice disclosure.

This profile specifies the record structure through which identification is co-regulated. Controller identification SHALL precede any demand for personal identification, and the artefacts specified in clause 7 SHALL be inspectable independently of any personal identifier. Where an implementation demands personal identification before a resolvable Controller Identification Record and its bound notice version are available, that implementation does not conform to this profile.

It supports layered and sequenced notices, notifications, and disclosures. Anchored Notice Receipt requirements are legal basis agnostic. When the lawful basis is consent, a corresponding authorization can be represented as a TS 27560:2023 consent receipt specialisation.

The base notice record extension defines a minimum interoperable set of notice artefacts for operational transparency:

- Controller Identification Record (CIR)
- Notice Record / Anchored Notice Receipt
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

## 2 Normative references

- ISO/IEC TS 27560:2023 Privacy technologies: Consent record information structure
- ISO/IEC 29100, Privacy framework

### 2.1 Other references (informative)

- ISO/IEC 29184, Online privacy notices and consent
    - Note: free and open access to this standard is required for it to be listed as normative, or would block the use of 27568 directly, although it can be used for control interoperability between 27560 TS Extension Profiles.

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

Smallest set of disclosures that SHALL be present, resolvable, and inspectable before identification or processing begins, comprising the Controller Identification Record, the notice version in effect, the asserted lawful basis, the scope of disclosure, and the privacy access point.

### 3.13 anonymity by default

Property whereby notice disclosure and the resulting evidence artefacts are generable, retrievable, and verifiable without identification of the individual, and without an account_id or pii_principal_id.

Note 1 to entry: Anonymity by default applies to the notice and evidence layer. It does not restrict identification that is required by the lawful basis for the processing itself.

Note 2 to entry: Retrieval of a Controller Identification Record is not an identification event, see 7.1.

### 3.14 non-exclusion

Property whereby the minimum notice disclosure and the routes to recourse are reachable through at least one privacy_access_point modality that does not require the individual to hold, present, or authenticate a digital identification credential.

Note 1 to entry: Non-exclusion addresses accessibility needs, low or absent connectivity, delegated and assisted interaction, and in person contexts where notice and identity are physically verifiable.

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
- **Factor 2, evidence receipt:** An Anchored Notice Receipt is generated to provide durable evidence that a specific notice version was presented or available at a specific time and, when the lawful basis is consent, to support proof of informed consent by binding the authorization state to the disclosed notice version.

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