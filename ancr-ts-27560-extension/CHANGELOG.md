# CHANGELOG: ANCR ISO/IEC TS 27560:2023 Notice record extension

This changelog records revisions to `27560 TS Notice Receipt Extension.md`. Until a canonical version is assigned by the ANCR Working Group, cite this document by its Git commit hash, not by a bare version string. Version numbers are not interchangeable across artefacts.

## [Unreleased]

### Restored
- Restored the complete document body from the authoritative local source. The published upstream file was truncated at the end of clause 6.3 and was missing clause 7 (Notice record specifications 7.1 to 7.4, including the CIR field table, the Notice Receipt field table, and the Notice Event Log), clause 8 (Mandatory requirements), and Annexes A, B, C, and D. These are now present.

### Changed
- Clause 1 (Scope): replaced the claim that TS 27560:2023 "adopted the Consent Receipt specification, which is completed here" with a contribution formulation: "an ISO technical specification to which the Consent Receipt specification was contributed, and which this profile extends." Rationale: the profile does not complete an ISO deliverable.
- Foreword: corrected the cross-reference list so ISO/IEC WD 27566-2 is described as comments submitted, not a contribution to "Annex F." ISO/IEC TS 27568 remains listed as a contribution; FDIS 27091 Annex B.4 and ISO/IEC 27560 are unchanged.

### Fixed (editorial)
- Standardised the acronym for co-regulated digital identification to CDRI throughout the Introduction (removed the CDRI/CRDI inconsistency).
- Corrected a broken sentence in the Introduction ("...assert claims about a person is called surveillance") into two sentences.
- Added clause 4 "Symbols and abbreviated terms".
- Renumbered the mislabelled "6.3.2 Required identifiers" heading to 7.3.3, its correct position within clause 7.
- Reworded the clause 7.2.1 disclosure-set text to list its elements directly instead of by a self-reference to clause 7.2.1.
- Corrected "ISO 31661" to "ISO 3166-1" in the recipient_jurisdictions field.
- Changed "MUST NOT" to "SHALL NOT" in the account_id constraint, consistent with the keyword note in clause 2.2.
- Corrected the "Annex B. 4" heading spacing to "B.4" and the matching cross-reference to ISO/IEC 27091 Annex B.4.
- Reworded the receipt-reuse sentence in clause 7.2.2 to a formal register.
- Removed a stray open parenthesis from the Annex A.2 heading.

### Added
- Revision line: instruction to cite by commit hash until a canonical version is fixed.

### Added (seeding-document update, per the external-facing brief)
- Clause 1: adopted the extension-voice scope statement (notice evidence artefacts for inspectable, verifiable digital transparency; does not replace 29184 or TS 27560; does not redefine consent).
- Clause 1.1 (informative): what this document enables others to standardize, worded as enablement only, no downstream document named, no commitment or dependency.
- Introduction: authority sequence stated once, in order (Convention 108+, 29100, 29184, TS 27560, minimum notice disclosure and anonymity by default, Transparency by Default).
- Clause 3: added defined terms 3.15 notice, 3.16 online notice, 3.17 digital transparency, 3.18 consent, 3.19 online consent, 3.20 permission, 3.21 consent record, 3.22 two-factor online notice (2FN), each with notes to entry and no SHALL. Removed the SHALL from 3.12; the normative requirement stays in 5.1 C2.
- Clause 4: symbols clause resolves CIR, ANCR, CDRI, MVCR, 2FN; 1FN not listed.
- Clause 7.4.4: processing events specified distinctly from notice lifecycle events, with a minimum processing event record.
- Clause 7.5: purpose specified as a recorded artefact, bound to legal authority, controller, and notice version. Unrecorded purpose is stated as a security defect in a note, with the conformance consequence in Clause 8.
- Clause 7.6: relationship to consent records specified as a reference to the prior notice disclosure event only.
- Clause 8: added mandatory requirements 7 (purpose) and 8 (processing events).
- Clause 7.3.2: added a purpose field to the Notice Receipt field specification table, bound to notice_version_reference and the controller, per 7.5.
- Clause 7.1.1A: corrected the duplicate 7.1.1 subclause number to 7.1.1A (the CIR field specification table).

### Terminology
- "terminology bridge" changed to "interoperability"; "lifecycle spine" and "evidence spine" changed to Notice Event Log and evidence model. The 2FN meaning is kept as two-factor online notice; 1FN is not introduced (see the 1FN/2FN collision decision in the brief).

### Added (separate proposal): TPI-R conformance appendix
- Annex E (informative): TPI-R conformance and compliance profile. Maps the extension's artefacts to the four TPI indicators (Timing, Required elements, Accessibility, Security integrity) and to the ANCR conformance indicators (CIR, Notice Receipt, Anchored Notice Receipt, Notice Event Log). E.3 states that a TPI-R score is a signal, not a conformance claim (conformance is defined by Clause 8 and 5.1). The choice between Kantara TPI-R and ANCR TPI-R is left as a working group decision recorded in E.1. Informative only; adds no normative requirement and no downstream dependency.

### Open for the editor
- The field name `controller_identity_record_id` retains "identity" while the referenced artefact is the Controller Identification Record. Decision: keep the field name for this version, with an explaining note in 7.1; align it to "identification" in a future version.
