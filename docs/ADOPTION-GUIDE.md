# ADOPTION-GUIDE.md — Adapting the Framework for Your Discipline

Stoa was developed in the context of project management and AI-PMO research, drawing on management methodology, project studies, and the academic-writing-pedagogy literatures. Its core architecture is discipline-agnostic; its surface vocabulary, its citation conventions, its example methodologies, and some of its standards reflect their origin and require adaptation for adopters working outside that lineage. This guide maps the adaptations needed for each major disciplinary cluster.

## Adaptation principle

A framework adoption is *clean* when an adopter changes the surface vocabulary and the example methodologies of the artefacts to fit their discipline while leaving the four-layer architecture, the four-step loop, the audit-gate discipline, and the persona standard intact. Adoption is *risky* when the adopter weakens the architectural commitments — for example, by allowing drafts to bypass the audit gate, by relaxing the persona discipline, or by abandoning the durable artefact spine. Risky adoptions tend to fail at the same failure modes the framework was designed to address.

If an adoption requires substantive architectural change, fork the framework and document the change in your fork's `DESIGN-RATIONALE.md` rather than weakening the canonical framework's discipline. The licence (CC BY-SA 4.0) explicitly permits forks; the contribution back through pull requests is welcome but not required.

## Adaptation by disciplinary cluster

### Adjacent management and policy disciplines

**Management research broadly (organisation studies, strategic management, organisational behaviour, marketing, operations management).** Adoption is expected to be clean. The framework's citation canon already includes the broad management methodology literature; substitute discipline-specific theory citations (for example, replace stakeholder salience with institutional theory or behavioural strategy where appropriate). The R10 audit-gate persona may need to be rephrased — *Editor-in-Chief of a leading [discipline-specific journal]* in place of *Editor-in-Chief of a world-elite [project management] journal* — but the audit's function is unchanged.

**Public administration, public policy, public management.** Adoption is clean with two adaptations. First, the framework's default outlet language assumes peer-reviewed journals; many policy programmes also produce reports for governmental or non-governmental stakeholders, which require a parallel quality bar but with a different reviewer audience. Add an R-standard tagging client or stakeholder reports as separate-but-equally-binding outputs. Second, public-sector research often involves restricted-access data; the integrity provisions in R8 should be tightened to specifically address handling of restricted data.

**Information systems.** The framework's spec-driven-development inheritance is closest to information systems' methodological tradition, which makes adoption mechanically clean. Substitute Hevner et al. (2004) and Peffers et al. (2007) as the canonical methodology citations (already in the bibliography template); use IS-specific maturity models if relevant. The Academic Vern persona's rejection of the *spike* idiom may be reversed in IS adoption, where *spike* has technical meaning beyond software engineering.

### Social sciences

**Sociology, anthropology, political science, economics.** Adoption requires moderate adaptation. The framework's case-study and comparative-method citations (Yin, 2018; Eisenhardt, 1989; Ragin, 2014; George & Bennett, 2005) translate well; add discipline-specific methodology canons (for sociology: Burawoy on extended case method; for anthropology: Geertz, Marcus and Fischer; for political science: King, Keohane, Verba; for economics: Hamermesh, Heckman). The audit-gate persona should reflect your discipline's editorial culture; some social-science journals have markedly different editorial norms than the management mainstream the default Chamber persona reflects.

**Psychology.** Adoption is clean with one substantive adaptation: the framework's R8 ethics provisions need to be expanded to include IRB and human-subjects standards, which are central to most psychology research. The Bem (2003) citation, already in the bibliography, is psychology-canonical and can be elevated to a more central role in the operating-model playbook.

**Education research.** Adoption is clean. The doctoral-writing pedagogy literature the framework already cites (Belcher, Booth et al., Wallace and Wray, Sword, Single) is itself education-adjacent; an education researcher will recognise much of the framework's foundation as native. Substitute education-research-specific theory citations (Vygotsky, Bourdieu, Bronfenbrenner) for the management theory canon.

### Humanities

