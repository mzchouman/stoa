# PROVENANCE.md — Intellectual Lineage and Attribution

This document declares the intellectual lineage of *Stoa* and the attribution standards under which the framework was authored and is released. It exists because the framework's first standard for the work it produces is *every claim cites* (`templates/REQUIREMENTS.template.md`, R2 and R4); that standard applies to the framework's own design as much as to the artefacts it helps produce. A doctoral-grade tool that releases its own artefacts without an honest provenance statement would fail its own standard.

## Authorship

Stoa is the original work of **Mohamad-Zouheir Chouman**. The framework is released under sole authorship. Affiliations at the time of initial public release: doctoral candidate (DBA, Strategy, Project Leadership, and PMO Management), SBS Swiss Business School; bachelor's-degree candidate, ISTEC Business School; EMBA, Arden University.

All design choices, all artefact structures, all documentation, and all integrations were authored by the named author. Where the framework draws on external traditions or borrowed substantive content, that lineage is declared in the sections below.

## Intellectual lineage

Stoa sits at the intersection of three established traditions, each of which contributes structurally to the framework's design without being its singular source.

**The spec-driven development tradition in software engineering.** The framework's artefact-spine discipline, its phase-gated execution model, and the convention that durable specifications precede substantive work are inherited from the broader spec-driven development tradition in software engineering. This tradition long predates any particular tool that instantiates it; it is recognisable across decades of practice in the systems engineering and methodology literatures, the agile and lean development communities, and the operational discipline of high-stakes software programmes. Stoa translates the tradition's three load-bearing commitments — *durability of specifications across sessions*, *gate-enforced quality between phases*, and *artefact-based memory that survives team or context changes* — into the academic publishing context, where the artefacts are manuscripts, the gates are editorial reviews, and the standards are doctoral and journal expectations rather than software acceptance criteria. Stoa does not borrow any single instantiation of spec-driven development; it inherits the tradition's design commitments and re-instantiates them for academic work.

**The academic writing pedagogy literature.** The framework's per-paper loop, its distinction between *parallel-safe* and *serial-only* drafting work, its convergence-pass discipline, and the onboarding architecture that introduces the framework to first-time adopters are all influenced by the doctoral-writing pedagogy literature, particularly the works that articulate how successful long-running scholarly writing differs from the failure modes that characterise abandoned or under-finished doctoral work. Specific influences are cited in `templates/BIBLIOGRAPHY.template.md` under *Doctoral writing pedagogy and the craft of scholarly prose*. Where the framework's design recapitulates or operationalises a published claim from this literature, the citation appears in the relevant artefact at the load-bearing point.

**The methodological transparency and peer review literatures in management research.** The framework's binding standards (`templates/REQUIREMENTS.template.md`), its design rationale (`templates/DESIGN-RATIONALE.template.md`), and its audit-gate discipline draw on the methodological transparency literature in management research and on the empirical studies of editorial peer review. The audit gate's structural design — a separate persona simulating editorial judgement, operating verdicts that are binary at the procedural level while preserving narrative richness at the assessment level — is a deliberate adaptation of the editorial-review literature's empirical findings into upstream-of-submission practice. Specific influences are cited in `templates/BIBLIOGRAPHY.template.md` under *Methodological transparency and replicability* and *Peer review, editorial judgement, and the gate function*.

## Borrowed substantive content

Stoa includes one piece of borrowed substantive content that requires explicit declaration.

**The Academic Vern persona.** The persona that supplies the framework's sentence-level evidentiary discipline was uploaded to the author's working environment as a single SKILL.md file. The persona's stance — evidence-first, comparative-analysis-default, limitation-acknowledging, *further-research-is-needed* as legitimate conclusion — was authored by an external party whose identity was not recorded with the upload. The framework's edition of the persona (`templates/SKILL.template.md`) departs from the original in three substantive ways: the original's closing instruction to end every response with humour was permanently removed because it conflicts with the framework's consultancy register; software-engineering examples and idioms in the original were replaced with academic-publishing equivalents; and the persona's stance was anchored explicitly in the philosophy-of-science and academic-writing-pedagogy literatures rather than left ungrounded.

The unmodified original persona is preserved as a separate file alongside the framework's edition for tooling-provenance traceability. Adopters who fork the framework inherit both the original (unchanged) and the framework's edition. If the original author of the Academic Vern persona becomes identifiable, this document will be amended to credit them by name; in the interim, the framework acknowledges that the persona's substantive stance was authored externally.

## Stacked tools the framework composes with

Stoa is designed to compose cleanly with two categories of external tooling without inheriting from them.

**AI assistants with file-access capabilities.** The framework presupposes that the adopter has access to an AI assistant capable of reading and writing files in the adopter's working directory and of maintaining persistent memory across chat sessions. The framework was developed and validated in Claude desktop's Cowork mode (Anthropic, 2026). Adoption with other capable assistants is expected to be clean but is not yet validated; assistant-specific install paths are documented in `docs/INSTALLATION.md`.

**Discipline-specific drafting bundles.** Many doctoral candidates use discipline-specific writing-and-research skill bundles that supply paper-level drafting mechanics (manuscript structure, methods boilerplate, results presentation). The framework stacks above any such bundle without inheriting from it; the cross-walk between the framework's protocol vocabulary and the bundle's drafting-skill names is the formal stacking specification, documented in `docs/INSTALLATION.md` for each supported bundle.

## What the framework does not borrow

To establish the framework's authorship boundaries clearly: the framework does not borrow any specific implementation of spec-driven development; it does not include or recommend any specific software-tool's runtime, command syntax, subagent inventory, or proprietary runtime artefacts; it does not transcribe or paraphrase any specific tool's documentation. The framework's protocol vocabulary — *discuss-phase*, *plan-phase*, *execute-phase*, *audit-milestone* — uses generic English verbs for the steps of a generic four-step loop and is not intended to designate any particular upstream tool.

## Citation expectations for adopters

Adopters who use Stoa in their research programmes and who wish to cite it should follow the citation form recommended in `README.md` and in `CHANGELOG.md`. Adopters who fork the framework and develop substantive variants are required by the licence (`LICENSE`, CC BY-SA 4.0) to credit the original author, link to the original repository, indicate that changes were made, and license the variant under the same terms.

The framework's accompanying methodological paper (in preparation; targeting a Q1-tier methodological venue) will, when published, supply a peer-reviewed citation form that supersedes the working citation form in `README.md`. Adopters will be notified through `CHANGELOG.md`.

## Verification commitment

Citations referenced in the framework's templates and design-defence documents are flagged for verification before any external publication of derivative work. Adopters who plan to cite the framework's bibliography in their own peer-reviewed scholarship should verify each citation against canonical sources before submitting to a journal. The framework's verification commitment is documented in `templates/BIBLIOGRAPHY.template.md`.

---

*This document is part of the framework's load-bearing apparatus and is updated whenever the framework's intellectual lineage changes. Pull requests proposing additions to the lineage statement are welcome, particularly identification of the original Academic Vern persona's author or of substantive prior work the framework should acknowledge.*
