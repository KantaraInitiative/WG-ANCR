# CHANGELOG — ANCR ISO/IEC TS 27560:2023 Notice record extension

This changelog records revisions to `27560 TS Notice Receipt Extension.md`. Until a canonical version is assigned by the ANCR Working Group, cite this document by its Git commit hash, not by a bare version string. Version numbers appearing across the file tree (v0.3), the archive (v1.02), the N-docs (v1.05, v1.06), and the Blueprint (v1.07.1) refer to different artefacts and are not interchangeable.

## [Unreleased] — body restoration

### Restored
- Restored the complete document body from the authoritative local source. The published upstream file was truncated at the end of clause 6.3 and was missing clause 7 (Notice record specifications 7.1 to 7.4, including the CIR field table, the Notice Receipt field table, and the Notice Event Log), clause 8 (Mandatory requirements), and Annexes A, B, C, and D. These are now present.

### Changed (authorized editorial fixes)
- Clause 1 (Scope): replaced the claim that TS 27560:2023 "adopted the Consent Receipt specification, which is completed here" with a contribution formulation: "an ISO technical specification to which the Consent Receipt specification was contributed, and which this profile extends." Rationale: the profile does not complete an ISO deliverable.
- Foreword: corrected the cross-reference list so ISO/IEC WD 27566-2 is described as comments submitted, not a contribution to "Annex F." ISO/IEC TS 27568 remains listed as a genuine contribution; FDIS 27091 Annex B.4 and ISO/IEC 27560 are unchanged.

### Added
- Revision line: instruction to cite by commit hash until a canonical version is fixed, with an explicit note on the version collision across artefacts.
- Informative editorial note recording the three deliberate positions on "minimum notice disclosure" (live at 3.12 and C2 in this extension, retired in the PWI 26689 brief, reinstated by Blueprint v1.07.1 item 9).

### Held (not applied — pending Mark's ruling as a separate decision)
The following ada80dc-review editorial defects were identified but deliberately NOT changed in this restoration, because they touch text marked "deliberately rough" in 27560-EXTENSION-FIXES.md and have not been ruled on:
1. Introduction surveillance sentence ("...assert claims about a person is called surveillance") — grammar and framing.
2. CDRI / CRDI acronym flip between the Introduction paragraphs.
3. Clause 4 heading appears as "Terms and definitions" while an alternate frame uses "Symbols and abbreviated terms."
4. Definitions in clause 3 carrying SHALL statements (normative content inside a terms clause).
5. "first notice receipt" bold treatment inconsistency.
6. Case inconsistency across defined terms and field names.
7. The 2.1 note wording.
8. Diagram rendered as an indented block rather than a figure.
9. Apostrophe / typography inconsistency.
10. Remaining minor wording roughness flagged in the review.
