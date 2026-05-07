# FAQ.md — Frequently Asked Questions

This document answers the questions adopters most often ask before, during, and after first install. Questions are grouped into four sections: *Before installing*, *During the first paper*, *During the long run*, and *Forking, contributing, and citing*. Where an answer points to a fuller treatment elsewhere, the reference is included.

## Before installing

**Is Stoa right for my programme?**

Read the *Who this is for* section of `README.md` and the *Adaptation triggers* section of `docs/ADOPTION-GUIDE.md`. Briefly: the framework is most likely a fit for programmes that span at least eighteen months, that involve at least three intended publications, that use AI assistance routinely, and that target peer-reviewed venues at the top quartile of their disciplinary categories. The framework is least likely a fit for single-thesis programmes, AI-free programmes, or genuinely short programmes where the artefact-spine overhead is not amortised.

**How long does the install take?**

The bootstrap-prompt path (Path A in `docs/INSTALLATION.md`) takes forty-five to ninety minutes for a single chat session. The manual path (Path B) takes longer because the adopter populates each artefact themselves, but it spreads the cost across multiple sittings. Either path is followed by an onboarding investment of one to two evenings (for adopters with prior exposure to spec-driven development or academic methodology) to three to five evenings (for adopters without that exposure) to read the framework's documentation and absorb its loop's vocabulary.

**Can I use the framework without an AI assistant?**

In principle, yes — the durable artefacts and the four-step loop work without AI augmentation. In practice, the framework was designed to address the failure modes of AI-augmented research, and many of its discipline benefits accrue specifically to AI-assisted work. An AI-free adopter would be using the framework primarily as a project-management overlay rather than as the LLM-discipline tool it was designed to be.

**Does the framework work with [my preferred AI assistant]?**

The framework was developed and validated in Claude desktop's Cowork mode. Other assistants with comparable file-access and persistent-memory capabilities are expected to support it but have not yet been validated. See `docs/INSTALLATION.md` for the assistant-specific notes that exist; documentation of other validated runtimes is welcome through the contribution process.

**Is my data private?**

The framework does not collect, transmit, or process your data; it is a configuration of files and conventions that lives entirely in your working environment. Whatever privacy properties your AI assistant offers are unchanged by the framework. The framework's discipline of treating AI assistance as a research aid rather than as an authorship surrogate (`REQUIREMENTS.md` R8) tends to push adopters toward more conservative data-handling practices, but the framework itself is data-handling-neutral.

## During the first paper

**The bootstrap prompt asked me six questions and I do not yet know the answer to one of them. What do I do?**

Pause the install at the question you cannot answer yet. The framework presupposes that an adopter knows their programme's substantive domain, work streams, time horizon, external gates, tone preferences, and existing skill bundles before installing. If one of these is genuinely undecided, the framework's discipline cannot apply to it cleanly. Resolve the open question first — by consultation with your supervisor, by review of your funding proposal, by clarification of your institutional milestones — and resume the install once you have an answer. Half-answered standing instructions will not produce reliable framework behaviour.

**My CONTEXT.md has a question I do not yet know the answer to. What do I do?**

The CONTEXT skeleton's *Decision required* prompts are not optional; if a prompt is unanswered, the per-paper chat does not advance from `discuss-phase` to `plan-phase`. The framework treats this as a feature: the question should be answered before drafting begins, because answers reached mid-draft tend to invalidate prior work. If the question requires external input — supervisor consultation, ethics committee approval, data-access negotiation — record that the answer is *pending external input* and pause the per-paper chat until it arrives. Do not advance `plan-phase` against an unanswered CONTEXT prompt.

**I drafted a paragraph that I think is good but the persona returns it for revision. What do I do?**

The persona's evaluation is not binding in the same way the audit gate's verdict is binding. The persona is a sentence-level discipline; the audit gate is the programme-level enforcement mechanism. If the persona returns a paragraph for revision and you disagree, you have three options: revise the paragraph along the persona's suggested lines; edit the persona's standards in `templates/SKILL.template.md` if you genuinely believe the persona is wrong (this is rare and should be documented); or override the persona's recommendation for the specific paragraph but expect the audit gate to evaluate the same paragraph against the same standards. The persona is correct most of the time; when you disagree with it, expect the audit gate to side with the persona.

