# AppScout — Maintenance Guide (v1.0)

Keep the Scout's sources, directories, and commands correct. Freshness baseline: 2026-10-29.

## 1. What goes stale fastest (check in this order)
1. **Per-app facts** (versions, licenses, pricing, health) — never stored; the agent re-searches per request. No action.
2. **Directory shapes** (OpenAlternative/AlternativeTo URL patterns, filter taxonomies, sponsored-label wording).
3. **Package-manager commands/flags** (winget/brew/apt/Flatpak/snap/F-Droid/pip/npm/cargo/docker) — re-open official
   docs each cycle; update Sheet 3.
4. **Docs URLs** (GitHub restructures docs — the old repo-search URL already 404s; track the canonical search-syntax URL).
5. **Student/education offers** (GitHub Pack rotates partners; JetBrains/Microsoft/Apple pages change yearly).
6. **Security feeds & tools** (OSV advisories, scanner repos, AUR incident list, F-Droid Anti-Features definitions).

## 2. Monthly checklist
- [ ] Re-open Sheet 2 directory homepages; fix dead URLs/patterns in Sheets 1–3.
- [ ] Re-open package-manager docs (winget, brew, Flatpak, F-Droid, AUR, npm, PyPI); update changed flags.
- [ ] Resolve the repo-search-docs 404: find canonical URL, update Sheet 1 + sources.
- [ ] Close source gaps: IzzyOnDroid, Flathub badges, OSV.dev, VirusTotal, crates/cargo-audit, Docker Hub badges,
  Nexus/CurseForge/Workshop, education pricing pages, Obtainium.
- [ ] Re-verify Student Pack offers; note rotations.
- [ ] Re-run ≥2 Phase-5 grounding searches; if verdicts changed, append dated rows to tests.md (append-only).
- [ ] Bump version + freshness stamp if anything changed (v1.1…; major on module/router changes).

## 3. File-sync rules
- Facts live in ONE place: `reference-sheets.md`. Prompts carry stamped summaries only; change sheet first, then mirror.
- Upgraded facts cite new URL + access date in `sources-and-credits.md` and leave the gap list.
- Test history is append-only: never edit old scored runs.

## 4. Monthly triage prompts (paste to any web-enabled assistant)
1. "Current GitHub repo/code search syntax qualifiers with official docs URLs."
2. "winget/brew/Flatpak/F-Droid: any changed install/upgrade/verify commands? Official URLs."
3. "OpenAlternative + AlternativeTo: URL patterns and sponsored-label wording today."
4. "GitHub Student Pack current offers; JetBrains/Microsoft student pages."
5. "OSV/F-Droid-Anti-Features/AUR: any new flags or incidents this month?"
