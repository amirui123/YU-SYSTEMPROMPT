# Deep Scout — Sources & Credits

> All web sources accessed 2026-10-29 unless noted. "Opened" = page content
> read via fetch. Snippet-only items are marked as such.

## Search infrastructure (opened)

1. Google Search Help — search operators
   `https://support.google.com/websearch/answer/2466433` — quotes, `site:`,
   `-`, `before:`/`after:`, `filetype:`, no-space-after-colon. `intitle:` /
   `inurl:` absent → UNVERIFIED.
2. SearXNG docs — search syntax
   `https://docs.searxng.org/user/search-syntax.html` — `!bang` chaining,
   `:lang`, `!!` external bangs with trust warnings.
3. HN Search API — `https://hn.algolia.com/api` — `/search` vs
   `/search_by_date`, tags, numericFilters, pagination, 10K req/hr/IP.
4. Stack Overflow Help — searching
   `https://stackoverflow.com/help/searching` (chunk 0 of 2) — tags,
   `title:`/`body:`/`code:`, ranges, `created:`, booleans, `or`.
5. arXiv API manual — `https://info.arxiv.org/help/api/user-manual`
   (chunk 0 of 7) — `export.arxiv.org/api/query?search_query=`, AND logic,
   Atom 1.0.
6. OpenAlex docs — `https://docs.openalex.org` → redirected to
   `https://help.openalex.org` — Quickstart/How-to/API reference,
   per-page `.md` + `llms.txt` agent pattern.
7. Hugging Face Papers trending — `https://huggingface.co/papers/trending`
   — reached via live redirect from `https://www.paperswithcode.com`
   (PWC as independent site: NOT VERIFIED live; HF Papers is its observed
   successor).

## Method & credibility (opened)

8. PRISMA statement — `https://www.prisma-statement.org/` — PRISMA 2020
    checklist, flow diagram, statement papers (doi:10.1136/bmj.n71/n160).
9. IFCN Code of Principles — `https://www.ifcncodeofprinciples.poynter.org/`
    — transparency/nonpartisanship commitments for fact-checkers.
10. CRAAP test (Wikipedia) — `https://en.wikipedia.org/wiki/CRAAP_test`
    (chunk 0 of 3) — Blakeslee/CSU Chico 2004; Meola "Chucking the
    Checklist" critique; Caulfield SIFT alternative; Esparrago-Kalidas 2021
    (Authority/Purpose hardest).
11. Triangulation, social science (Wikipedia)
    `https://en.wikipedia.org/wiki/Triangulation_(social_science)` — Denzin
    4 types: data / investigator / theory / methodological.
12. Grounded theory (Wikipedia) — `https://en.wikipedia.org/wiki/Grounded_theory`
    (chunk 0 of 11) — Glaser & Strauss, constant comparative method,
    emergence basis for saturation stop rule. Note: standalone
    `Theoretical_saturation` article does NOT exist (verified missing page).
13. Decision-matrix method (Wikipedia)
    `https://en.wikipedia.org/wiki/Decision-matrix_method` — Pugh 1981,
    reference candidate, weighted variant, disadvantages (arbitrary
    criteria, must-have outvoting, false precision).
14. Connected Papers — `https://www.connectedpapers.com/` — visual graphs,
    prior/derivative views, built on Semantic Scholar corpus.
15. Semantic Scholar API — `https://www.semanticscholar.org/product/api`
    (chunk 0 of 2) — Academic Graph/Recommendations/Datasets, 214M papers,
    2.49B citations, key rate limits.
16. Crossref REST API
    `https://www.crossref.org/documentation/retrieve-metadata/rest-api/`
    (chunks 0–1) — `api.crossref.org` endpoints, polite pool `mailto=`,
    no-signup, JSON.
17. NIST AI RMF — `https://www.nist.gov/itl/ai-risk-management-framework`
    (chunk 0 of 2) — AI RMF 1.0 (2023-01-26), voluntary, Playbook/Roadmap,
    GenAI Profile 600-1 (2024-07-26).

## Security (opened)

18. OWASP GenAI — LLM01:2025 Prompt Injection
    `https://genai.owasp.org/llmrisk/llm01-prompt-injection/` (chunk 0 of 2)
    — direct/indirect injection, 9 attack scenarios, 7 mitigations
    (constrain behavior, validate output, filter I/O, least privilege,
    human approval, segregate external content, adversarial testing);
    RAG/fine-tuning do not cure it.

