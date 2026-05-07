# STATE.md — Live Status Board (Template)

> **Adopter notes.** Replace each `[BRACKETED PLACEHOLDER]` with content specific to your programme. Italicised paragraphs are guidance and should be deleted from the final populated file. Update this file frequently — whenever an output changes phase status, the Paper Evaluation Chamber returns a verdict, a target outlet is reaffirmed or changed, a chat is opened or closed, or a framework artefact is amended. Stale state-boards are worse than no state-board.

**Last updated:** [YYYY-MM-DD] (by Pipeline Control chat).

This is the live status board for the [NUMBER]-output programme running under Stoa. The framework's name and orientation are introduced in `PROJECT.md`; the binding standards are in `REQUIREMENTS.md`; the phased schedule is in `ROADMAP.md`; the playbook is in `OPERATING-MODEL.md`.

## Programme-level state

| Field | Value |
|---|---|
| Active phase | **Phase [N]** ([TIMING]) |
| Phases closed | [LIST OR — if none yet] |
| Phases queued | [LIST] |
| Active per-paper chats | [LIST CHAT NAMES] |
| Pipeline Control chat | this chat |
| Paper Evaluation Chamber chat | [STATUS — open/idle/closed; LAST VERDICT] |
| Standing instructions in force | (1) [LIST EACH STANDING INSTRUCTION YOUR PROGRAMME HAS SAVED TO MEMORY, NUMBERED] |

## Framework artefact inventory at workspace root

*Maintain this table. Mark artefacts as **Stable**, **Updated**, **Elevated**, **New**, or **Pending**. Update the *Last revision* column with an ISO date and a one-line description of the change.*

| Artefact | Status | Last revision |
|---|---|---|
| `PROJECT.md` | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |
| `REQUIREMENTS.md` | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |
| `ROADMAP.md` | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |
| `STATE.md` | Updated | [YYYY-MM-DD] — this revision |
| `OPERATING-MODEL.md` | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |
| `DESIGN-RATIONALE.md` | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |
| `BIBLIOGRAPHY.md` | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |
| `[n]-CONTEXT.md` (each active phase) | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |
| `.claude/skills/academic/SKILL.md` *or equivalent* | [STATUS] | [YYYY-MM-DD] — [DESCRIPTION] |

## Per-output state

*Repeat the structure below for each output in your programme — typically one block per active output, plus a single block for queued outputs that share the same status.*

### [OUTPUT TITLE]
- **phase:** [N]
- **stream:** [STREAM TAG IF APPLICABLE]
- **traceability tag:** [TAG IF APPLICABLE]
- **target outlet:** [Q1-TIER VENUE IN SUBJECT CATEGORY]
- **status:** [STATUS — Active – discuss-phase / Active – plan-phase / Active – execute-phase / In Chamber / In review / In R&R / Accepted / Rejected]
- **last evaluation:** [DATE AND VERDICT, OR "—" IF NONE YET]
- **next milestone:** [NEXT EXPECTED EVENT]
- **action items:** [LIST]

### Queued outputs ([LIST OUTPUT NUMBERS OR TITLES])
- **status:** Queued. Cannot open until predecessor phase closes (per `ROADMAP.md` parallelism rules).
- **action items:** none until predecessor phase closes.

## Recognition / external-gate state (if applicable)

*If your programme is engineering for specific recognition targets — best-paper awards, emerging-scholar awards, conference acceptances, institutional milestones — track them here. Use the table format below or adapt as suits your programme.*

| Target | Eligible outputs | Status |
|---|---|---|
| [AWARD OR GATE] | [LIST] | [STATUS] |

## Outstanding decisions for Pipeline Control

*Items that belong in this chat and are not delegated to per-paper chats. Number them. Resolve them in this chat or, if they require external input, mark them as awaiting that input.*

1. [DECISION ITEM]
2. [DECISION ITEM]
3. [DECISION ITEM]

## Bibliography revisions

*Whenever `BIBLIOGRAPHY.md` is amended — entries added, removed, or corrected — record the change here with date and one-line description.*

- [YYYY-MM-DD] — [DESCRIPTION OF CHANGE]
