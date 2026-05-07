# Stoa

**An operating model for multi-paper scholarly research programmes.**

Authored by Mohamad-Zouheir Chouman.
Released under [Creative Commons BY-SA 4.0](LICENSE).

---

## What this is

Stoa is a layered configuration of durable file artefacts, workflow protocols, persona-discipline standards, and a non-overridable audit gate, designed to produce outputs of doctoral and Q1-tier-publishable quality across long-running research programmes that span months to years. It is not a software application. It is not a writing tutor. It is not a journal selector or a citation manager. It is the operating environment within which a researcher organises a multi-paper research programme so the cumulative effect of dozens of writing sessions across several years yields outputs that meet the bar of top-tier peer review and best-paper award competition.

The framework draws on the broader spec-driven development tradition in software engineering — durable specifications, phase-gated execution, artefact-based memory — and translates that discipline into the academic publishing context, where the artefacts are manuscripts, the gates are editorial reviews, and the standards are doctoral and journal expectations rather than software acceptance criteria.

## Why it exists

Doctoral candidates working on multi-paper programmes — and increasingly on dissertation-by-publication programmes that commingle peer-review milestones with thesis defence — confront a recurring set of failure modes that the literature on doctoral writing pedagogy has named in adjacent terms but has not yet operationalised in tooling. The productivity collapse that follows extended periods without a working artefact in front of the candidate; the recurrent re-litigation of decisions, where the same question is re-decided across sessions because no durable record retains the prior answer; the register drift that accumulates across long-running projects, where successive sections of a programme acquire incompatible voices; the loss of stylistic discipline as projects extend beyond a single sustained writing season. None of these has, at the time of this release, a published technological-rule response.

A further set of difficulties arises when AI-augmented research enters the picture. The recent literature on large language models in scholarship identifies a class of failures specific to LLM-assisted writing: *context-rot*, the degradation of LLM output quality across extended conversations as the model's working context fills with accumulated prior turns; *register collapse*, the gradual drift of LLM output toward generic prose absent explicit voice anchoring; and *evidence inflation*, the tendency of unconstrained LLMs to assert without citing or to cite without verifying.

Stoa targets the intersection of these two literatures: the enduring failure modes of long doctoral programmes, exacerbated by the new failure modes of AI-augmented authorship.

## Who this is for

Researchers working on multi-paper research programmes who want their cumulative output to meet the bar of top-tier peer review and best-paper award competition. The framework was developed in a doctoral context with AI assistance as the original case, but its discipline applies broadly: doctoral candidates and post-doctoral fellows; academic faculty assembling cohesive research portfolios; independent scholars producing structured intellectual outputs; consulting researchers building rigorous bodies of work for institutional clients.

It will be most useful to programmes that span at least eighteen months, that involve at least three intended publications, and that target peer-reviewed venues at the top quartile of their disciplinary subject categories. It will be less useful for single-output projects with no companion publications or for programmes so short that the artefact-spine overhead is not amortised.

The framework is discipline-agnostic in its core architecture but was developed in the context of project management and AI-PMO research; adoption in adjacent management and policy disciplines is expected to be clean, while adoption in distant disciplines (humanities, formal sciences, life sciences) will require non-trivial adaptation. Boundary conditions and adaptation guidance live in [docs/ADOPTION-GUIDE.md](docs/ADOPTION-GUIDE.md).

## How it works

Stoa has four layers, each operating at a different altitude.

**At the programme altitude**, a small set of durable file artefacts at the project root encodes the programme's persistent state. These files are the framework's response to context-rot and to the recurrent re-litigation pattern. They are read first by any new chat session, including by a chat opened cold after a multi-month interval. The five files are:

- [PROJECT.md](templates/PROJECT.template.md) — the programme charter
- [REQUIREMENTS.md](templates/REQUIREMENTS.template.md) — the binding standards
- [ROADMAP.md](templates/ROADMAP.template.md) — the phased schedule
- [STATE.md](templates/STATE.template.md) — the live status board
- [OPERATING-MODEL.md](templates/OPERATING-MODEL.template.md) — the playbook

A `BIBLIOGRAPHY.md` and a `DESIGN-RATIONALE.md` accompany the spine for citation discipline and design defence.

