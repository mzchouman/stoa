# ROADMAP.md — Phased Schedule (Template)

> **Adopter notes.** Replace each `[BRACKETED PLACEHOLDER]` with content specific to your programme. Italicised paragraphs are guidance and should be deleted from the final populated file. The roadmap is the authoritative sequencing artefact; the live status board is `STATE.md`; the binding standards are `REQUIREMENTS.md`; the workflow loop is `OPERATING-MODEL.md`.

This roadmap is the authoritative sequencing artefact for the programme. [NUMBER] non-overlapping phases govern execution. Within a phase, the listed items run in parallel; between phases, work proceeds strictly in sequence — no Phase *n+1* item begins research, drafting, or evaluation until every Phase *n* item has cleared the Paper Evaluation Chamber and reached its targeted submission status. Each output appears in exactly one phase. Stream tags and any cross-deliverable traceability tags (per `REQUIREMENTS.md` R9) are binding metadata.

The live status board is in `STATE.md`. The binding standards are in `REQUIREMENTS.md`. The workflow loop is in `OPERATING-MODEL.md`.

---

## Phase 1 — [TIMING] — *[STATUS, e.g. Complete; Active; Queued]*

### [OUTPUT 1 TITLE]
- **stream:** [STREAM TAG IF APPLICABLE]
- **traceability tag:** [PROGRAMME-SPECIFIC TAG, e.g. RQ1, Client objective 1, Capstone foundation]
- **target outlet:** [TARGET — for example, "a Q1-tier journal in [subject category]"; do *not* name specific journals here unless your programme convention requires it]
- **status:** [STATUS]
- **depends_on:** [DEPENDENCIES OR — if Phase 1]
- **recognition targets:** [LIST APPLICABLE BEST-PAPER, EMERGING-SCHOLAR, OR OTHER AWARDS]
- **chat:** [CHAT NAME]

### [OUTPUT 2 TITLE — IF APPLICABLE]
- **stream:** [STREAM TAG IF APPLICABLE]
- **traceability tag:** [PROGRAMME-SPECIFIC TAG]
- **target outlet:** [Q1-TIER VENUE IN RELEVANT SUBJECT CATEGORY]
- **status:** [STATUS]
- **depends_on:** [DEPENDENCIES]
- **recognition targets:** [LIST]
- **chat:** [CHAT NAME]

---

## Phase 2 — [TIMING]

*Repeat the per-output structure above for each output in Phase 2. Within a phase, two or more outputs may run in parallel as long as their drafting chats are independent. The standard pattern is two outputs per phase running in parallel; programmes with more or fewer outputs per phase adapt accordingly.*

### [OUTPUT TITLE]
- **stream:** [STREAM TAG IF APPLICABLE]
- **traceability tag:** [PROGRAMME-SPECIFIC TAG]
- **target outlet:** [Q1-TIER VENUE IN RELEVANT SUBJECT CATEGORY]
- **status:** [STATUS]
- **depends_on:** [DEPENDENCIES]
- **recognition targets:** [LIST]
- **chat:** [CHAT NAME]

---

## Phase 3 — [TIMING]

*Continue the pattern for each phase. Every phase is non-overlapping with every other phase in time and in active-chat allocation. Each phase has at least one output and may have more; phases need not be the same length.*

[FILL IN PER-PHASE STRUCTURE]

---

## Final phase — [CAPSTONE OR CONCLUSION, IF APPLICABLE]

*If your programme has a capstone — a final integrating output that synthesises the prior phases — describe it here. The capstone cannot open until all preceding outputs are closed.*

[CAPSTONE STRUCTURE]

---

## Cross-cutting parallelism rules

These rules govern execution across phases. They are binding and apply regardless of the specific number of phases or outputs.

1. **Within a phase:** the listed outputs run in parallel in dedicated per-paper chats. They share the Pipeline Control chat for cross-output coherence checks but never share drafting context. (Per `REQUIREMENTS.md` R12.)
2. **Between phases:** the gate is binary. Phase *n* must close — meaning every output in the phase has cleared the Paper Evaluation Chamber and reached its targeted submission status — before Phase *n+1* opens. (Per `REQUIREMENTS.md` R10 and the workflow discipline in R11.)
3. **Cross-deliverable traceability:** every output that triggers R9 carries its traceability tag end-to-end. The tag determines whether the output has done its programme-anchoring job, regardless of journal acceptance status.
4. **Convergence rule (if applicable):** if your programme has a convergence stream that synthesises across earlier streams, those convergence outputs cannot be opened until at least one upstream-stream output from each adjacent prior phase has closed.
5. **Capstone rule (if applicable):** the capstone cannot open until all preceding outputs are closed.

---

## How to maintain this artefact

Update `ROADMAP.md` whenever an output's title, target outlet, dependencies, or recognition targets materially change. Update `STATE.md` more frequently — whenever an output changes phase status, the Paper Evaluation Chamber returns a verdict, or a chat is opened or closed. The roadmap is the *plan*; the state board is the *current observation*. Drift between the two is a defect and should be reconciled in Pipeline Control.
