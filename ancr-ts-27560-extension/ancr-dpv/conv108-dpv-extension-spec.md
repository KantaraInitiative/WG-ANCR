# Convention 108+ DPV Style Legal Model Extension

**External review draft**

**Author and editor:** Mark Lizar  

**Version:** 0.2 draft  

**Date:** 28 August 2026  

**Review context:** Prepared for technical review in relation to the ANCR Working Group at Kantara Initiative. This attribution does not imply endorsement, adoption, or authorship by Kantara Initiative, the ANCR Working Group, the W3C Data Privacy Vocabularies and Controls Community Group, the Council of Europe, ISO, or IEC.

## Abstract

This document proposes a DPV style model for representing selected requirements of the modernised Convention 108 in machine readable notice and consent records. It also defines evidence based acceptance criteria for digital and open network contexts.

The proposal distinguishes three concepts:

- **Consent:** an individual's freely given, specific, informed, and unambiguous authorization where consent is the applicable legal basis.
- **Permission:** a technical control enforced by a system after the applicable authority has been established.
- **Identification:** information or processes used to distinguish or recognize a party. Identification is not consent or permission.

The proposed model supports three related artefacts: a machine readable notice or consent receipt, a resolvable Controller Identification Record (CIR), and a transparency code of practice. Together, these artefacts are intended to make the accountable party, purpose, legal basis, recipients, rights mechanisms, and record state inspectable.

## 1. Scope and status

This document:

1. provides a traceable modelling structure based on the modernised Convention 108;
2. uses established DPV terms where suitable and labels every proposed term;
3. defines testable acceptance criteria for evidence carried in notice and consent records; and
4. describes alignment with ISO/IEC TS 27560:2023 and related standards.

This document is an independent draft. It is not an official Council of Europe text, W3C DPVCG deliverable, Kantara Initiative recommendation, or ISO/IEC publication. It does not replace DPV specifications or the published DPV guidance for ISO/IEC TS 27560:2023. References to standards and community specifications indicate alignment only.

The Convention 108+ article references identify relevant source provisions. Proposed technical requirements that go beyond the treaty text are identified as implementation requirements, not treaty obligations.

## 2. Proposed namespace

Proposed namespace and prefix for the Convention 108+ legal-model extension:

