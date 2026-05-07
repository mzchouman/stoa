# OPERATING-MODEL.md — The Loop and Its Adaptations (Template)

> **Adopter notes.** This template specifies Stoa's loop and the six adaptations under which the framework's spec-driven artefact-spine discipline is translated for academic publishing. Replace each `[BRACKETED PLACEHOLDER]` with content specific to your programme. Italicised paragraphs are guidance and should be deleted from the final populated file. The framework's name and orientation are introduced in `PROJECT.md`; the binding standards are in `REQUIREMENTS.md`; the design defence is in `DESIGN-RATIONALE.md`; the reference base is in `BIBLIOGRAPHY.md`. This document presupposes those four artefacts and proceeds to the loop's operational specification.

**Last revised:** [YYYY-MM-DD].

This is the playbook every chat in this project opens with. It maps Stoa loop onto the academic publishing pipeline that produces this programme's [NUMBER] outputs.

The framework's value is not its software-engineering inheritance but its core loop and its insistence on durable artefacts that survive across chats. Stripped to its essence, the framework says: before you do, you discuss; before you discuss substantively, you have a roadmap; before you ship, you audit; and the loop is recorded in files that future you, or future versions of your AI assistant, can pick up cold and trust. That discipline, ported into academic publishing, is what Stoa adds to the doctoral candidate's existing methodological toolkit.

## Why this loop and not another

The four-step loop deserves explicit defence against the named alternatives in the doctoral writing pedagogy literature. Belcher's (2019) twelve-week journal-article workflow is the most widely-adopted comparable in doctoral-writing practice. Stoa loop is *compatible* with Belcher's twelve-week schedule but operates at a different level of abstraction: Belcher prescribes the temporal schedule of a single paper; Stoa prescribes the *artefact-and-gate structure* under which any temporal schedule can run. Bem's (2003) hourglass model is similarly orthogonal: Bem prescribes the *internal architecture of the manuscript*; Stoa prescribes the *operating environment in which manuscripts are produced*. Single (2009) prescribes a streamlined dissertation-writing process that begins with topic selection; Stoa presupposes topic selection and operates from research-programme architecture forward. Booth, Colomb, Williams, Bizup, and Fitzgerald (2016) supply the craft-of-research foundations on which the *discuss* step rests. Stoa does not displace these established methodologies; it composes with them and supplies a layer they do not.

## The four layers, translated for academic publishing

**The project root** is this chat — Pipeline Control. Its persistent artefacts are `PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`, `STATE.md`, `DESIGN-RATIONALE.md`, `BIBLIOGRAPHY.md`, and this playbook. These files are the durable memory of the programme. Any chat that re-opens cold reads them first.

**Each phase** is one output, drafted in its own dedicated chat. The chat opens by declaring its role with a CHAT OPENER, then runs Stoa loop locally: a `{n}-CONTEXT.md` (the decisions that lock before drafting begins), a `{n}-RESEARCH.md` (the literature review and evidence synthesis), a `{n}-PLAN.md` (the atomic drafting tasks ordered into safe-parallelism waves), and the drafting itself executed in those waves. Each artefact is written to the project root; nothing of value lives only in chat memory. This is the framework's response to the context-rot failure mode documented in the recent LLM-augmented-writing literature (Lund et al., 2023; van Dis et al., 2023).

**Each draft milestone** triggers an audit. The Paper Evaluation Chamber — a dedicated chat in which the persona is [DESCRIBE YOUR DISCIPLINE-APPROPRIATE EDITORIAL PERSONA] — performs the framework's `audit-milestone` step. Its verdict is binary in operational terms (per `REQUIREMENTS.md` R10): *Publish-immediately* opens the next gate; anything else returns the paper to its per-paper chat for revision and re-audit. The Chamber's design draws on the empirical literature on editorial peer review (Lamont, 2009; Hirschauer, 2010; Bornmann, 2011); the design defence is in `DESIGN-RATIONALE.md`.

