# DESIGN-RATIONALE.md — Design Defence (Template)

> **Adopter notes.** This template treats Stoa's instantiation in your project as the product of a structured design exercise. It is written to a higher bar than is strictly necessary for adoption — adopters who do not intend to publish a methodological paper about their use of the framework can shorten or simplify it. Adopters who *do* intend to publish methodologically (or who want their use of the framework to withstand the scrutiny of a doctoral committee, an external reviewer, or a future ethics audit) should retain the full structure. Replace each `[BRACKETED PLACEHOLDER]` with content specific to your project. Italicised paragraphs are guidance.

**Document purpose.** This artefact defends the operating model that governs this research programme as the product of a structured design exercise. It is written to the bar that a doctoral committee or a methodological reviewer would expect, and it serves three audiences: the principal investigator (the author), prospective adopters of the framework's adaptation in this project, and reviewers of any methodological paper that may be derived from this work. Every load-bearing claim is anchored to `BIBLIOGRAPHY.md`.

The framework's name and orientation are introduced in `PROJECT.md`; this document presupposes that introduction and proceeds to the design defence.

## 1. Problem identification

*Adopter, write one to two paragraphs that name the failure modes the framework addresses in your specific project. The general failure modes — productivity collapse, recurrent re-litigation, register drift, context-rot, register collapse, evidence inflation — are documented in the framework's own provenance and are the reason the framework exists. Your job in this section is to particularise: which of those failure modes are most acute in your specific project's context, and what additional project-specific failure modes (if any) the framework is being asked to address.*

[POPULATED PROBLEM STATEMENT]

## 2. Design objectives

*The framework's six default design objectives are listed below. Adapt the wording to your project's domain; do not weaken any objective without explicit reasoning.*

**Objective 1 — Durability of context across sessions.** The configuration must produce decision-records that survive arbitrary chat-session boundaries, model updates, and time gaps of months or years.

**Objective 2 — Phase-gate enforcement of quality.** The configuration must prevent unaudited work from being submitted for external peer review. The audit mechanism must be non-overridable inside the system.

**Objective 3 — Cross-output coherence.** The configuration must enforce that constructs, definitions, datasets, and theoretical scaffolds remain consistent across the programme's outputs.

**Objective 4 — Methodological transparency at the deliverable level.** Every output produced under the configuration must satisfy the transparency requirements of the relevant disciplinary literature.

**Objective 5 — Integrity at the programme level.** The configuration must encode and enforce the ethical standards governing AI-augmented scholarly authorship.

**Objective 6 — Onboarding-friendliness for new adopters.** The configuration must be openable and usable by a new adopter encountering it cold. *(This is non-negotiable for any project-internal configuration that will be shared, forked, or referenced by collaborators or successors.)*

## 3. Design and development — the artefact

*Adopter, describe the configuration you have actually instantiated. The general structure is given below. Replace placeholders with your project's specifics — for example, which discipline-specific drafting bundle you use, which audit-gate persona you have configured, which protocol-vocabulary extensions you have added.*

The configuration is a layered artefact comprising four components, each operating at a different altitude.

**The first component is the durable artefact spine.** Five files at the project root — `PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`, `STATE.md`, and `OPERATING-MODEL.md` — encode the programme's persistent state. They are read first by any new chat session.

**The second component is the four-step loop applied per output.** Each output in the programme is a phase. Each phase runs *discuss-phase*, *plan-phase*, *execute-phase*, *audit-milestone*. The loop is compatible with established doctoral-writing methodologies (Belcher, 2019; Bem, 2003; Booth et al., 2016; Single, 2009) and operates at a different level of abstraction.

**The third component is the persona-discipline layer.** The Academic Vern persona, installed at the project's skills directory, encodes the sentence-level evidentiary standards. The persona's stance is grounded in the falsificationist tradition (Popper, 2002), in Lakatos's (1970) account of research programmes as the unit of progress, and in Toulmin's (2003) argumentative structure.

**The fourth component is the audit gate.** The Paper Evaluation Chamber is a dedicated chat in which an evaluator persona simulates editorial judgement. Its design is informed by the empirical literature on editorial peer review (Lamont, 2009; Hirschauer, 2010; Bornmann, 2011).

