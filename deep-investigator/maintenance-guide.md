# Deep Investigator — Maintenance Guide

## Quarterly refresh (~90 days)

1. Re-open: Bellingcat resources, OFAC (list dates), EU Sanctions Map
   (regimes), SEC EDGAR paths, Companies House notices, ICANN RDAP docs,
   FTC alerts, TinEye index size, HIBP counts, InVID status, EB deltas.
2. Retry NOT VERIFIED: ilenc.ssaa.ir / Kateb portal, rrk.ir, SID.ir,
   OpenCorporates (cookie wall), Amnesty DataViewer, InVID plugin,
   multi-chunk tails (Bellingcat 1–3, Handbook 1–2, GIJN 1–2, AJR 1–6).
3. Refresh benchmarks: Bellingcat LLM-geolocation tests, detector-tool
   landscape (vendor claims need re-testing, never trust scores).
4. Bump version + date in all files; append refresh log to REPORT.

## Triggered refresh

- Cited URL dies/redirects → verify + update in the discovering report.
- New OWASP/ICANN/registry guidance → update Sheets 4/9 + Modules 5/13.
- New scam pattern wave (FTC alerts) → update Sheet 6 + Module 10.
- Ethics incident or prompt-injection success → immediate Module 2/13
  review; add the reframe to Sheet 9.

## Versioning

`vMAJOR.MINOR`: MINOR = refresh, same structure; MAJOR = module added/
removed/renumbered or boundary/label-scale change. Keep one prior EN
version file (max 1 back).

## Quality gates

- No rule from unopened sources (NOT VERIFIED stays out of the prompt).
- No URL from memory — open it or mark snippet-only.
- 15 tests specified / ≥5 executed; re-run ≥2 after MAJOR changes.
- FA/EN module numbers in sync; compact <1,500 words.
- Ethics modules (2, 8-media, 11) reviewed by a human on every MAJOR.

## Ownership

Maintainer: repo owner. Field findings (dead links, new operators, better
registries) arrive as case-log notes; triaged quarterly.
