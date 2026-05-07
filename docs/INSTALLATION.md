# INSTALLATION.md — Assistant-Specific Install Notes

This document describes how to install Stoa in the AI assistants where the framework has been validated, and what to expect when adopting the framework in assistants that have not yet been validated. The recommended primary install path for first-time adopters is the bootstrap prompt (`BOOTSTRAP.md`); the manual paths described here are alternative routes for adopters who want finer control over the install or whose assistant runtime makes the bootstrap prompt awkward.

## Validated runtime

**Claude desktop, Cowork mode** — the framework was developed and validated in this runtime through the production of the demonstration programme (single site, multi-paper). Cowork supplies the file-access capabilities, persistent memory, and project-scoped skill installation that the framework's discipline relies on. Other Anthropic Claude product surfaces (Claude API with file tools, Claude Code) are expected to support the framework cleanly but have not yet been validated against the full loop.

### Path A — bootstrap prompt (recommended)

Open `BOOTSTRAP.md`. Copy the entire prompt block between the two `── COPY EVERYTHING BELOW/ABOVE THIS LINE ──` rules. Open a new chat in Claude desktop, with a workspace folder selected, and paste the prompt as the very first message of that chat. Approve the assistant's six clarifying questions, review the artefacts as they are generated, and let the assistant complete the install. The whole process takes forty-five to ninety minutes.

### Path B — manual install

For adopters who prefer to populate the artefacts themselves rather than via the assistant's clarifying questions:

1. Copy the contents of `templates/` into the root of your research-programme working directory. Rename each file from `*.template.md` to `*.md` (for example, `PROJECT.template.md` becomes `PROJECT.md`).
2. Edit each artefact by replacing each `[BRACKETED PLACEHOLDER]` with content specific to your programme. Delete italicised guidance paragraphs from the populated files; they are intended only as adopter-facing notes during population.
3. Install the persona skill by copying `templates/SKILL.template.md` to your assistant's project-scoped skills directory. In Cowork, that path is typically `.claude/skills/academic/SKILL.md` inside your workspace folder. Rename the file from `SKILL.template.md` to `SKILL.md` at install.
4. In a new chat with the workspace folder selected, save the three standing instructions described in `BOOTSTRAP.md` Step 1 to long-term memory before doing any other work.
5. Begin work by opening the first per-paper chat and running `discuss-phase` against the seeded `{n}-CONTEXT.md` skeleton.

## Adaptation notes for unvalidated assistants

The framework presupposes that the assistant has the following capabilities. Validate that your assistant supports each before attempting to adopt the framework.

- **File access in a project-scoped working directory.** The assistant must be able to read and write Markdown files in a directory you control, including creating new files, editing existing ones, and listing directory contents.
- **Persistent memory across chat sessions.** The assistant must support some form of long-term memory — durable across chats — that you can write to and that the assistant reads when starting a new chat. The framework's standing instructions live in this memory.
- **Project-scoped skills or persona configuration.** The assistant must support some form of persona or system-prompt configuration that is project-scoped. The Academic Vern skill lives in this configuration.
- **Multi-chat workflows.** The framework's discipline of per-paper chats with role-locked CHAT OPENERs presupposes that you can open multiple independent chats against the same project, each with its own context.

Assistants that meet all four requirements should support the framework cleanly. Assistants that meet some but not all may require adaptation; documentation of such adaptations through the framework's contribution process (`CONTRIBUTING.md`) is welcome.

### OpenAI ChatGPT (with Code Interpreter and project-scoped instructions)

ChatGPT's project feature supplies project-scoped instructions and the GPT layer can be used as a workspace for the framework. Persistent memory across chats is supported but is more limited than Cowork's; the durable artefacts at the project root are correspondingly more important. File access is limited to the chat session unless extended by Code Interpreter; adopters should be prepared to upload artefacts at the start of each session if their plan does not support persistent file storage. Path B (manual install) is the cleaner route for ChatGPT adopters; the bootstrap prompt path is workable but requires the adopter to follow up with file uploads.

### Google Gemini (Workspace integration)

Gemini's Workspace integration can serve as the workspace folder if Google Drive is the storage. The persona skill installs as a Custom Gem. Validation of the framework against Gemini is in progress; documentation of any adaptations required will be added to this file as it accumulates.

### Local LLMs (Ollama, LM Studio, llama.cpp, vLLM)

Local LLMs with file-access tooling (for example, configured through OpenWebUI, librechat, or similar interfaces with file plugins) can support the framework provided the model has sufficient context length to load the framework's artefacts and provided the runtime supports project-scoped persistent memory. The framework's artefact discipline is well-suited to context-constrained local models because the durable files reduce the amount of context the model must hold in memory; however, the persona discipline depends on the model's instruction-following quality, which varies by model. Adoption with strong open-weight models (Llama 3.1 70B and above, Qwen2.5 72B, DeepSeek V3, or similar) is expected to be cleaner than with smaller models.

## Migration from a prior framework

If you are currently using a different research-management framework (a custom Notion setup, a spec-driven-development variant, an institutional doctoral-writing platform), the framework can be installed alongside without disturbing your existing tooling. The framework's artefacts live in the project root and do not depend on any specific tooling integration; if your prior framework lives in a different surface (a cloud service, a specific app), the two can co-exist while you decide whether to fully migrate.

For migration *to* the framework from a prior setup:

1. Read `README.md`, `BOOTSTRAP.md`, and at least one of the artefact templates before starting.
2. Choose a single intermediate state — for example, *artefact spine populated, persona skill installed, but no audit gate yet* — and run one paper through the loop to that state to test the framework's fit before fully committing.
3. If the test paper shows the framework's discipline is workable for your project, convert your other in-flight work to the framework's loop. If the test paper shows the framework is not a fit, document why in your project's `STATE.md` and either adapt the framework or revert.

## Troubleshooting

The framework's most common adoption issues, in rough order of frequency:

- **The assistant forgets the standing instructions across sessions.** This is a memory-propagation issue (named in `templates/DESIGN-RATIONALE.template.md` section 8). The mitigation is to ensure the four root artefacts are read at the start of every new chat; if the assistant supports a per-project system prompt, encode the three standing instructions there as well.
- **The assistant produces drafts without running the loop.** This is a workflow-discipline failure (`REQUIREMENTS.md` R11). The mitigation is to begin every chat with a CHAT OPENER that names the role and refuses to draft outside the loop.
- **Citations are inconsistent across artefacts.** This is a cross-output coherence failure (`REQUIREMENTS.md` R12). The mitigation is to maintain `BIBLIOGRAPHY.md` actively and to run a coherence pass at every phase boundary.
- **The audit gate is bypassed under deadline pressure.** This is the failure mode the gate was designed to prevent and is the framework's most consequential adoption failure. The mitigation is the procedural one: do not submit until the Chamber returns *Publish-immediately*. If the gate's discipline cannot be maintained under your operating constraints, the framework may not be the right fit for your programme.

## Reporting installation issues

Installation issues that are not resolved by this document or by `docs/FAQ.md` should be reported through the repository's issue tracker (see `CONTRIBUTING.md`). Documentation of new assistant adaptations, new troubleshooting findings, and new validated runtimes is welcome through pull requests.
