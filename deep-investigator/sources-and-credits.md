# Deep Investigator — Sources & Credits

> All web sources accessed 2026-10-29 unless noted. "Opened" = content read
> via fetch. Prior Deep Scout bank (2026-10-29) reused: Google operators,
> SearXNG, HN Algolia, SO search, arXiv, OpenAlex, PRISMA, IFCN, CRAAP,
> triangulation, OWASP LLM01:2025, Pugh, Connected Papers, S2 API, Crossref,
> NIST AI RMF, Magiran, 4 SIFT/SLR transcripts — see
> `../deep-scout/sources-and-credits.md`.

## Verification methodology (opened)

1. Bellingcat Resources — `https://www.bellingcat.com/category/resources/`
   — 2026 how-tos index (geolocation, satellite, flight tracking,
   weapons ID). Note: `/category/guides/` is 404 (dead end).
2. Bellingcat LLM-geolocation benchmark (2026-10-22)
   `https://www.bellingcat.com/resources/2026/10/22/can-llms-supercharge-geolocations-.../`
   (chunk 0 of 4) — 52 unpublished photos, 16 models; best (Opus, Fable,
   Gemini 4 Argon) >50% within 25km; none exact-spot reliable; humans key.
3. Verification Handbook — `https://verificationhandbook.com/` (chunk 0 of
   3) — EJC handbook for verifying UGC in emergencies (Silverman, Wardle,
   BBC/Storyful); editions in 10+ languages; Handbook 3 (disinformation)
   at datajournalism.com.
4. Amnesty Citizen Evidence Lab — `https://citizenevidence.org/` — Evidence
   Lab methods (digital verification, remote sensing, data science,
   well-being); case studies incl. Mariupol theatre, Gaza white
   phosphorus, Iran Baluchi protests video analysis.
5. First Draft articles — `https://firstdraftnews.org/articles/` — archived
   site (hosted by Internet Archive); misinformation playbooks, prebunking,
   influence-operation anatomies.
6. GIJN sun/shadow guide (Youri van der Weide, 2021-01-04)
   `https://gijn.org/stories/using-the-sun-and-shadows-for-geolocating-photos-and-videos/`
   (chunk 0 of 3) — SunCalc chronolocation + geolocation via camera
   direction; Lisbon case (5–10 min solve).
7. Al Jazeera AJR video verification (Mahmoud Ghazayel, 2021-11-15)
   `https://institute.aljazeera.net/en/ajr/article/1668` (chunk 0 of 7) —
   5-class fake taxonomy; reverse search = #1 skill; Amnesty YouTube
   DataViewer (UTC upload time + key frames); Google+TinEye different DBs.
8. Poynter fact-checking — `https://www.poynter.org/category/fact-checking/`
   — live fact-check feed (Oct 2026); PolitiFact rulings methodology.

## Company / sanctions / domain registries (opened)

9. SEC EDGAR search-filings — `https://www.sec.gov/search-filings` —
   company search (name/ticker/CIK/state/SIC), full-text search (20+ yrs),
   latest filings, CIK lookup, EDGAR APIs, RSS. (Note: `/edgar` redirects
   to submit-filings side.)
10. UK Companies House — `https://find-and-update.company-information.service.gov.uk/`
    — name/number/officer search, filings, disqualified directors;
    "does not check accuracy of information filed".
11. OFAC Sanctions List Search — `https://sanctionssearch.ofac.treas.gov/`
    — SDN + non-SDN lists, fuzzy matching slider; SDN updated 10/28/2026.
12. EU Sanctions Map — `https://www.sanctionsmap.eu/` (chunk 0 of 3) —
    per-country regimes incl. 3 Iran programs (HR, WMD, UAV).
13. ICANN RDAP lookup — `https://lookup.icann.org/en` — RDAP replaces WHOIS
    port-43; differentiated access; RDRS for nonpublic data (law
    enforcement/IP/consumer-protection).
14. Wikipedia List of official business registers (redirect target of
    List_of_company_registers; chunk 0 of 56) — global pointer list;
    register types (company, UBO, procurement, land). Deep-read NOT done —
    pointer use only.
15. OpenCorporates homepage — cookie wall (chunk 0 of 4, no content) —
    treated as NOT VERIFIED open; described via Lighthouse/README text only.

## Privacy / legal / scam / self-audit (opened)

16. GDPR full text — `https://gdpr-info.eu/` (chunk 0 of 3) — Reg. 2016/679;
    principles (Art. 5), lawfulness (Art. 6), erasure (Art. 17) structure.
17. FTC scams hub — `https://consumer.ftc.gov/scams` (chunk 0 of 2) —
    avoid/report/recover guides, ReportFraud.ftc.gov, 691 consumer alerts
    (impersonation, QR swaps, brushing, tax-debt, social-ad scams…).
