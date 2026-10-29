# App Scout — Final Report (v1.0, 2026-10-29)

## a. Numbers
- Searches run: **20** (8 GitHub-scoped + 2 video-ID + 10 Phase-5 grounding).
- Repos reviewed (opened + read): 6 (awesome-selfhosted, sindresorhus/awesome, offa/android-foss, microsoft/winget-pkgs,
  + topic/trending pages) plus ~40 repos surveyed via search snippets (taps, forks, scanners, alternatives lists).
- Articles/guides read: **20** (GitHub code-search syntax ×2 chunks, winget, brew, Flatpak, F-Droid Anti-Features, AUR,
  npm audit, PyPI install, GHCR, OpenAlternative, AlternativeTo, Student Pack, Modrinth, VS Marketplace + repo pages).
- Videos analyzed: **4** (real transcripts read in full: 3× winget, 1× F-Droid).
- Grounded test runs: 5 (R1 23/25, R2 25/25, R3 24/25, R4 25/25, R5 24/25) → 5 fixes folded into v1.0.

## b. What could not be verified
Repo-search docs canonical URL (old URL 404s) · IzzyOnDroid/Flathub/OSV/VirusTotal/crates/Docker-Hub/Nexus/CurseForge/
Workshop/education-pricing/Obtainium pages (not opened — agent must check live) · any per-app facts (by design:
re-searched per request) · AFFiNE exact license (MIT vs NOASSERTION conflict — needs LICENSE file read) · ShareX MIT
claim from `Desktop-App-ShareX` org (treat as impersonation suspect; canonical GPL-3.0 needs LICENSE confirmation).

## c. Biggest risks & weaknesses of this agent
1. **Aggregator laundering** — directories/LLM-SEO pages (stars, licenses) look authoritative but drift; mitigated by F1
   (open repo + LICENSE) but depends on agent discipline. 2. **Lookalike repos/orgs** (ShareX case, counterfeit
   extensions) — bidirectional-link rule helps; zero-days still possible. 3. **Crowdsourced-rank bias** (AlternativeTo
   votes/sponsors) mistaken for vetting — cross-check rule required. 4. **No-web degradation** — without live checks the
   agent is a search planner, not a verifier; freshness protocol says so explicitly. 5. **Supply-chain speed** — malicious
   packages appear hourly; scanner feeds (OSV/MAL/GHSA) must be consulted per install, not cached.

## d. How to keep it updated
Monthly pass per `maintenance-guide.md`: re-open directories + package-manager docs, resolve the docs-404, close source
gaps, re-verify Student Pack, re-run ≥2 grounding searches (append-only rows), bump version + stamp on change.

## e. 5 changes that would improve it most
1. Add a live OSV/GHSA lookup step to §4 Security (currently "where checkable"). 2. Add Flathub publisher-verification
   + VS Marketplace publisher checks as explicit sub-steps (docs partially unopened). 3. Add a Persian-app-source sheet
   (Cafe Bazaar/Myket rules differ; unresearched). 4. Add download-checksum automation (script snippet for SHA-256/PGP
   verify per OS). 5. Add a "report back" loop: user confirms install success → agent logs it (needs memory whose design
   is out of scope).
