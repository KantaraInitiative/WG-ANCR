# CHANGELOG: ANCR ISO/IEC TS 27560:2023 Notice record extension

This changelog records revisions to `27560 TS Notice Receipt Extension.md`. Until a canonical version is assigned by the ANCR Working Group, cite this document by its Git commit hash, not by a bare version string. Version numbers appearing across the file tree (v0.3), the archive (v1.02), the N-docs (v1.05, v1.06), and the Blueprint (v1.07.1) refer to different artefacts and are not interchangeable.

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
- Revision line: instruction to cite by commit hash until a canonical version is fixed, with an explicit note on the version collision across artefacts.
- Informative editorial note recording the three deliberate positions on "minimum notice disclosure" (live at 3.12 and C2 in this extension, retired in the PWI 26689 brief, reinstated by Blueprint v1.07.1 item 9).
