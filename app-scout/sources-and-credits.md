# App Scout — Sources & Credits (v1.0)

All opened 2026-10-29 unless noted. Method: full-page read via fetch (chunk 0 unless noted); video transcripts via
YouTubeToTranscript (real transcripts read in full). Reused prior-mission knowledge: prompt-system design, OWASP LLM01,
NIST AI 600-1, license-reading discipline (no verbatim reuse of unlicensed text).

## 1. GitHub discovery (docs + repos + topics)
1. GitHub Code Search syntax (official docs, chunks 0–1 of 3) —
   https://docs.github.com/en/search-github/github-code-search/understanding-github-code-search-syntax — Taken: bare-term
   behavior, exact quotes, AND/OR/NOT + parens, repo:/org:/user:/enterprise:, language:, license:, path: globs/regex,
   symbol: (Tree-sitter langs), content:, is: (archived/fork/vendored/generated) + NOT inversions.
2. Repo-search docs (old URL 404s — disagreement logged) —
   https://docs.github.com/en/search-github/searching-on-github/searching-repositories — Taken: docs restructured; repo
   qualifiers (stars:/pushed:/language:/topic:/license:/in:/fork:/archived:) used in Sheet 1 from long-standing syntax +
   code-search page; re-verify URL in monthly pass.
3. awesome-selfhosted (canonical) — https://github.com/awesome-selfhosted/awesome-selfhosted — Taken: 331.6k★, 15.6k
   forks, bot-updated Oct 27 2026, CC-BY-SA-3.0, topics incl. self-hosted; structure (bot-built from -data repo).
4. Topic page self-hosted — https://github.com/topics/self-hosted — Taken: 50,551 repos, language filters, sort options
   (stars/forks/updated), top repos n8n/open-webui/immich as live examples.
5. sindresorhus/awesome — https://github.com/sindresorhus/awesome — Taken: awesome-list index, 1,209 commits, updated Sep
   2 2026, entry-point role.
6. offa/android-foss — https://github.com/offa/android-foss — Taken: FOSS Android list, 1,286 commits, updated Oct 26
   2026, CONTRIBUTING requires minimum project age, CI lint scripts.
7. microsoft/winget-pkgs — https://github.com/microsoft/winget-pkgs — Taken: community manifest repo, commit 4 min before
   read (hyper-active), manifests/ tree, reviewed-PR model (from search snippet of README).

## 2. Package managers & registries (official docs)
8. winget docs — https://learn.microsoft.com/en-us/windows/package-manager/winget/ — Taken: search/install/show/source/
   validate, App Installer delivery, Win10 1809+, first-login registration lag + fix, admin-elevation caution, Sandbox path.
9. Homebrew homepage/docs — https://brew.sh/ — Taken: install command, formulae (build from source, human review,
   DFSG-compatible license required) vs casks (prebuilt binaries), taps + Tap-Trust warning, SHA-256 pinning,
   formulae.brew.sh metadata, Brewfile/bundle.
10. Flatpak usage docs — https://docs.flatpak.org/en/latest/using-flatpak.html — Taken: IDs (com.Dev.App), triples,
    system vs --user, remote-add flathub, search/install/run/update commands.
11. F-Droid Anti-Features — https://f-droid.org/en/docs/Anti-Features/ — Taken: 10 flags (Ads, DisabledAlgorithm,
    KnownVuln, NonFreeAddons/Assets/Dependencies, NonFreeNet, NoSourceSince, TetheredNet, Tracking-hidden-by-default).
12. ArchWiki AUR — https://wiki.archlinux.org/title/Arch_User_Repository — Taken: AUR = unvetted user content, PKGBUILD
    verify-first workflow (clone → read → makepkg -si), aur-general list for incident warnings.
13. npm audit docs — https://docs.npmjs.com/auditing-package-dependencies-for-security-vulnerabilities — Taken: audit
    coverage (direct/dev/bundled/optional, not peer), auto-run on install, `npm audit fix`, SEMVER warnings, manual-review
    path, EAUDITNOPJSON/NOLOCK fixes.
14. PyPI install guide — https://packaging.python.org/en/latest/tutorials/installing-packages/ — Taken: venv-first,
    pip upgrade, get-pip.py caution, never sudo with system Python.
