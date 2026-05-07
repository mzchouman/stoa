# Contributing to Stoa

Thank you for considering a contribution to Stoa. This document sets out how to propose changes, what kinds of contribution are welcome, and the standards under which contributions are reviewed and merged.

The framework is authored under sole authorship by Mohamad-Zouheir Chouman. Contributions are accepted through pull requests and are reviewed against the same doctoral-grade and Q1-tier-publishable standards that the framework imposes on its own artefacts. The discipline that distinguishes a useful contribution from one that is declined is summarised in the standards listed in `templates/REQUIREMENTS.template.md`. Contributors are encouraged to read those standards before opening a substantive pull request.

## What contributions are welcome

**Worked examples.** The framework's documentation is materially improved by anonymised worked examples of populated artefacts — completed `CONTEXT.md` files, populated `ROADMAP.md` files for non-management disciplines, and populated `REQUIREMENTS.md` adaptations for fields whose conventions differ from the management default. Worked examples should be added to the `examples/` directory with a brief README in each example folder describing the discipline, the programme stage, and any framework adaptations made.

**Adaptation guidance for new disciplines.** The framework was designed in the context of project management and AI-PMO research. Adopters in adjacent and distant disciplines are warmly invited to share their adaptations through pull requests against `docs/ADOPTION-GUIDE.md`, with discipline-specific notes on which standards required adaptation and how the framework's loop maps onto the disciplinary conventions of the new field.

**Documentation improvements.** Clarifications, typo fixes, broken-link repairs, and onboarding-friendliness improvements are welcome. The first concern of the framework's documentation is to be openable and usable by an unknown doctoral candidate encountering the framework cold; contributions that improve that openability are particularly welcome.

**Translations.** The framework is currently in English. Translations of the README, BOOTSTRAP, and the templates into other major languages of doctoral scholarship are welcome and will be merged as separate localisation directories under `translations/`.

**Bibliography additions and corrections.** Citations in the framework's bibliography template are flagged for verification before public reuse; if you identify an error in an existing citation or know of a substantive work the framework should reference, a pull request against `templates/BIBLIOGRAPHY.template.md` is welcome.

## What contributions will not be accepted

**Substantive design changes that compromise the four-layer architecture.** The framework's design is the product of a defended set of choices documented in `docs/DESIGN-PRINCIPLES.md`. Proposals that would dissolve the layer separation, weaken the audit-gate non-overridability, or relax the persona-discipline requirements will not be accepted into the canonical release. Contributors who genuinely need a different architecture are encouraged to fork and maintain their own variant.

**Content that conflicts with the citation discipline.** Contributions that introduce uncited assertions, fabricated citations, or claims unsupported by the supplied evidence will be returned for revision. The framework imposes the same evidentiary standard on its own artefacts as it imposes on the work of its adopters.

**Software-tool-specific dependencies.** The framework is designed to work with any AI assistant that has file-access capabilities. Contributions that hard-code dependencies on a particular assistant's runtime, command syntax, or proprietary features will be re-engineered to remain assistant-agnostic.

**Promotional material for individual researchers, institutions, or services.** The framework is positioned as a piece of methodological infrastructure, not as a marketing channel. Pull requests that primarily advertise external services, tools, or institutions will be declined.

## How to propose a contribution

1. **Open an issue first** for substantive contributions (a new template, a new documentation section, a worked example longer than a single page). The issue should describe the proposed contribution, name the section of the framework it would touch, and reference any relevant scholarship. The maintainer will respond with whether the contribution is in scope before you invest substantial effort.

2. **For minor contributions** (typo fixes, broken-link repairs, single-paragraph clarifications), proceed directly to a pull request without opening an issue first.

3. **Fork, branch, and propose.** Fork the repository, create a branch named for the contribution (e.g., `add-anthropology-adaptation`, `fix-citation-aguinis-2018`), make the changes, and open a pull request against the `main` branch.

4. **Pull request hygiene.** The pull request description should state what the contribution does, why it is needed, and what alternatives were considered. Long pull requests that bundle multiple unrelated changes will be returned for splitting.

## Review process

Pull requests are reviewed by the maintainer against the framework's standards. Review may take days or weeks depending on the maintainer's research-programme load. A pull request may receive one of four outcomes: merged as proposed; merged after requested revisions; declined with explanation; or held pending further discussion. The maintainer commits to giving a substantive response within two weeks of opening for any pull request that has met the hygiene standards above.

## Authorship and credit

Contributors retain authorship of their contributions and are credited in the repository's contributor list. Substantive contributions to the framework's design, documentation, or worked-example library are additionally credited by name in the next published version of `CHANGELOG.md`. The framework's overall authorship attribution remains with the maintainer; contributions to specific artefacts are credited to their authors but do not transfer overall authorship of the framework.

## Code of conduct

All contributions and discussions are governed by `CODE_OF_CONDUCT.md`. Read it before participating.

## Licence

By submitting a contribution, you agree that your contribution is licensed under the same Creative Commons Attribution-ShareAlike 4.0 International licence as the rest of the framework. See `LICENSE`.

## Contact

For questions that are not appropriate for a public issue, contact the maintainer through the affiliations listed in `PROVENANCE.md`. Sensitive issues — for example, conduct concerns or licensing questions — should be raised privately rather than as public issues.

---

*This document follows the conventions of well-maintained open-source academic-tool projects. Adaptations to the contribution process will be reflected here as the framework matures.*
