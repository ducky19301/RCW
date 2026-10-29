# RCW — Revised Code of Washington

Offline markdown snapshot of the **Revised Code of Washington** (all published Titles), for local search, citation, and agent/skill use.

| Directory | Covers |
|-----------|--------|
| [`wa-rcw-1-50/`](./wa-rcw-1-50/) | Titles 1–50 (+ lettered variants 9A, 23B, 28A/B/C, 29A/B, 30A/B, 35A, 50A/B) — 58 Titles, ~1,873 chapters |
| [`wa-rcw-51-100/`](./wa-rcw-51-100/) | Titles 51–91 (+ lettered variants 62A, 70A, 71A, 79A) — 42 Titles, ~891 chapters |

**Snapshot date:** 2026-05-20 (from the Washington State Legislature **2025 RCW Archive**).

## Layout

Each Title is a folder with:

- `README.md` — title playbook (scope, grep tips, caveats)
- `rules.md` — consolidated statute body for that Title

Each half also has a router `SKILL.md` for Claude Code / agent skill install.

```sh
# Example: find a section
grep -n -E 'RCW\s+46\.61\.502' wa-rcw-1-50/46-motor-vehicles/rules.md

# Install as Claude Code skills (optional)
cp -r wa-rcw-1-50   ~/.claude/skills/rcw-1-50
cp -r wa-rcw-51-100 ~/.claude/skills/rcw-51-100
```

## Source & provenance

Statute text is derived from the official Legislature “Complete Title” PDFs:

- https://lawfilesext.leg.wa.gov/law/RCWArchive/2025/
- https://app.leg.wa.gov/RCW/

Packaging, Title READMEs, and `SKILL.md` routers come from [Civic-Informer/wa-state-legal](https://github.com/Civic-Informer/wa-state-legal) (MIT). Official RCW text is a government edict and is not copyrightable; see `LICENSE`.

## Disclaimer

Not legal advice. Verify against the official Legislature site for filing-critical or time-sensitive use — this snapshot will drift as statutes are amended.
