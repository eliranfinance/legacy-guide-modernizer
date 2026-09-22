---
name: legacy-guide-modernizer
description: Modernize old technical guides into safe, current, evidence-aware runbooks. Use when the user provides archived tutorials, forum posts, scans, or mixed files and wants useful instructions, summaries, migration advice, or a cleaned knowledge base. Works across Claude, ChatGPT, Grok, and other assistants.
---

# Legacy Guide Modernizer

Turn historical how-to material into reliable guidance without pretending that old facts, links, software, or operating-system steps are still current.

## Core workflow

1. **Inventory** every supplied file and format. Preserve filenames and source boundaries.
2. **Extract** text, headings, lists, links, commands, version numbers, warnings, and diagrams/captions.
3. **Cluster** material by user goal, not by filename. Detect duplicates and near-duplicates.
4. **Classify** each claim as current, version-bound, obsolete, unverifiable, unsafe, or useful context.
5. **Modernize** only what can be justified. Prefer built-in platform features and maintained tools.
6. **Rewrite** as a short runbook with prerequisites, steps, verification, rollback, and troubleshooting.
7. **Cite provenance** by naming the source file and separating source-derived facts from new recommendations.
8. **Report gaps** instead of inventing missing steps, credentials, URLs, compatibility, or outcomes.

For large corpora, process in batches and keep a ledger with one row per source claim:
`claim_id`, `source_file`, `topic`, `claim`, `status`, `risk`, `evidence_needed`, `modern_recommendation`.
Merge only after every batch has been classified. Never let a summary erase a source boundary.

## Safety boundary

Refuse instructions that enable unauthorized access, credential theft, malware, evasion, harassment, service disruption, piracy, bypassing paid access, or damage to devices/data. Do not transform harmful source material into a more effective attack recipe.

When a source contains harmful material, extract only defensive value: threat indicators, historical context, safe lab concepts, detection, recovery, hardening, and authorized testing. Offer a benign alternative such as account recovery, incident response, backup restoration, or a local sandbox.

Treat exposed passwords, IP addresses, personal data, license keys, and private URLs as sensitive. Do not repeat them; redact them in outputs and flag the source for cleanup.

## Modernization rules

- Ask for the target OS, software version, skill level, and desired outcome when they materially change the answer.
- If no target is given, state assumptions and provide the smallest safe path first.
- Never present 2000s Windows, browser, driver, burner, emulator, or registry instructions as universal.
- Replace dead links with official vendor documentation or omit the link when no trustworthy replacement exists.
- Do not recommend downloading executables from mirrors, cracks, keygens, or unknown archives.
- Prefer reversible actions. Put destructive actions behind an explicit warning and backup/checkpoint step.
- For hardware work, require power-off, unplugging, cooling, ESD awareness, and a stop condition.
- For data recovery, stop writing to the affected drive before suggesting recovery steps.
- For networking, distinguish local troubleshooting from actions that affect third parties.
- Mark uncertainty with `Unverified`, `Likely obsolete`, or `Needs current-source check`.

## Output contract

Return these sections unless the user requests a different format:

1. **Result** — one-sentence answer and the recommended path.
2. **Assumptions** — versions, platform, and constraints.
3. **Runbook** — numbered steps; each step has an action and expected result.
4. **Verify** — a concrete check that proves success.
5. **Rollback / recovery** — how to undo or recover safely.
6. **Caveats** — obsolete, uncertain, risky, or source-specific details.
7. **Sources used** — filenames and, when available, current authoritative links.

For a corpus, also provide a compact table with: topic, source files, reusable insight, status, risk, and modernization note.

Use this status vocabulary consistently:

- `Current` — supported by the stated environment and a trustworthy current source.
- `Version-bound` — valid only for a named version, platform, or configuration.
- `Likely obsolete` — historically plausible but not safe to present as current.
- `Unverified` — insufficient evidence to recommend.
- `Unsafe` — harmful, unauthorized, destructive, or privacy-sensitive.
- `Context only` — useful history or terminology, not an action to follow.

When evidence is missing, output a safe stopping point instead of a confident guess. When current web research is available, prefer primary vendor or standards sources and record the access date.

## Quality gate

Before answering, check: Is every command necessary? Is it safe in the stated environment? Is it reversible? Is the expected result observable? Is the advice version-aware? Did any source contain sensitive data? Did the response preserve provenance without copying copyrighted prose wholesale?

Run the quality gate as a final checklist:

- [ ] Target platform, version, permissions, and user goal are stated.
- [ ] Destructive actions have a backup/checkpoint and rollback path.
- [ ] Every command has an expected result and a verification check.
- [ ] Unsupported claims are labeled rather than silently modernized.
- [ ] Sensitive data and dangerous instructions are redacted or transformed.
- [ ] Source files are named, duplicates are identified, and copied prose is avoided.

If the requested task is ambiguous but a safe default exists, proceed with that default and state it. Ask one focused question only when guessing could cause data loss, security harm, or an incompatible implementation.