**At the paper altitude**, each paper in the programme is treated as a phase. Each phase runs the four-step loop: *discuss-phase* surfaces and locks decisions in `{n}-CONTEXT.md` before drafting begins; *plan-phase* produces `{n}-RESEARCH.md` and `{n}-PLAN.md`; *execute-phase* produces the draft itself in safe-parallelism mode (parallel where coherence permits, serial where the argument requires); *audit-milestone* routes the manuscript to the Paper Evaluation Chamber. Per-paper context files preserve decisions across chats so the candidate can resume work after intervals of weeks or months without re-deriving the prior state.

**At the sentence altitude**, an evidence-first persona — *Academic Vern* in this distribution, installable via the included [SKILL.md template](templates/SKILL.template.md) — enforces the citation, comparative-analysis, and limitation-acknowledgement standards that the methodological transparency literature in management research demands. Every claim cites; every approach is positioned comparatively; limitations and uncertainty are acknowledged explicitly; *further research is needed* is treated as a legitimate conclusion. The persona's stance is anchored in Popperian falsificationism, Lakatosian research programmes, and Toulmin's argumentative structure.

**At the audit altitude**, the Paper Evaluation Chamber — a separate chat in which an evaluator persona simulates the editorial judgement of an Editor-in-Chief at a top-quartile journal — performs the framework's binding audit before any external submission. The Chamber's verdict is operationally binary: *Publish-immediately* opens the next gate; anything else returns the paper to its per-paper chat for revision and re-audit. The Chamber is non-overridable inside the framework, on the principle that a quality gate that can be skipped under deadline pressure is a quality gate that will be skipped, and is therefore not a quality gate.

## Installation

Stoa is distributed as a set of artefact templates and a bootstrap prompt. Two installation paths are supported.

