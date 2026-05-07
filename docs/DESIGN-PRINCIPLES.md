# DESIGN-PRINCIPLES.md — The Principles Behind the Framework's Design Choices

This document explains *why* Stoa is configured as it is. It is the philosophical and methodological complement to the per-project `DESIGN-RATIONALE.md` template: where that template defends an instantiation in a specific programme, this document defends the framework's general configuration. Adopters who plan to fork the framework, who plan to publish methodologically about their use of it, or who simply want to understand the framework deeply enough to teach it to others, should read this document carefully.

The document is structured as five principles. Each principle states the design choice the framework makes, the alternative the framework rejects, and the reasoning behind the choice. Citations refer to the framework's bibliography template.

## Principle 1 — Durability is a property of files, not of conversations

The framework's first principle is that the persistent state of a research programme should live in *files*, not in the working memory of any AI assistant or the conversational context of any chat session. The four root artefacts (`PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`, `STATE.md`), the playbook, the design-rationale, and the bibliography are all flat Markdown files at the project root. They are read by every new chat session at start; they are written to by every chat session at close; they survive any model upgrade, any service migration, any chat interruption.

The alternative — relying on the AI assistant's persistent memory or on the model's in-context recall — is rejected because both are unreliable in ways the framework cannot tolerate. AI-assistant memories are non-deterministic in current implementations: an instruction saved to memory may or may not be retrieved on any given turn, and the assistant's behaviour can drift in ways the user does not directly observe. In-context recall fails predictably as conversations extend — the *context-rot* failure mode documented by Lund et al. (2023) and others. Files are durable because they are inspectable, version-controllable, and outside the assistant's behavioural envelope.

This principle has a cost: every artefact change must be written to a file, which adds friction compared to relying on the assistant's memory. The friction is the price the framework pays for durability. In a single-session interaction, the friction is excessive; in a multi-month programme, the friction is recovered many times over by the absence of re-litigation and re-derivation.

## Principle 2 — Quality gates are non-overridable or they are not gates

The framework's second principle is that the audit gate (`REQUIREMENTS.md` R10) must be non-overridable inside the system. This is not a stylistic preference; it is the response to a well-documented failure mode in deadline-driven scholarly work: gates that can be bypassed under pressure get bypassed under pressure, and the consequences arrive after submission rather than before.

The alternative — making the gate advisory rather than mandatory — is rejected because the empirical evidence on editorial peer review (Lamont, 2009; Hirschauer, 2010; Bornmann, 2011) consistently shows that editorial discipline is the property of structured procedure, not of individual editor judgement. A procedure that can be skipped is no procedure at all. The framework therefore configures the audit gate to issue verdicts that are operationally binary (*Publish-immediately* or anything else) and to require a fresh evaluation cycle for any non-Publish verdict, with no override and no time-discount.

The cost of this principle is that the framework can hold up submission past the adopter's preferred timeline. The framework's response is that this is a feature: a submission that misses an editor's submission window because it has not yet cleared the audit gate is a submission that was not yet ready. Adopters who consistently encounter this tension are encouraged either to budget more time for the audit cycle or to lower the audit gate's standards in their `REQUIREMENTS.md` rewrite — the latter being a more honest move than overriding a gate set at standards the adopter cannot meet.

The framework's audit gate has a candid limitation worth restating: the gate is an editorial-discipline simulator, not a real editor. Its calibration against actual editorial outcomes is unknown until a corpus of papers that have passed through it has accumulated decisions at target outlets. The non-overridability is procedural, not predictive; the gate raises the floor of what is submitted, not a guarantee of what is accepted.

## Principle 3 — Voice is a property of persona, not of checklist

The framework's third principle is that the sentence-level evidentiary standard — every claim cites; every approach is positioned comparatively; every limitation is named — is enforced through a *persona* (the Academic Vern skill) rather than through a checklist. The choice is deliberate.