A candid note on the audit-gate component's limitation: the Chamber is an editorial-discipline simulator, not a real editor. Its value lies in raising the floor of what leaves the project, not in predicting what an actual journal editor will accept.

## 4. Demonstration — application to this programme

*State briefly how the framework was instantiated in your specific programme, what evaluation evidence you have at the time of writing, and what the next demonstration milestones are.*

[POPULATED DEMONSTRATION SECTION]

## 5. Evaluation — preliminary report against design objectives

*State, for each of the six objectives in section 2, the evaluation evidence you have at this point and what evidence you expect to acquire as the programme proceeds. Honest "not yet tested" responses are admissible; mistating evidence is not.*

*Objective 1 — Durability of context.* [STATUS, EVIDENCE]

*Objective 2 — Phase-gate enforcement.* [STATUS, EVIDENCE]

*Objective 3 — Cross-output coherence.* [STATUS, EVIDENCE]

*Objective 4 — Methodological transparency.* [STATUS, EVIDENCE]

*Objective 5 — Integrity.* [STATUS, EVIDENCE]

*Objective 6 — Onboarding-friendliness for new adopters.* [STATUS, EVIDENCE]

## 6. Comparison with alternative configurations

*A defensible design must show why it was not done differently. State the alternatives you considered and rejected, with reasons.*

**Alternative 1 — A pure [NAMED METHODOLOGY] regime, with no cross-paper artefact spine.** Rejected because [REASON].

**Alternative 2 — [DESCRIBE].** Rejected because [REASON].

**Alternative 3 — [DESCRIBE].** Rejected because [REASON].

A fourth alternative — *no operating model at all* — is acknowledged as the dominant practice in doctoral programmes and is the implicit baseline against which the framework's adoption value is measured.

## 7. Provenance and credit

*Restate, in your own project's terms, the framework's intellectual lineage. The full provenance discipline is in the public-release `PROVENANCE.md`.*

Stoa in this project draws on the broader spec-driven development tradition in software engineering and on the academic-writing-pedagogy and methodological-transparency literatures in management research. It composes with [LIST DISCIPLINE-SPECIFIC DRAFTING BUNDLES YOUR PROJECT USES]. The Academic Vern persona's substantive stance was authored externally and is preserved alongside the framework's tuning of it for traceability.

This project is authored under sole authorship by [AUTHOR NAME].

## 8. Threats to validity

*A design science artefact is incomplete without an explicit account of the threats to its validity. The general threats below apply to any single-site adoption; add project-specific threats as relevant.*

**Single-site demonstration.** The configuration has been instantiated on this programme alone, so far. Single-site demonstration has well-known generalisability limitations.

**Author-as-evaluator confound.** The principal investigator who instantiated the configuration is also the principal investigator who evaluates whether it works. The audit gate mitigates the confound by introducing a structurally distinct evaluator persona, but the persona is run by the same underlying assistant; the structural distinction is procedural rather than independent.

**Editorial-simulator limitation.** The audit gate is an editorial-discipline simulator, not a real editor. Its calibration against actual editorial outcomes is unknown until the programme accumulates editor decisions at target outlets.

**Memory-propagation probabilism.** The framework's standing instructions are saved to the assistant's long-term memory. Adherence across many future chats depends on memory-recall behaviour, which is non-deterministic in current implementations. The durable artefacts at the project root mitigate this.

**Cultural and disciplinary boundedness.** The framework was developed in the context of project management and AI-PMO research. Adoption in distant disciplines may require non-trivial adaptation.

[ADD PROJECT-SPECIFIC VALIDITY THREATS]

## 9. Closing remark

This document is a design defence, not a marketing claim. It establishes *that* the configuration is engineered to a doctoral bar, *why* its components are configured as they are, *what* alternatives were considered, and *which* limitations attach to the present state. It does not establish that the configuration outperforms what other doctoral candidates use; that claim awaits independent demonstration evidence.

A reader who arrives at this document looking for a guarantee will not find one. A reader who arrives looking for a defensible scaffold under which to organise their own multi-paper research programme will find a configuration whose design is explicit, whose limitations are named, and whose evolution is open to amendment as evidence accumulates.

---

*References cited in this document are listed in `BIBLIOGRAPHY.md`. Citations are formatted to the convention specified in `REQUIREMENTS.md` R5.*