**Each phase closes** when every output in the phase has cleared the Chamber and reached its targeted submission status. Pipeline Control then performs a programme-level coherence check against the prior phases (per `REQUIREMENTS.md` R12) before opening the next phase. This is the `extract-learnings` step: terminology, constructs, and theoretical scaffolds are reconciled across the programme so that any capstone or convergence output remains buildable. The cross-paper-coherence imperative is grounded in the cumulative-knowledge literature (Bettis et al., 2016).

## The loop in one paragraph

For any output in any phase: the per-paper chat opens, declares its role, reads `PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`, `STATE.md`, `DESIGN-RATIONALE.md`, and this playbook in that order; then either creates `{n}-CONTEXT.md` from scratch or picks up an existing skeleton seeded by Pipeline Control; then runs `discuss-phase` with the author until the gray areas are closed and CONTEXT is signed; then runs `plan-phase`, producing `{n}-RESEARCH.md` and `{n}-PLAN.md`; then runs `execute-phase` in the safe-parallelism mode described below; then routes the complete draft to the Paper Evaluation Chamber, which runs `audit-milestone`; and only on a *Publish-immediately* verdict does the output exit the framework for submission. After exit, the per-paper chat updates `STATE.md` with the in-review status and goes idle until the editor responds.

## Three layers stack throughout — they do not compete

Stoa governs the workflow at programme level. The discipline-specific drafting bundle (if installed) governs paper-level drafting mechanics. The Academic Vern persona — substance adopted; closing humour permanently disabled — governs the evidentiary standard at the sentence level. The three altitudes are mutually compatible because each operates on a different unit of work: programme, paper, paragraph.

## What Pipeline Control owns and what it does not own

Pipeline Control owns the four root artefacts plus the three derivative artefacts (`DESIGN-RATIONALE.md`, `BIBLIOGRAPHY.md`, the bootstrap prompt for any further propagation), the cross-paper coherence pass, the journal and award strategy, the phase-gate decisions, and any standing instruction that should propagate across all chats. It does not draft papers. It does not run the Chamber's audits. It does not duplicate or override decisions taken inside per-paper chats; if a per-paper chat's decision conflicts with a programme-level standard, Pipeline Control issues a clarifying note and, where necessary, edits the binding standard in `REQUIREMENTS.md` rather than overriding the chat. The principle is clean separation of altitude: this chat sees the programme; the per-paper chats see the paper; the Chamber sees the manuscript.

---

## Adaptation 1 — Safe-parallelism rule for `execute-phase`

The default spec-driven `execute-phase` runs atomic tasks in parallel waves with fresh context per wave. That works for independent code files; it fragments coherence in a single manuscript. The academic safe-parallelism rule is:

- **Parallel-safe** drafting: literature review sections, methods boilerplate, descriptive case sections, reference list assembly, figure and table captioning. These can be drafted in parallel waves with fresh context because they are loosely coupled to argumentative voice. The looseness is grounded in Bem's (2003) hourglass model: the wide top and wide bottom of the hourglass are structurally separable from the narrow middle.
- **Serial-only** drafting: introduction, theoretical framework, discussion, contribution-and-boundary-conditions paragraph, abstract. These must be drafted serially after the body has settled because each depends on the developed argument. The seriality is grounded in the *making your argument* tradition (Booth et al., 2016).
- **Convergence pass:** every paper closes with a single-context, end-to-end read by the same chat that drafted it, before the manuscript is routed to the Paper Evaluation Chamber. This pass is non-negotiable and is grounded in the register-drift findings of Wallace and Wray (2021).

## Adaptation 2 — Cross-walk to your discipline-specific drafting bundle

*If your project has a discipline-specific drafting skill bundle installed, document the cross-walk here. State which protocol-name from the framework's loop maps to which skill in your bundle. State which framework concepts have no counterpart in your bundle and are therefore retained as concept handles to be executed inline by the per-paper chat or by Pipeline Control. State which features of your bundle are out of scope for framework adoption.*