The alternative — a checklist of sentence-level criteria the assistant should follow — is rejected for two reasons. First, checklists invite surface-level rule-following: the assistant produces output that satisfies the explicit criteria while missing the underlying discipline they encode. Second, checklists are brittle: as the assistant encounters paragraph types the checklist did not anticipate, it falls back to default behaviours. A persona, by contrast, encodes a *stance* that generalises across paragraph types and does not require the assistant to anticipate every rule it should follow.

The persona's stance is grounded in three traditions: Popperian falsificationism, which holds that claims acquire scientific status through exposure to refutation; Lakatosian research-programme epistemology, which holds that scholarly progress is the property of structured comparison against named alternatives; and Toulmin's argumentative structure, which supplies the paragraph-level mechanics of how an evidence-based claim is built. Together they give the assistant something stronger than rules: a perspective from which to evaluate any sentence it produces.

The cost is that personas are harder to verify than checklists. The framework cannot mechanically test whether a paragraph satisfies the persona's stance; it can only ask the audit gate to evaluate whether the paragraph would convince the persona. This is the same situation an academic reviewer faces, and the framework is comfortable with that limitation.

## Principle 4 — Compose, do not displace

The framework's fourth principle is that it composes with existing methodologies rather than displacing them. The four-step loop is compatible with Belcher's (2019) twelve-week journal-article workflow, with Bem's (2003) hourglass model for empirical-paper structure, with Booth, Colomb, Williams, Bizup, and Fitzgerald's (2016) craft-of-research foundations, and with Single's (2009) streamlined dissertation-writing process. The framework operates at a different level of abstraction: where these methodologies prescribe the *internal* discipline of writing, the framework prescribes the *operating environment* in which any of these methodologies can run.

The alternative — designing the framework as a complete replacement for existing methodologies — was rejected because it would require adopters to abandon the methodological investments they have already made. The framework does not require adopters to give up Belcher's twelve-week schedule; it provides the artefact-and-gate structure under which the schedule operates. The framework does not require adopters to abandon Bem's hourglass; it provides the operating environment in which the hourglass paragraph-by-paragraph is drafted. This compositional posture is what makes the framework adoptable by candidates whose existing practices are working.

The cost is that the framework is not a one-stop shop: an adopter still needs to bring (or learn) the discipline-specific writing methodology that operates inside the framework's loop. The framework is a scaffold, not a comprehensive writing tutor.

## Principle 5 — Architecture stays clean by being layered

The framework's fifth principle is that programme-level workflow, paper-level drafting mechanics, and sentence-level evidentiary discipline operate at different altitudes and should not bleed into one another. Stoa governs the workflow at programme level. The discipline-specific drafting bundle (if installed) governs paper-level drafting mechanics. The Academic Vern persona governs the sentence-level evidentiary standard inside both. The three altitudes are mutually compatible because each operates on a different unit of work.

The alternative — collapsing the three altitudes into a single integrated tool — was rejected because integrated tools tend to grow unmaintainable: each layer's concerns leak into the others, and changes in one layer cause unexpected behaviour in another. The layered architecture limits the scope of any change. A change to the audit gate (programme altitude) does not require changes to the persona (sentence altitude). A change to the discipline-specific drafting bundle (paper altitude) does not require changes to the artefact spine (programme altitude). The layers are independent in the sense that matters for maintenance.

The cost is that the framework requires the adopter to install three pieces (the framework itself, the drafting bundle, the persona) rather than one. The cost is paid once at install and recovered many times over in maintainability.

## Closing remark

These five principles were articulated retrospectively, after the framework had been instantiated and demonstrated. They are not a commitment to a frozen design; they are an account of what the framework currently does and why. As the framework accumulates demonstration evidence across multiple sites and disciplines, the principles may evolve. Where they evolve, the change will be recorded in `CHANGELOG.md` and explained here.

A reader who arrives at this document looking for a final word will not find one. A reader who arrives looking to understand the framework deeply enough to teach it, fork it, or critique it will find a configuration whose design choices are explicit and whose evolution is open.