18. EFF Surveillance Self-Defense — `https://ssd.eff.org/` (chunk 0 of 2) —
    Basics/Tool Guides/Scenarios incl. "Manage Your Digital Footprint",
    2FA, phishing, Tor/Signal guides.
19. Have I Been Pwned — `https://haveibeenpwned.com/` — email breach lookup,
    Notify Me, 1,048 sites / 17.8B addresses.

## Media tools (opened)

20. TinEye — `https://tineye.com/` (chunk 0 of 3) — 86.5B+ images,
    oldest-sort, private (no search-image retention), API/Alerts.
21. FotoForensics — `https://fotoforensics.com/` — ELA/metadata analysis
    (JPEG/PNG/WebP/HEIC/AVIF), ~9M unique images.
22. Wayback Machine — `https://web.archive.org/` (chunk 0 of 4) — 1T+ pages,
    Save Page Now, browser extensions, CDX API pattern via osint-toolkit.
23. InVID project — `https://www.invid-project.eu/` — EU video-verification
    plugin project (site news frozen ~2018; current plugin status NOT
    VERIFIED).

## Video transcripts read (4)

24. `p8tLcWpqbLs` — GeoPeter, Bellingcat "Background Check" challenge
    (chunk 0 of 3) — trolley-text clue, Overpass Turbo (shops + water
    towers + stations → 3 results), brand-logo search, street-view confirm.
25. `59mMk-k_t-U` — Shreateh, AI/deepfake detector tutorial — consumer
    detector demo (GenAI% + face-manipulation% + model guess); ad-blocker
    caveat.
26. `TAfFxdZqmLg` — Easy Tech, FaceOnLive detector demo — real-vs-ChatGPT
    image test; catfish-check use case.
27. `p5e9wTdAulA` — Common Sense Education, Google reverse-image tutorial —
    drag-drop / URL / right-click flows; critical-questions close.

## Iran company pointers (search results, portals NOT opened)

28. ilenc.ssaa.ir national legal-entity portal + Kateb migration notice +
    rrk.ir gazette — corroborated by 3 secondary guides (sabtshakhes,
    sabtebrand, sabtedadmehr) and 3 more (ashasabt, sabtenilgoon):
    search by name/registration/national-ID; LIKELY leads, verify live.

## GitHub discovery searches (2026-10-29, depth 1, ~3 results each)

Queries: OSINT framework; image verification forensics; fact-check
toolkit; awesome OSINT methodology; company registry due diligence;
deepfake/AI detection; scam/fraud checker; geolocation/shadow tools;
self-OSINT/footprint; domain/whois history. Notables: `edwardtay/awesome-OSINT`
(360+ tools), `ivbeg/awesome-forensicstools` (Bellingcat list source),
`zachisparanoid/lighthouse-osint` (ethics-gated graph platform),
`bytemallet/shadowtrace` (ShadowFinder method), `georevelo/georevelo`
(chronolocation claims — vendor hype, NOT VERIFIED),
`ruhanshaikh2577/ScamLens` (in-browser scam rules),
`frangelbarrera/OSINT-BIBLE` + `twtdata/OSINT-BIBLE` (2026 guides —
sock-puppet "buy aged accounts" advice REJECTED as ToS-breaking),
`AnshumanAtrey/domain-history-contact-osint` (pre-GDPR WHOIS ethics flag),
`0xnull-sec/osint-toolkit` (crt.sh/Wayback patterns),
`m-yusufuysal/delete`, `Codex-Crusader/digital-footprint-cleaner`
(self-only design praised), `dRafaleD/The-Trackher` (ETHICS.md).

## Failed / dead ends

- `bellingcat.com/category/guides/` → 404 (use /category/resources/).
- `sec.gov/edgar` → redirects to filing (submit) side; use /search-filings.
- `rrk.ir/` → fetch failed; `sid.ir` → JS shell (prior).
- `citizenevidence.amnestyusa.org/` (YouTube DataViewer) → fetch failed;
  concept kept via AJR citation, marked NOT VERIFIED open.
- `opencorporates.com/` → cookie wall, no content read.
- InVID site frozen ~2018 → current status NOT VERIFIED.

## Credits

Bellingcat, EJC Verification Handbook, Amnesty Evidence Lab, First Draft,
GIJN, Al Jazeera Media Institute, Poynter/PolitiFact, SEC, Companies
House, OFAC, EU Sanctions Map, ICANN, EFF, FTC, TinEye, FotoForensics,
Internet Archive, and the open-source OSINT community. Synthesis only; no
verbatim reuse beyond short attributed phrases.