## Reference agent architectures (opened, chunk 0 unless noted)

19. `assafelovic/gpt-researcher` (canonical; 3,219 commits; latest
    2026-10-10) — planner + execution agents, Jev decision models, multi-agent
    workflows, recursive deep research, `evals/`.
20. `stanford-oval/storm` — STORM paper arXiv:2402.14207; outline →
    multi-perspective Q&A → retrieval → cited report; Co-STORM (EMNLP 2024).
21. `EleutherAI/lm-evaluation-harness` (chunk 13 of 14; 14.3K★, 3.7K forks)
    — task-implementation priority list (community agreement → official
    impl → evaluator agreement → preferred common), MIT license.

## Persian sources

22. Magiran — `https://www.magiran.com/` (opened, Persian) — est. 1380,
    3,500+ journals, 160K volumes, 2.5M+ full texts; personal/org annual
    subscription for full text; newspapers since 1385.
23. SID.ir — `https://www.sid.ir/` — access returned only a JS redirect
    shell ("در حال انتقال…"); content UNVERIFIED.

## Video transcripts read (4)

24. `BQ49tAJOqIQ` — All Things Academia, "How to Do a Systematic
    Literature Review (Step-by-Step + Free PRISMA Template)" — 6 steps,
    PICO/SPIDER, boolean strategy, doc-everything, PRISMA diagram,
    extraction table, synthesis (not summaries).
25. `qsrXJGpxwIE` — Vanderbilt Libraries, "Using SIFT to Evaluate Sources
    for Credibility" — full SIFT walkthrough, lateral reading, knowledge
    panel, newspaper-of-record, telephone game.
26. `eL8zL5-MIb0` — Teaching in Higher Ed, "Using Caulfield's SIFT… Nurses"
    (chunks 0–1 of 3) — live SIFT demo: Stop, broaden-over-narrowed search,
    Wikipedia + Ad Fontes for source check, trace to original scholarship.
27. `SHNprb2hgzU` — Digital Inquiry Group (ex-SHEG), "Sort Fact from
    Fiction Online with Lateral Reading" — checkers vs Stanford students/
    professors study (100% vs 40% link rate), `.org` open domain, checklist
    critique.

## GitHub discovery searches (2026-10-29, depth 1, ~3 results each —

disclosed, not padded to 10)

Queries: `site:github.com deep research agent`, `awesome fact-checking
OSINT`, `systematic review tools PRISMA`, `source credibility scoring`,
`prompt injection guardrails`, `fake stars detection github`,
`benchmarking LLM evaluation`, `query expansion search`, `awesome
evidence synthesis`, `papers with code alternatives`. Notable snippet
finds: `searxng/searxng` (38.9K★, AGPL-3.0, updated Oct 2026),
`gpt-researcher` forks analyses, `awesome-ai-research-tools` variants,
`evidencesynthesis-tools/awesome-evidence-synthesis` (ASReview, GROBID,
LatteReview), `darrshangovender/guardrail` (4 detectors incl. bidi-char),
`royalpinto007/awesome-llm-guardrails` (Llama Guard, Prompt Guard, Rebuff,
Vigil), `mancano-tales` OSINT, `brycewang-stanford` lit-review table
format, `stn1slv/StarAudit` + `masteryoda101/fake_star_check`
(star-burst = human-review flag), `leoncuhk`/`x-tahosin` LLM-benchmark
lists (model names UNVERIFIED), SMU SIFT PDF (CC-BY 4.0, snippet only).

## Failed / dead ends (do not retry without cause)

- `docs.github.com/…/searching-repositories` → 404 (GitHub restructured
  docs paths).
- `en.wikipedia.org/wiki/Theoretical_saturation` → no such article.
- `www.sid.ir/` → JS redirect shell, no readable content.
- YouTube direct/advanced chunks → 401/player shells; working route is
  `youtubetotranscript.com/transcript?v=ID`.

## Credits

Method foundations: PRISMA 2020 (Page et al.), CRAAP (Blakeslee, CSU
Chico), SIFT + lateral reading (Caulfield; SHEG/Digital Inquiry Group),
triangulation (Denzin), theoretical saturation (Glaser & Strauss), Pugh
matrices (Stuart Pugh), OWASP GenAI Security Project, NIST AI RMF,
STORM (Stanford OVAL), GPT-Researcher community, EleutherAI eval harness.
This prompt synthesizes; it does not copy any source verbatim beyond
short attributed phrases.