**History, literature, philosophy, classics, religious studies.** Adoption requires substantial adaptation because the framework's methodological commitments — design science research, transparent data provenance, comparative-criteria-based analysis — assume an empirical-research mode that humanities scholarship often does not adopt. Adopters in these fields should:

- Replace the methodology section of `REQUIREMENTS.md` R3 with discipline-specific transparency conventions (archival provenance for history; primary-source apparatus for literature; argumentation transparency for philosophy).
- Replace the citation format (R5) with the discipline's preference (typically Chicago for history and humanities; MLA for literature in some traditions; OSCOLA for legal and constitutional history).
- Adapt the audit-gate persona to reflect the discipline's editorial culture, which is often more book-centric than article-centric. Adopters writing toward a book rather than journal articles should rethink the four-step loop's per-output structure to operate at the chapter level rather than the article level.
- Retain the persona discipline (R7) and the integrity provisions (R8) without modification; these translate cleanly across all scholarly traditions.

The framework has not been validated in humanities adoption; documentation of adaptations made by humanities adopters through the contribution process (`CONTRIBUTING.md`) is particularly welcome.

### Formal sciences

**Mathematics, theoretical computer science, formal philosophy.** Adoption requires substantial adaptation because the framework's per-output structure assumes a paper-of-evidence-and-argument format that does not map cleanly onto a paper-of-proof-and-theorem format. Adopters in these fields should:

- Reconsider whether the four-step loop maps onto theorem-proving work or whether a different loop (conjecture → proof attempt → review → publication) is more appropriate.
- Replace `{n}-RESEARCH.md` with a `{n}-LITERATURE.md` and add a `{n}-PROOF-SKETCH.md` artefact for the formal content.
- Replace the methodology section of R3 with the discipline's expected proof-presentation conventions.
- Retain the audit-gate discipline (R10) but adapt the Chamber persona to a *referee at a leading mathematics journal* or equivalent.

Adoption in this cluster has not been validated; adopters should expect to fork and adapt substantially.

### Life sciences and physical sciences

**Biology, medicine, chemistry, physics, engineering, environmental sciences.** Adoption requires substantial adaptation primarily because of the experimental-evidence and reproducibility expectations that go beyond the framework's defaults. Adopters in these fields should:

- Expand `REQUIREMENTS.md` R3 to include preregistration, data deposition, statistical reporting standards (CONSORT, PRISMA, ARRIVE, or discipline-specific equivalents), and code/data availability statements that conform to the target outlet's policies.
- Expand R8 to include IRB, IACUC, biosafety, or other relevant ethics-committee provisions.
- Adopt the discipline's standard citation convention in R5 (typically Vancouver or Council of Science Editors style for medicine and biology).
- Adapt the audit-gate persona to reflect the discipline's editorial culture, which often involves multi-reviewer consensus rather than single-editor judgement.

The framework has not been validated in these clusters; adoption is feasible but requires the adopter to do the heavy lifting of adapting R3, R5, R8, and R10. Adopters who succeed are warmly invited to share their adaptations through the contribution process.

## Adaptation triggers — signals that the framework is or is not the right fit

The framework is *probably the right fit* if:

- The programme spans at least eighteen months and at least three intended publications.
- The programme uses AI assistance routinely as a research and drafting aid.
- The programme's outputs target peer-reviewed venues at the top quartile of their disciplinary categories.
- The principal investigator is willing to invest one to five evenings of onboarding cost in exchange for sustained discipline over the programme's duration.

The framework is *probably not the right fit* if:

- The programme is a single thesis with no intended journal publications.
- The programme operates entirely without AI assistance.
- The programme is genuinely short — under six months — such that the artefact-spine overhead is not amortised over enough work.
- The programme's discipline is in a cluster the framework has not yet been validated against (humanities, formal sciences, life sciences, physical sciences) and the principal investigator is not willing to do the adaptation work.

## Reporting adaptation experiences

Adopters who adapt the framework for their discipline are warmly invited to share their experience through the repository's issue tracker or, for substantive adaptations, through a pull request against this guide. Adaptations from disciplines the framework has not yet been validated against are particularly valuable; the framework's intended evolution is toward broader cross-disciplinary applicability, and adopter experience is the primary input to that evolution.