**Path A — bootstrap prompt (recommended for first-time adopters).** Open the [BOOTSTRAP.md](BOOTSTRAP.md) file, copy the prompt block in full, and paste it as the very first message of a new chat in your AI assistant of choice (the framework has been validated in Claude desktop's Cowork mode; other assistants with comparable file-access capabilities are expected to work but are not yet validated). The receiving assistant will ask six clarifying questions about your research programme, then generate the full set of root artefacts populated with your actual content.

**Path B — manual installation.** Copy the contents of `templates/` into the root of your research-programme working directory. Edit each template by replacing placeholders with your actual programme content. Install the persona skill by copying `templates/SKILL.template.md` to your AI assistant's skills directory (path varies by assistant). Read [docs/INSTALLATION.md](docs/INSTALLATION.md) for assistant-specific instructions.

After installation, regardless of path, your project root will contain the four root artefacts, the playbook, the bibliography skeleton, and the design-rationale skeleton. The first per-paper chat is opened with a CHAT OPENER declaring its role and runs *discuss-phase* against the seeded `{n}-CONTEXT.md` skeleton.

The onboarding cost is roughly one to two evenings for a candidate with prior exposure to spec-driven development or to academic methodology, and three to five evenings for a candidate without that exposure. The pay-off accrues over the following months as the artefact spine produces durable decision-records that survive cross-session intervals and as the audit gate raises the floor of what is submitted to external review.

## What is included in this release

```
operating-model/
├── README.md                                  This file.
├── LICENSE                                    Creative Commons BY-SA 4.0 (pending confirmation).
├── BOOTSTRAP.md                               The paste-ready bootstrap prompt for first-time adopters.
├── PROVENANCE.md                              Provenance discipline and inherited tradition.
├── CHANGELOG.md                               Versioned record of releases.
├── CONTRIBUTING.md                            How to contribute to the framework.
├── CODE_OF_CONDUCT.md                         Standards for community participation.
├── templates/
│   ├── PROJECT.template.md                    Programme charter template.
│   ├── REQUIREMENTS.template.md               Binding-standards template (R1–R13).
│   ├── ROADMAP.template.md                    Phased-schedule template.
│   ├── STATE.template.md                      Live status board template.
│   ├── OPERATING-MODEL.template.md            Playbook template.
│   ├── DESIGN-RATIONALE.template.md           Design-defence template.
│   ├── BIBLIOGRAPHY.template.md               Reference-base template.
│   ├── CONTEXT.template.md                    Per-paper CONTEXT skeleton template.
│   └── SKILL.template.md                      Academic Vern persona skill template.
├── docs/
│   ├── INSTALLATION.md                        Assistant-specific install notes.
│   ├── ADOPTION-GUIDE.md                      Adaptation guidance for non-management disciplines.
│   ├── DESIGN-PRINCIPLES.md                   The principles behind the framework's design choices.
│   └── FAQ.md                                 Frequently asked questions.
└── examples/
    └── (worked-example artefacts to be added in a future release)
```

## What this is not

This document and the framework it describes are provided in the spirit of helping doctoral candidates organise long-running, AI-augmented research programmes. They are not a guarantee of acceptance at any journal, of recognition by any award committee, of approval by any thesis committee, or of any other external outcome. The Paper Evaluation Chamber is an editorial-discipline simulator, not a real editor; its calibration against actual editorial outcomes is unknown until a corpus of papers that have passed the gate has accumulated decisions at target journals. The framework's value lies in raising the floor of what is produced, not in guaranteeing what is accepted.

The framework does not replace supervisor relationships, IRB processes, journal editorial decisions, or the candidate's own intellectual labour. It supplements those existing structures with a durable operating environment.

## Honest limitations

The framework was designed and demonstrated on a single research programme as of the time of this initial release. Single-site demonstration has well-known generalisability limitations, named in [docs/DESIGN-PRINCIPLES.md](docs/DESIGN-PRINCIPLES.md). The framework's behavioural compliance — its consistent application of the standards across long sessions — depends on the AI assistant's memory and instruction-following behaviour, which is non-deterministic in current implementations. The durable file artefacts at the project root mitigate this by encoding critical state in files; the residual non-determinism applies to behavioural compliance rather than to factual recall.

The framework was developed in the context of project management and AI-PMO research. Adoption in adjacent management and policy disciplines is expected to be clean; adoption in distant disciplines will require non-trivial adaptation. Adopters in those disciplines are invited to fork, adapt, and either share their adaptations back through pull requests or maintain their own forks.

## Provenance

Stoa is original work by Mohamad-Zouheir Chouman, drawing on the broader spec-driven development tradition in software engineering and on the academic-writing pedagogy and methodological-transparency literatures in management research. Where the framework borrows specific substantive content from named prior work, that work is attributed in [PROVENANCE.md](PROVENANCE.md). Where the framework cites scholarly literature in its design defence, those citations are listed in [templates/BIBLIOGRAPHY.template.md](templates/BIBLIOGRAPHY.template.md).

## License

Stoa is released under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](LICENSE). Adopters are free to use, modify, and redistribute the framework provided they credit the original author and license derivative works under the same terms.

## Citation

If you use Stoa in your research programme and wish to cite it, the recommended citation form is:

> Chouman, M.-Z. (2026). *Stoa: An operating model for multi-paper scholarly research programmes* (Version 0.1.1) [Methodological framework]. https://github.com/mzchouman/stoa

The bracketed descriptor `[Methodological framework]` follows APA 7 §10.10's provision for an author-supplied descriptor where no prescribed descriptor (`[Computer software]`, `[Mobile app]`, `[Data set]`) precisely fits the form of the work. Stoa is a Markdown corpus of templates, workflow protocols, and a persona skill — a methodological framework rather than executable software in a strict sense — and the descriptor reflects that classification, positioning the citation alongside other published methodological frameworks (CONSORT, STROBE, PRISMA, and the Design Science Research framework of Peffers, Tuunanen, Rothenberger, & Chatterjee, 2007).

A more substantive methodological paper describing the framework, its design rationale, and its evaluation evidence is in preparation and will target a Q1-tier methodological venue. When that paper is published, the citation form will update accordingly.

## Contact and feedback

Questions, adaptation reports, and pull requests are welcome through the repository's issue tracker. For substantive collaboration enquiries, contact the author through the affiliations listed in [PROVENANCE.md](PROVENANCE.md).

---

*Document version: 0.1.1. Verification of citations referenced in design-rationale documents is recommended before any external publication of derivative work.*