conv108: [https://w3id.org/dpv/legal/int/conv108plus#](https://w3id.org/dpv/legal/int/conv108plus#)

The proposed IRI uses `conv108plus` because a literal plus sign can be re-encoded by intermediaries. The short prefix remains `conv108`. The proposed namespace is not registered or published by W3C or the DPVCG.

Companion namespaces reused (not redefined here). This extension reuses core DPV and its modules rather than duplicating terms:
Prefix	Namespace	Reused for
dpv	[https://w3id.org/dpv#](https://w3id.org/dpv#)	controller, purpose, personal data, legal basis, rights, timing
pd	[https://w3id.org/dpv/pd#](https://w3id.org/dpv/pd#)	personal-data categories
loc	[https://w3id.org/dpv/loc#](https://w3id.org/dpv/loc#)	processing / destination locations
tech	[https://w3id.org/dpv/tech#](https://w3id.org/dpv/tech#)	technical / processing detail
dct	[http://purl.org/dc/terms/](http://purl.org/dc/terms/)	title, description, issued, modified
dcat	[http://www.w3.org/ns/dcat#](http://www.w3.org/ns/dcat#)	version
ancr	(ANCR extension, alignment reference)	receipt / record structure, notice-event object

New terms are proposed only where an existing DPV term does not express the required concept.

## 3. Convention 108+ legal model

### 3.1 Legitimacy and purpose compatibility

Article 5.2 provides for processing based on the individual's free, specific, informed, and unambiguous consent or another legitimate basis laid down by law. Article 5.4(b) separately requires explicit, specified, and legitimate purposes and prohibits incompatible further processing, subject to the stated exceptions and safeguards.

The model therefore keeps legal basis and purpose compatibility separate:

| **Proposed term** | **DPV relationship** | **Convention 108+ anchor** | **Meaning** |
| --- | --- | --- | --- |
| `conv108:ConsentBasis` | Specialization of `dpv:Consent` | Article 5.2 | Consent used as the legal basis for a specified purpose |
| `conv108:OtherLegitimateBasisUnderLaw` | Specialization of `dpv:LegalBasis` | Article 5.2 | Another legitimate basis established by applicable law |
| `conv108:CompatibleFurtherProcessing` | Proposed processing condition, not a legal basis | Article 5.4(b) | A recorded determination that further processing is compatible with the original purpose |

This proposal does not create Convention 108+ legal bases for legal obligation, legitimate interests, accountability, or transborder safeguards. Any more specific legal basis must be established under the applicable law. Article 8 transparency and Article 14 transborder safeguards are represented as requirements, not legal bases.
⸻
4. Principles, rights, and transparency requirements (DPV-style)

4.1 Principles

Convention 108+ principles expressed as conv108: classes for reference by a record. These are modelling handles for the articles, not new obligations.
Term (proposed)	Convention 108+ anchor	Principle
conv108:LawfulnessPrinciple	Article 5.1 to 5.3	Lawful and proportionate processing that reflects a fair balance of interests, rights, and freedoms
conv108:PurposeSpecificationPrinciple	Article 5.4(b)	Explicit, specified, and legitimate purposes; no incompatible further processing
conv108:DataMinimisationPrinciple	Article 5.4(c)	Adequate, relevant, and not excessive
conv108:TransparencyRequirement	Article 8	Required information about the controller and intended processing
conv108:TransborderProtectionRequirement	Article 14	Appropriate protection for transborder data flows

4.2 Rights

Rights are expressed DPV-style via dpv:hasRight with conv108: subclasses of dpv:DataSubjectRight, each anchored to Article 9.
Term (proposed)	Convention 108+ anchor	Right
conv108:RightOfAccess	Article 9.1(b)	Confirmation of processing, communication of personal data in an intelligible form, and available information concerning origin, preservation period, and other required details
conv108:RightAgainstSolelyAutomatedDecision	Article 9.1(a)	Not to be subject to a decision significantly affecting the individual when based solely on automated processing, without the individual's views being taken into consideration
conv108:RightToKnowAutomatedReasoning	Article 9.1(c)	To obtain knowledge of the reasoning underlying relevant automated processing results
conv108:RightToObject	Article 9.1(d)	To object on grounds relating to the individual's situation, subject to the conditions in the Convention
conv108:RightToRectificationOrErasure	Article 9.1(e)	To obtain rectification or erasure where processing does not comply with the Convention

A consent withdrawal route may be included as an ISO/IEC TS 27560 aligned consent lifecycle requirement. It is not attributed here as an express Article 9 right under Convention 108+.

4.3 Transparency requirements

Transparency requirements express the synchronic property: what must be inspectable, and when, expressed with DPV timing terms (dpv:isBefore, dpv:isDuring) relative to dpv:Collect.
Term (proposed)	Source	Requirement
conv108:TransparencyInformation	Convention 108+ Article 8	Controller identity and establishment, legal basis, purposes, personal data categories, recipients, rights mechanisms, and any additional information needed for fair and transparent processing
conv108:TransparencyBeforeCollection	Implementation requirement aligned with Transparency by Default	Required transparency information is resolvable before the first collection event
conv108:TransborderTransparency	Convention 108+ Article 14 plus implementation requirement	Destination and applicable safeguard information are resolvable before transfer
conv108:AutomatedProcessingTransparency	Convention 108+ Article 9.1(a) and 9.1(c) plus implementation requirement	Relevant automated decision scope and reasoning information are available in time for the individual to exercise applicable rights
conv108:DualHeldRecordRequirement	ISO/IEC TS 27560 and ANCR alignment	A record of what was presented is available to the individual as well as the controller

The timing and dual custody requirements are technical design requirements. They are not presented as verbatim Convention 108+ obligations.
⸻
5. The Controller Identification Record (CIR): accountability expressed (Art 8)

The CIR is a proposed implementation artefact for expressing the controller information required by Article 8. It is published by the controller and is designed to make the accountable party resolvable before the individual is asked to identify themselves. The CIR reuses DPV controller terms and adds proposed implementation properties:
Field	DPV / conv108 expression	Convention 108+ / I-anchor
Controller identity	dpv:hasDataController + dpv:hasIdentifier (e.g. did:web:)	Art 8; I1
Privacy contact point	dpv:hasContact (schema:ContactPoint)	Art 8
Lawful basis per purpose	dpv:hasLegalBasis → conv108:*	Article 5.2; I2
Purposes, including any model training purpose	dpv:hasPurpose + conv108:CompatibleFurtherProcessing where applicable	Article 5.4(b); I3, I4
Processing / destination locations	dpv:hasLocation (loc:)	Art 14; I8
Transborder safeguard	conv108:hasTransborderSafeguard	Art 14; I8
Rights access reference	conv108:hasRightsAccessReference	Art 9; I10
Issuing authority + registry id	conv108:hasIssuingAuthority, conv108:hasRegistryIdentifier	registry; I14
Active validity state	conv108:hasActiveState	dynamic transparency; I15

A CIR may be self asserted or registry verified. The record must state its assurance status. A registry verified CIR may include evidence of domain control, legal entity verification, issuing authority, jurisdiction, and registry identifier. These are proposed assurance features, not requirements stated in Convention 108+.
⸻
6. New vs existing terms: legal-model layer

Honesty about what is reused vs proposed. Existing = already in DPV or a DPV module. Proposed = introduced by this extension (design layer, not adopted standard text).
Term	Status
dpv:hasLegalBasis, dpv:Consent, dpv:hasPurpose, dpv:hasPersonalData, dpv:hasLocation, dpv:hasRight, dpv:DataSubjectRight, dpv:hasDataController, dpv:hasIdentifier, dpv:hasContact, dpv:isBefore, dpv:Collect, dcat:version, dct:issued, dct:modified	Existing DPV: reused, not redefined
conv108:ConsentBasis, OtherLegitimateBasisUnderLaw	Proposed: Article 5.2 aligned legal basis classes
conv108:CompatibleFurtherProcessing	Proposed: Article 5.4(b) aligned processing condition, not a legal basis
conv108:*Principle (5 terms), conv108:RightTo* / RightOf* / RightAgainst* (6 terms)	Proposed (new): modelling handles for Conv 108+ Art 5, 8, 9, 14
conv108:TransparencyBeforeCollection, TransborderTransparency, AutomatedProcessingTransparency, DualHeldRecordRequirement	Proposed (new): transparency-timing requirements
conv108:hasTransborderSafeguard, hasRightsAccessReference, hasIssuingAuthority, hasRegistryIdentifier, hasActiveState	Proposed (new): CIR / registry properties
conv108:ChainOfNotice, hasNoticeParticipant, hasParticipantScope, hasLifecycleRole	Proposed (new): chain-of-notice (I16); hasLifecycleRole carries an ISO/IEC 22989 alignment-reference role value, not an adopted term

Note on I12 / I13 (ANCR field reuse). No conv108: term is minted for the notice version hash (I12) or the receipt identifier (I13). These reuse the existing ANCR field names notice_id plus notice_version_reference (I12) and receipt_id (I13) and are mapped in section 7.1. The earlier candidates conv108:hasNoticeVersionHash and conv108:hasReceiptIdentifier are retired to avoid minting conv108: duplicates of fields the ANCR extension already defines.

`conv108:CompatibleFurtherProcessing` is modelled separately from legal basis. Article 5.4(b) addresses compatibility of further processing with the original purpose. It does not itself supply a legal basis.
⸻
## 7. Proposed information set for dynamic data and AI systems

The I1 to I16 set is a proposed implementation profile. It combines treaty anchored information, standards aligned record fields, and new technical requirements. It must not be described as a requirement of Convention 108+, DPV, the EU AI Act, or ISO/IEC TS 27560 as a whole.
I#	Required information	DPV-style expression	Existing / New	Anchor
I1	Accountable party identity, resolvable before collection	dpv:hasDataController + dpv:hasIdentifier; conv108:TransparencyBeforeCollection	Existing (DPV) + New (timing req)	Conv 108+ Art 8; CIR
I2	Legal basis for each purpose	dpv:hasLegalBasis → conv108:ConsentBasis or conv108:OtherLegitimateBasisUnderLaw	Existing base + proposed specialization	Convention 108+ Article 5.2
I3	Legal basis and compatibility assessment for model training as further processing	dpv:hasLegalBasis + conv108:CompatibleFurtherProcessing	Existing base + proposed condition	Convention 108+ Article 5.2 and 5.4(b)
I4	Purpose(s), incl. training as named secondary purpose	dpv:hasPurpose (+ dct:title/dct:description)	Existing (DPV)	Conv 108+ Art 5; AI Act 53
I5	Training-data provenance / sources	conv108:hasTrainingDataProvenance	New	AI Act 53(1)(d)
I6	Copyright / machine-actionable rights-reservation status	conv108:hasRightsReservationStatus	New	AI Act 53(1)(c); Dir 2019/790 Art 4(3)
I7	Personal-data categories in training data	dpv:hasPersonalData (pd: categories)	Existing (DPV)	Conv 108+ Art 5-6
I8	Processing & disclosure locations / destination jurisdictions	dpv:hasLocation (loc:) + conv108:hasTransborderSafeguard	Existing base + New safeguard prop	Conv 108+ Art 14
I9	Automated decision scope and relevant reasoning information	conv108:AutomatedProcessingTransparency; conv108:RightAgainstSolelyAutomatedDecision; conv108:RightToKnowAutomatedReasoning	Proposed	Convention 108+ Article 9.1(a) and 9.1(c)
I10	Applicable rights mechanisms and, where consent is used, a consent lifecycle route	dpv:hasRight + conv108:hasRightsAccessReference	Existing base + proposed property	Convention 108+ Article 9; ISO/IEC TS 27560 alignment for consent lifecycle management
I11	Machine-readable record of I1-I10, held by >=2 parties	conv108:DualHeldRecordRequirement; ancr:Receipt (alignment)	New (+ ANCR alignment)	TS 27560 + ANCR
I12	Notice version reference + hash (notice as first-class object)	ANCR notice_id (stable family) + notice_version_reference (immutable, URI and/or hash)	Reused (ANCR): mapped, not re-minted	ANCR / TS 27560
I13	Receipt identifier carried with a training contribution	ANCR receipt_id (base record_id, renamed)	Reused (ANCR): mapped, not re-minted	ANCR extension
I14	Issuing authority + jurisdiction-scoped registry identifier	conv108:hasIssuingAuthority + conv108:hasRegistryIdentifier	New	CIR / registry
I15	Active-state / live validity (valid / invalid / suspended)	conv108:hasActiveState (enum: valid, invalid, suspended)	New	dynamic transparency
I16	Per-participant notice through the chain, bound to ISO/IEC 22989 AI-lifecycle roles	conv108:ChainOfNotice, conv108:hasNoticeParticipant (typed by conv108:hasLifecycleRole → 22989 role), conv108:hasParticipantScope	New	Chain-of-notice; ISO/IEC 22989 roles

### 7.1 Additional implementation requirements, I11 to I16

I11 to I16 are proposed design requirements. They are not attributed to Convention 108+, DPV, the EU AI Act, or adopted ISO text unless a specific field is explicitly identified as reused from another source.

- I11 conv108:DualHeldRecordRequirement: the record of I1-I10 is machine-readable and held by >=2 parties, so the affected person can produce it, not only the provider. Custody is the difference between disclosure-oriented and receipt-oriented transparency.
- I12: ANCR notice_id plus notice_version_reference: the notice becomes a first-class object with a stable family identifier and an immutable version reference, so "what was presented at time T" has an answer independent of the presenting party's goodwill or retention practice. The proposal reuses the ANCR field names and does not mint a duplicate `conv108:` property. The ANCR extension already defines notice_version_reference as an immutable reference to the disclosed notice version (URI and/or hash reference) bound to the exact notice version in effect at disclosure; that is exactly the version-plus-hash binding I12 needs. Mapping: this extension's "notice version reference plus hash" is ANCR notice_version_reference (carrying the immutable/hash binding), with ANCR notice_id supplying the stable notice-family identifier. No conv108:hasNoticeVersionHash term is introduced.
- I13: ANCR receipt_id: a receipt id carried with a training contribution, converting a consent claim into an artefact validatable before training and revisitable on withdrawal. Resolved: reuse ANCR receipt_id, do not mint a conv108: duplicate. In the ANCR extension receipt_id is the base ISO/IEC TS 27560 record_id field renamed for semantic clarity (receipt-instance tracking). Mapping: this extension's "receipt identifier" is ANCR receipt_id (base record_id). No conv108:hasReceiptIdentifier term is introduced.

ANCR field mapping (I12, I13): reuse, not duplication. I12 and I13 are carried by existing ANCR field names rather than fresh conv108: properties, and this extension only provides the mapping:
This extension's need	ANCR field reused	ANCR definition (source)	I#
Stable notice-family identifier	notice_id	Stable notice family identifier, stable across notice versions	I12
Immutable notice version reference + hash	notice_version_reference	Immutable reference to the disclosed notice version (URI and/or hash reference), bound to the exact version in effect at disclosure	I12
Receipt identifier for a contribution	receipt_id	Base TS 27560 record_id renamed for receipt-instance tracking	I13

The retired conv108:hasNoticeVersionHash and conv108:hasReceiptIdentifier proposals are removed from the term set; see section 6.

- I14 conv108:hasRegistryIdentifier: a jurisdiction-scoped identifier issued after registry verification, so a receipt issued under one authority can be evaluated against the authority claimed in another (cross-jurisdiction by construction).
- I15 conv108:hasActiveState: live validity (valid / invalid / suspended) evaluable in real time, because a receipt issued last month cannot represent a risk posture that changed last week. This is the dynamic-transparency requirement AI contexts add.
- I16 conv108:ChainOfNotice: notice per participant through the AI lifecycle, each notice bound to the participant that issued it and to the notice version it issued, and tested by the next participant before that participant relies on it. This proposal binds chain participants to ISO/IEC 22989 lifecycle role concepts rather than leaving the participant role unspecified. Each conv108:hasNoticeParticipant is typed by conv108:hasLifecycleRole naming the 22989 stakeholder / lifecycle role it acts in, so "who issued this notice, in which lifecycle role, at which version" is answerable from the record.

I16 chain-of-notice: ISO/IEC 22989 role binding. Chain participants map to the ISO/IEC 22989:2022 AI stakeholder / lifecycle roles as follows. Each role's notice is bound to the party acting in that role and to the notice version it issued; each downstream role tests the upstream notice before relying on it.
Chain stage	ISO/IEC 22989 role	Notice binding	Tested by
Design	AI provider acting as AI designer (sub-role of AI producer)	Notice bound to designer party + notice version	AI developer
Develop	AI provider acting as AI developer (sub-role of AI producer)	Notice bound to developer party + notice version	AI producer / trainer
Train / produce	AI producer (training / model production)	Notice bound to producer party + notice version, incl. training as Art 5.4 secondary purpose (I3)	AI operator / deployer
Deploy / operate	AI operator (deployer; toward the AI customer / AI user)	Notice bound to operator party + notice version	AI customer / AI subject (relying party)

The 22989 role labels are used as alignment references to name the participant's lifecycle role, not as adopted conv108: terms; conv108:hasLifecycleRole carries the role value. Where 22989 collapses several of these under "AI provider / AI producer", the chain preserves the finer stage (design vs develop vs train) so each notice-issuance point stays individually testable. If a deployment does not distinguish designer from developer, the stages may be merged, but the merge SHALL be explicit in the record rather than silently backfilled (see AC-SEQ-2).
⸻
## 8. Evidence based acceptance criteria

Each criterion is a testable condition on a record or receipt. Detailed test procedures may be maintained separately and referenced by criterion identifier.

8.1 Sequence integrity

- AC-SEQ-1: The CIR or accountable party record is resolvable at a timestamp before the first collection event. Evidence: the notice event or receipt timestamp precedes the first processing timestamp. This is a Transparency by Default implementation requirement aligned with the information listed in Article 8.
- AC-SEQ-2: Where a chain of notice is claimed (I16), each participant is typed by its ISO/IEC 22989 lifecycle role (conv108:hasLifecycleRole), each notice is bound to the issuing party + notice version, and each participant's notice timestamp precedes the next participant's build/test event. Ordering is verifiable, the next role in the chain has tested the upstream notice, and no gap or role merge is silently backfilled (any stage merge is explicit in the record). (I16; ISO/IEC 22989 roles)

8.2 Notice binding

- AC-BIND-1: The record carries a notice version reference (ANCR notice_version_reference, URI and/or hash) bound to the stable notice family (ANCR notice_id) and resolving to the notice text in force at the moment recorded. (I12; ANCR / TS 27560)
- AC-BIND-2: The legal basis for each purpose and any applicable further processing compatibility assessment are bound to the versioned notice. The record identifies the basis relied on, the purpose, and the relevant time. (I2 and I3; Article 5.2 and 5.4(b))

8.3 Receipt availability

- AC-RCPT-1: A receipt exists and is held by the individual (or an agent for them), not only the controller: the dual-held condition. (I11; conv108:DualHeldRecordRequirement)
- AC-RCPT-2: The receipt carries a receipt identifier (ANCR receipt_id, base TS 27560 record_id) that can be carried with a training contribution and re-resolved on withdrawal. (I13)

8.4 Recipient transparency

- AC-RECIP-1: Processing and destination locations (dpv:hasLocation) and, for transborder flows, the Art 14 safeguard (conv108:hasTransborderSafeguard) are resolvable in advance of the transfer. (I8; Art 14, conv108:TransborderTransparency)
- AC-RECIP-2: Automated-decision / inference scope (conv108:AutomatedProcessingTransparency) is disclosed before processing, making the Art 9.1.c right meaningful. (I9; Art 9.1.c)

8.5 Identifier governance

- AC-ID-1: The controller identifier resolves to an issuing authority (conv108:hasIssuingAuthority) and, where verified, a jurisdiction-scoped registry identifier (conv108:hasRegistryIdentifier). A self-asserted CIR is distinguishable from a registry-verified one. (I14; Art 8 / registry)
- AC-ID-2: The record's active state (conv108:hasActiveState) is evaluable in real time as valid / invalid / suspended; an expired or suspended state is detectable at the point of reliance. (I15; dynamic transparency)

## 9. Attribution and publication status

This document is an independent external review draft authored and edited by **Mark Lizar**. It was prepared for technical discussion in relation to the ANCR Working Group at Kantara Initiative. Kantara Initiative and the ANCR Working Group are not identified as authors or editors, and no endorsement or adoption is implied.

All `conv108:` terms are proposals in this document. They are not Council of Europe treaty text, published DPV terms, or ISO/IEC terms. Existing `dpv:`, `pd:`, `loc:`, `tech:`, `dct:`, and `dcat:` terms remain attributable to their respective specifications. The `ancr:` references identify an alignment target and do not claim a published namespace.

ISO/IEC TS 27560:2023 is correctly identified as a **Technical Specification** titled *Privacy technologies: Consent record information structure*. ISO/IEC 27091 is not quoted or analysed in this external draft because, as of 28 August 2026, it remains under development at the Final Draft International Standard stage.

## 10. References

- Council of Europe, [Convention 108 as it will be amended by Protocol CETS No. 223](https://rm.coe.int/16808ade9d).
- ISO/IEC TS 27560:2023, [Privacy technologies: Consent record information structure](https://www.iso.org/standard/80392.html).
- W3C Data Privacy Vocabularies and Controls Community Group, [Consent Records and Receipts as per ISO/IEC TS 27560:2023 using DPV](https://w3id.org/dpv/guides/consent-27560).
- ISO/IEC FDIS 27091, [Cybersecurity and Privacy: Artificial Intelligence: Privacy protection](https://www.iso.org/standard/56582.html).