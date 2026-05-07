# CHANGELOG

All notable changes to Stoa are documented in this file. The format follows the conventions of *Keep a Changelog* and adheres to semantic versioning where applicable. Versions describe the framework artefacts and documentation, not the consuming project.

## [0.1.1] — 2026-05-07 — Citation-descriptor correction

### Changed

- Recommended-citation bracket descriptor changed from `[Software and documentation]` to `[Methodological framework]`. The change reflects a more accurate APA 7 §10.10 classification of the work: Stoa is a Markdown corpus of templates, workflow protocols, and a persona skill — a methodological framework rather than executable software in the strict sense. The new descriptor is an author-supplied APA 7 descriptor (the standard, prescribed forms `[Computer software]`, `[Mobile app]`, `[Data set]` did not precisely fit the form of the work) and positions the citation alongside other published methodological frameworks (CONSORT, STROBE, PRISMA, the Design Science Research framework of Peffers, Tuunanen, Rothenberger, & Chatterjee, 2007).
- Author surname-first short form `Chouman, M.-Z.` adopted in the recommended-citation block as the canonical APA 7 author-element form (the prior `Chouman, Mohamad-Zouheir.` form, with full given names spelled out, is also valid; the short form is preferred for citation strings and the long form is preserved in the LICENSE attribution clause and in the PROVENANCE document).

### Surfaces touched

- `README.md` recommended-citation block, with an explanatory note on the descriptor selection.
- `README.md` document-version footer.
- `CHANGELOG.md` (this entry).

### Notes for adopters

- No structural change to any template, protocol, or persona skill. Adopters who installed Stoa under v0.1.0 are not required to take any action; the descriptor change is metadata-only.
- A future v0.1.2 will back-propagate the Zenodo DOI (once minted via the GitHub-Zenodo integration) into the recommended-citation block, replacing the GitHub URL with the DOI URL while retaining the canonical-source note.

## [0.1.0] — 2026-05-07 — Initial public release (working draft)

### Added

- The framework's public name, *Stoa*, was selected and adopted across all artefacts.
- Public README at the repository root introducing the framework, its problem domain, the four-layer architecture, installation paths, release contents, honest limitations, provenance, and recommended citation form.
- LICENSE under Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0).
- BOOTSTRAP prompt providing a paste-ready install path for first-time adopters in any AI assistant with file-access capabilities; the prompt is self-contained and embeds the Academic Vern persona skill template directly.
- PROVENANCE document declaring the intellectual lineage of the framework: the broader spec-driven development tradition in software engineering; the academic-writing pedagogy and methodological-transparency literatures in management research; the Academic Vern persona authored separately and tuned for this release.
- CONTRIBUTING and CODE_OF_CONDUCT documents establishing the standards for community participation.
- Nine artefact templates in `templates/`: PROJECT, REQUIREMENTS, ROADMAP, STATE, OPERATING-MODEL, DESIGN-RATIONALE, BIBLIOGRAPHY, CONTEXT, and SKILL.
- Four documentation files in `docs/`: INSTALLATION, ADOPTION-GUIDE, DESIGN-PRINCIPLES, and FAQ.

### Known limitations

- Single-site demonstration evidence at the time of this release; multi-site adoption evidence will accumulate as adopters fork and use the framework.
- Citations referenced in design-defence documents and templates are flagged for verification by an authoritative reference-management process before any external publication of derivative work.
- The framework's behavioural compliance — consistent application of the standards across long sessions — depends on the AI assistant's memory and instruction-following behaviour, which is non-deterministic in current implementations.

### Notes for adopters

- Place this release in a working directory and follow the BOOTSTRAP path for first-time use.
- Read README, BOOTSTRAP, PROVENANCE, and the nine templates in that order before customising.
- Pull-request adaptations and worked examples are welcomed; see CONTRIBUTING for the contribution process.

---

Future releases will record changes in this format, with one section per version, dated, and structured under *Added*, *Changed*, *Deprecated*, *Removed*, *Fixed*, and *Security* subheadings as appropriate.