**The Paper Evaluation Chamber returned anything-but-Publish-immediately. What do I do?**

Take the verdict seriously and revise. The Chamber's purpose is to catch problems before submission, not to bless the work as ready. A verdict of *Revise-and-resubmit* — the most common non-Publish verdict — is itself blocking under R10; the paper returns to its per-paper chat, the revisions are made, and the Chamber re-evaluates from scratch. There is no override. The discipline is the value.

If the Chamber's verdict seems wrong — for example, if it requests revisions that are out of scope for the paper's contribution claim — re-read the verdict's reasoning carefully. The Chamber's reasoning is more often than not correct. If after careful re-reading you still believe the Chamber is wrong, document your disagreement in the per-paper chat and either revise the paper anyway (deferring to the Chamber's discipline) or revise the Chamber's standards in `REQUIREMENTS.md` R10 (rare; document the change).

## During the long run

**I have not opened the project in three months. How do I resume?**

Open Pipeline Control. Read `PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`, `STATE.md`, `OPERATING-MODEL.md`, and `DESIGN-RATIONALE.md` in that order. The state of the programme is in `STATE.md`; the standing instructions are in your AI assistant's long-term memory; the framework's discipline is in the artefacts. The framework is designed for exactly this situation; resumption from a multi-month gap is a first-class use case, not an exception.

**A new paper has emerged that I want to add to the programme. What do I do?**

Edit `ROADMAP.md` to add the new paper to the appropriate phase or to introduce a new phase if the new paper does not fit existing phases. Update `STATE.md` to reflect the new paper. Open a per-paper chat and seed `{n}-CONTEXT.md`. The framework's modularity allows additions without restructuring.

**My target outlet has changed. What do I do?**

Update the relevant entries in `ROADMAP.md` and `STATE.md`. Re-run the cross-paper coherence pass against the new outlet's recent record (per R12); the new outlet's recent five-year record may have anchor articles different from the old outlet's, and the paper's positioning may need adjustment. The framework treats outlet changes as in-scope events, not as exceptions; the cost is a few hours of repositioning work, not a re-draft.

**My discipline's editorial culture differs from what the audit gate persona simulates. What do I do?**

Edit the audit-gate persona configuration in `REQUIREMENTS.md` R10 to match your discipline's editorial culture. The default persona reflects management research's editorial culture; adopters in other disciplines will often need to adjust. The substantive checklist the Chamber evaluates against (contribution, rigour, transparency, ethics, prose, replicability) is robust across disciplines; the procedural framing of the persona (HBS Dean / Editor-in-Chief at world-elite journal) is the part most often adapted.

## Forking, contributing, and citing

**Can I fork the framework and adapt it for my discipline?**

Yes. The framework is licensed CC BY-SA 4.0; you are free to fork, adapt, and redistribute, provided you credit the original author, indicate that changes were made, and license your derivative under the same terms. See `LICENSE` for canonical terms.

**How should I cite the framework if I use it?**

The recommended citation form is in `README.md` and in `CHANGELOG.md`. Briefly: cite Mohamad-Zouheir Chouman as the author, *Stoa* as the work, the year of the version you used, and the repository URL and version. When the framework's accompanying methodological paper is published in a Q1-tier venue, the citation form will update; the update will be announced in `CHANGELOG.md`.

**I want to contribute a worked example or a discipline adaptation. How?**

Read `CONTRIBUTING.md`, then either open an issue describing your proposed contribution (recommended for substantive contributions) or open a pull request directly (for minor fixes). Worked examples and adaptations from disciplines the framework has not yet been validated against are particularly welcome.

**I have a question that is not answered here. Where do I ask?**

Open an issue against the repository. Documentation improvements — including additions to this FAQ — are welcomed through pull requests.
