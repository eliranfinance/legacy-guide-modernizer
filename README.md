# Legacy Guide Modernizer

A portable instruction skill for turning old tutorials, forum exports, scans, and mixed archives into safe, current, practical runbooks.

It was distilled from a 68-item Hebrew archive spanning PC building, Windows maintenance, networking, recovery, graphics, game creation, optical media, and security-related material. The useful pattern was not the obsolete commands; it was the editorial method: preserve intent, separate trustworthy maintenance from dangerous shortcuts, and modernize around the user's actual environment.

## What it does

- inventories and clusters a guide corpus
- extracts reusable concepts while preserving provenance
- flags obsolete versions, dead links, unsafe steps, and exposed secrets
- rewrites surviving advice into prerequisites, actions, verification, rollback, and troubleshooting
- converts harmful offensive material into defensive guidance
- works in English or Hebrew and can be pasted into Claude, ChatGPT, Grok, or another assistant

## Install

### Claude-style skill

Copy `SKILL.md` into the assistant's skills directory or upload it as a project skill.

### ChatGPT or Grok

Paste the contents of `SKILL.md` as a project/system instruction, or use the compact prompt in `adapters/portable-prompt.md`.

## Example prompts

- "Modernize these archived Windows maintenance notes for Windows 11. Keep only safe, reversible steps."
- "Cluster this folder of old tutorials and produce a source-backed runbook for recovering deleted files."
- "Separate defensive security lessons from the offensive instructions and rewrite them for an authorized home lab."
- "Translate the result to Hebrew, but keep commands, warnings, and verification checks exact."

## Design principles

Current sources beat nostalgia. Reversible steps beat clever shortcuts. Observable verification beats confident wording. A useful refusal should redirect to a safe, authorized outcome.

## License

MIT. The skill is original synthesis; source archives are not redistributed here.