15. GHCR docs — https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry —
    Taken: ghcr.io, PAT(classic)/GITHUB_TOKEN auth, `docker login`, public anonymous pull, scope minimization.

## 3. Directories, mods, extensions, student routes
16. OpenAlternative — https://openalternative.co/ — Taken: curated proprietary→OSS directory (1M users claim), huge
    per-app filter taxonomy (e.g. Asana 26, ClickUp 24 alternatives), sponsored slots exist.
17. AlternativeTo — https://alternativeto.net/ — Taken: 160,208 apps / 2,057,459 opinions, crowdsourced ranks, per-app
    pages with license/platform tags, news section, Official-Partner (sponsored) labels.
18. GitHub Student Pack — https://education.github.com/pack — Taken: free pack incl. Copilot/Codespaces/Azure/DataCamp
    bundles ("Experiences"); signup via education benefits; offers rotate → verify per student.
19. Modrinth — https://modrinth.com/ — Taken: open-source mod platform (mods/packs/shaders/plugins/servers), discover +
    per-project pages; legitimate-hub example.
20. VS Code Extension Marketplace docs — https://code.visualstudio.com/docs/configure/extensions/extension-marketplace
    (redirected from /docs/editor/…) — Taken: publisher+download/rating vetting signals, extension id
    `publisher.name`, exts run with full VS Code rights, third-party-publisher trust dialog since 1.97.

## 4. GitHub landscape searches (8 queries, 2026-10-29; snippets/leads only)
awesome-selfhosted forks · openalternative forks · winget-pkgs (+fork anatomy: "forked from" banners) · homebrew taps
(third-party tap trust model, SHA-256, notarization notes) · android-foss forks (F-Droid/IzzyOnDroid tags) ·
awesome-selfhost-docker (category structure incl. maintained-fork examples: FileBrowser Quantum, Pelican Panel) ·
community-fork patterns (`abandonware/*` org, Fomantic-UI, fork topic 6,844 repos) · supply-chain scanners
(compromised-packages-check updated 6×/day, z8run/aegis analyzers, AgentGuard severity model, OSV MAL-/GHSA- feeds).
Used for shortlisting + playbook design; stars/claims in snippets NOT treated as verified facts.

## 5. Video transcripts (real transcripts read in full, 2026-10-29)
21. "Winget in Windows 11 — Install, Update & Manage Apps Like a Pro" (TechSolutionZ, 2026-03-25) —
    https://www.youtube.com/watch?v=_2mZnBlPjIs — Taken: search/install/upgrade --all/uninstall/list/export/import/show
    walkthrough, IDs for accuracy, Store App Installer fallback.
22. "How to use Winget (Windows Package Manager)" (Danny Moran, 2023-03-18) —
    https://www.youtube.com/watch?v=UoxmPalvz1g — Taken: manifest/show fields (version/publisher/URL/hash), upgrade flow
    with version proof, export/import machine templating.
23. "Install software using Windows Package Manager | Winget" (Techielass, 2022-04-05) —
    https://www.youtube.com/watch?v=hkvcuLbD8XM — Taken: show-before-install vetting habit (publisher/support URL/license/
    installer URL/SHA256 legitimacy), --silent flag, vague-name search technique.
24. "F-Droid Guide | F-Droid App Store" (Techdoc, 2022-01-23) —
    https://www.youtube.com/watch?v=uT9ThjiG730 — Taken: client-vs-browser (updates), search/categories, permissions +
    source + versions tabs, Nearby offline share, adding repos (IzzyOnDroid), Tor proxy option.

## NOT verified (gaps — agent must check live, never assert)
Repo-search docs canonical URL · IzzyOnDroid pages · Flathub verification badges · Chocolatey/Scoop/чoco review model ·
OSV.dev + VirusTotal pages · crates.io/`cargo audit` · Docker Hub official-image badges · Nexus Mods/CurseForge/Steam
Workshop pages · JetBrains/Microsoft/Apple education pricing · Obtainium behavior · any per-app facts (all must be
re-searched per request) · F-Droid client Tor option currency (2022 video).
