# Deep Scout — Maintenance Guide

## Quarterly refresh (every ~90 days)

1. **Re-open time-sensitive sources:** Google operators page (operator
   deprecations), HN Algolia API (rate limits), S2AG/OpenAlex/Crossref docs
   (endpoint + limit changes), Magiran (coverage counts), OWASP LLM Top 10
   (ranking changes), NIST AI RMF (1.0 revision status).
2. **Re-check redirects:** paperswithcode.com (still → HF Papers?),
   docs.openalex.org, docs.github.com search paths (find new repo-search URL).
3. **Retry UNVERIFIED:** SID.ir content, `intitle:`/`inurl:` on Google,
   arXiv chunks 1–6, SO chunk 2, CRAAP chunks 1–2, Grounded-theory chunks
   1–10, OWASP chunk 2, S2 chunk 2, NIST chunk 2, eL8zL5 chunk 3.
4. **Re-validate architectures:** gpt-researcher README (planner/executor
   still current?), STORM activity, lm-eval task-priority list.
5. **Bump version + date** in all 8 files; log changes in REPORT (append
   "Refresh log").

## Triggered refresh (any time)

- A cited URL 404s or redirects somewhere new → verify + update within the
  report that discovers it; file an issue-style note in the log.
- A new injection technique appears in OWASP/Anthropic/OpenAI guidance →
  update Sheet 8 + Module 9 immediately.
- Search-engine operator changes → update Sheet 3 + Module 4.

## Versioning

- `vMAJOR.MINOR`: MINOR = refresh with same structure; MAJOR = module
  added/removed/renumbered or verdict scale changed.
- Keep one prior version: `system-prompt.en.v<prev>.md` (max 1 back).

## Quality gates for any edit

- No claim without URL + access date (or UNVERIFIED label).
- No URL copied from memory — open it or mark snippet-only.
- Test count stays ≥15 specified / ≥5 executed; re-run ≥2 grounded tests
  after MAJOR changes.
- FA and EN stay in sync (same module numbers, same examples).
- Compact stays <1,500 words.

## Ownership

Maintainer: repo owner. Reviewers: anyone running Deep Scout missions —
file findings (dead links, new operators, better sources) as mission-log
notes; maintainer triages quarterly.