[POPULATED CROSS-WALK]

## Adaptation 3 — Assumptions-vs-questions choice rule for `discuss-phase`

The framework offers two `discuss-phase` modes: question-driven (default) and *assumptions* mode (reads existing artefacts, surfaces inferred assumptions, asks the author to correct only the wrong ones). The choice rule for this project is:

- **Use assumptions mode** when one or more substantive drafts already exist in the workspace.
- **Use question-driven mode** when no draft yet exists.
- **Hybrid mode** is admissible when prior outputs seed assumptions for downstream outputs but the new output's specific contribution still needs question-driven elicitation.

The choice rule is grounded in the methodological practice of progressive elaboration in case-based research (Eisenhardt, 1989; Yin, 2018).

## Adaptation 4 — `map-literature` (future-work item)

The framework's spec-driven heritage includes a `map-codebase` operation that indexes source files. The academic analogue — `map-literature` — would index the body of works cited across the programme's outputs, surface cross-paper terminology drift, flag candidate definitions and constructs that recur, and produce the coherence pass mandated by `REQUIREMENTS.md` R12 in an automated rather than manual form. Implementation deferred for this programme; flagged here so it is not forgotten. Until implemented, the cross-paper coherence pass is a manual exercise. The conceptual debt is to the cumulative-knowledge concerns of Bettis et al. (2016).

## Adaptation 5 — Out-of-scope features

The framework's spec-driven inheritance includes features that are not adopted in academic publishing because they are software-delivery features. *Adopter, list any features your programme deliberately does not adopt. The standard list — out of scope unless your programme is itself software-related — includes: multi-runtime installer logic; hook compilation; schema-drift detection for ORM migrations; build-and-test gates; canary release workflows; token-budget tooling; runtime-specific review-model selection; minimal-install profiles. Add or remove items as fits your programme.*

[POPULATED OUT-OF-SCOPE LIST]

## Adaptation 6 — Protocol vocabulary

The framework's protocol vocabulary — *discuss-phase*, *plan-phase*, *execute-phase*, *audit-milestone*, *extract-learnings*, *update*, *new-milestone*, *pause-work* — uses generic English verbs for the steps of the loop. They are protocol names used in conversation to signal which step of the loop is being executed; nothing further is required for them to function. Authoring runtime-native bindings that translate these names to file actions is a future-work item, not a prerequisite for using the framework.

---

## Onboarding paragraph for new adopters

*This paragraph is for adopters who fork this template into their own projects and need to brief their own future-selves on first use. Replace this paragraph with content that reflects your own project's first-week experience.*

A new adopter installing Stoa in their project should expect the following first-week experience. The framework is installed by following the bootstrap prompt, which produces the four root artefacts (`PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`, `STATE.md`), this playbook, the bibliography, and the design rationale, all populated with the adopter's actual research-programme content rather than boilerplate. The Academic Vern skill is installed alongside the existing skills directory. The first per-paper chat is opened with a CHAT OPENER declaring its role and runs `discuss-phase` against the seeded `{n}-CONTEXT.md` skeleton. The loop runs as documented above. The first paper does not exit the framework until the Paper Evaluation Chamber returns *Publish-immediately*. Existing supervisor relationships, IRB processes, and journal selection processes are unchanged; the framework sits beside those relationships, not over them.

The onboarding cost is the time required to read this document, `REQUIREMENTS.md`, `DESIGN-RATIONALE.md`, and `PROJECT.md` once; to populate the four root artefacts with actual programme content; and to absorb the loop's vocabulary. Empirically, this is one to two evenings for an adopter with prior exposure to spec-driven development or to academic methodology, and three to five evenings for an adopter without that exposure.

---

*References cited in this template are listed in `BIBLIOGRAPHY.md`. The framework's design defence is in `DESIGN-RATIONALE.md`. The binding standards are in `REQUIREMENTS.md`. The framework's name and orientation are introduced in `PROJECT.md`.*
