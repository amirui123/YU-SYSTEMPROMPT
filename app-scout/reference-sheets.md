# App Scout — Reference Sheets (v1.0)

Companion to `system-prompt.en.md` (`AppScout v1.0`). Freshness baseline: **2026-10-29**.
Full source list: `sources-and-credits.md`. Key: commands verified from official docs on 2026-10-29.

---

## Sheet 1 — GitHub search cheat sheet (qualifiers verified from GitHub Docs + topic pages)

### Repo discovery (github.com search bar, `github.com/search?q=…&type=repositories`)
```
<keywords> stars:>1000 pushed:>2026-01-01 language:TypeScript NOT is:archived
<keywords> topic:self-hosted license:mit stars:>500
<keywords> in:name,description,readme fork:false archived:false
"alternative to <App>" OR "<App> alternative" stars:>100
org:<org> <keywords>          # restrict to an org
```
- Sort: by stars for popularity, by recently-updated for maintenance. Always check both.
- `pushed:>` beats `created:>` for health. `good-first-issues:>1` / `help-wanted-issues:>1` signal live maintenance.
- License keywords: `license:mit`, `license:apache-2.0`, `license:gpl-3.0`, `license:agpl-3.0` (full keyword list: GitHub
  Docs "Licensing a repository").

### Code search (verified syntax page)
```
repo:OWNER/REPO <terms>            # full owner/repo required, no partial match
org:<org> OR user:<user>           # org/user scope (full names only)
language:python path:/src/**/*.py   # globs: * (one level), ** (nested), ? (one char)
content:<term>                     # content only, not paths
symbol:ClassName                   # definitions (Tree-sitter, 20 langs incl. py/js/go/rust/ts)
license:MIT  /  NOT is:fork  /  NOT is:archived  /  is:archived (for dead originals)
"exact phrase"  (AND/OR/NOT + parens)  /regex/    # boolean + regex supported
```

### Issues & discussions search (non-code syntax — different page from code search)
```
repo:OWNER/REPO is:issue is:open <symptom>        # known bugs before recommending
repo:OWNER/REPO is:issue label:security           # security track record
repo:OWNER/REPO is:discussion <topic>             # community Q&A, alternatives threads
```

### Topic pages & trending (verified live)
- `github.com/topics/<topic>` — e.g. `self-hosted` (50,551 repos, filter by language, sort by stars/updated/forks).
- `github.com/trending/<language>?since=daily|weekly|monthly` — spike check (see red flags: sudden stars, no history).
- awesome-lists: `sindresorhus/awesome` (index, 1,209 commits, updated Sep 2026) → category lists, e.g.
  `awesome-selfhosted/awesome-selfhosted` (331.6k★, updated Oct 27 2026, CC-BY-SA-3.0), `offa/android-foss`
  (1,286 commits, updated Oct 26 2026, requires minimum project age for entries).

### Playbook A — "Find the maintained fork of abandoned X"
1. Open original repo → confirm dead: last commit/release date, archived banner, pinned "unmaintained" issue, CI failing.
2. `/forks` → sort by stars / recently-pushed; also search `"<X>" fork stars:>50 pushed:>2025-01-01`.
3. Check `github.com/topics/fork` + web: `"<X>" "community fork" OR "maintained fork" OR "active fork"`.
4. Vet each candidate (Sheet 4): commits ahead of upstream, releases, issues answered, license file intact, scope sane.
5. Known-good patterns seen in research: org named `abandonware/*` hosts community continuations (e.g. `noble`);
   `Fomantic-UI` = official community fork of Semantic-UI; FileBrowser Quantum = maintained FileBrowser fork.
6. If none qualifies → say so, offer a different tool instead. Never crown a fork on stars alone.

### Playbook B — "Find alternatives to X"
1. Directories: OpenAlternative (`openalternative.co/<slug>`), AlternativeTo (`alternativeto.net/software/<slug>/`),
   awesome-list for the category, `"<X> alternative" site:github.com`.
2. Code/topics: `topic:<category>-alternative`, `"<X>-alternative" OR "<X> clone" stars:>200 pushed:>2025-06-01`.
3. Package managers (Sheet 3): `winget search`, `brew search`, `flatpak search`, F-Droid search, `apt search`.
4. Discussions: `site:reddit.com "<X> alternative"`, Hacker News search, GitHub Discussions on X's repo.
5. Cross-check every claim on ≥2 independent sources; crowdsourced ranks (AlternativeTo) ≠ verification.

---

## Sheet 2 — Trusted sources & directories

| Source | URL (opened 2026-10-29 unless noted) | Use for | Trust note |
|---|---|---|---|
| GitHub search / topics / trending | github.com/search · github.com/topics · github.com/trending | discovery, health signals | primary; verify each repo |
| awesome-selfhosted (canonical) | github.com/awesome-selfhosted/awesome-selfhosted | self-hostable software | 331.6k★, bot-updated daily |
| sindresorhus/awesome | github.com/sindresorhus/awesome | index of awesome-lists | entry point, not an endorsement |
| offa/android-foss | github.com/offa/android-foss | FOSS Android apps | active; min-age rule for entries |
| OpenAlternative | openalternative.co | proprietary→OSS mapping | curated; sponsored slots exist |
| AlternativeTo | alternativeto.net | crowdsourced alternatives (160k apps, 2M opinions) | votes ≠ vetting; check Official-Partner labels |
| winget-pkgs (manifests) | github.com/microsoft/winget-pkgs | Windows package existence/versions | reviewed PRs; manifests ≠ malware scan |
| formulae.brew.sh | formulae.brew.sh | brew formulae/casks metadata | human-reviewed core |
| F-Droid + Anti-Features | f-droid.org (+ /en/docs/Anti-Features/) | FOSS Android + behavior flags | strict inclusion policy |
| IzzyOnDroid | (video-cited; page NOT opened → verify) | faster F-Droid-compatible repo | community repo, own trust call |
| ArchWiki AUR | wiki.archlinux.org/title/Arch_User_Repository | AUR install method | AUR = UNVETTED by design |
| Flatpak docs / Flathub | docs.flatpak.org · flathub.org (latter not opened) | Linux sandboxed apps | check publisher verification on Flathub |
| npm docs (audit) | docs.npmjs.com | dep vuln scanning | `npm audit` / `npm audit fix` |
| PyPI guide | packaging.python.org | pip/venv install method | venv-first, never sudo pip |
| GHCR docs | docs.github.com (Container registry) | ghcr.io auth/pull | PAT or GITHUB_TOKEN |
| Modrinth | modrinth.com | Minecraft mods (open platform) | legit mod hub; still vet files |
| VS Marketplace docs | code.visualstudio.com (Extension Marketplace) | extension install/trust | publisher-trust dialog since 1.97 |
| GitHub Student Pack | education.github.com/pack | student freebies (Copilot, Azure…) | verify current offers per student |
| OSV.dev | (cited by security scanners; NOT opened → verify) | vuln/malware advisories (MAL-, GHSA-) | scanner-grade source |
| VirusTotal | (NOT opened → verify) | multi-engine file/URL scan | recommended pre-run scan step |

---

## Sheet 3 — Package-manager & install-command cheat sheet (per OS)

### Windows — winget (verified MS Learn + 3 transcripts)
```powershell
winget search <app>            # find; note exact Id
winget show <Id>               # publisher, license, installer URL, SHA256 <- VET THIS
winget install <Id>            # silent default; add --silent to suppress dialogs
winget upgrade / winget upgrade --all
winget list                    # installed (+ source column)
winget export -o apps.json / winget import -i apps.json   # machine templates
```
- Ships via App Installer (MS Store); needs Win10 1809+; first-login Store registration may lag (fix documented).
- Admin: prefer non-admin; only elevate for installers you trust. Unknown tools → Windows Sandbox first.
### Windows — others (commands standard; pages NOT opened → verify flags)
- Chocolatey: `choco install <pkg> -y` · Scoop: `scoop install <pkg>` · MS Store apps as fallback.
### macOS/Linux — Homebrew (verified brew.sh)
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install <formula> / brew install --cask <app>   # cask = GUI binaries
brew search / brew info / brew upgrade / brew bundle # Brewfile for repeatable setups
```
- Core formulae: human-reviewed, must be DFSG-compatible OSS. Taps = anyone's repo → read Tap-Trust before third-party
  taps; formulae/casks pin SHA-256. Check `formulae.brew.sh` for metadata + analytics.
### Linux — system + universal (Flatpak verified; apt/snap standard)
```bash
sudo apt update && sudo apt install <pkg>        # Debian/Ubuntu official repos first
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak search <app> && flatpak install flathub <com.Dev.App> && flatpak run <com.Dev.App>
flatpak update
snap install <pkg>                               # prefer strictly-confined, verified publishers
```
### Linux — AUR (verified ArchWiki; UNVETTED by design)
```bash
git clone https://aur.archlinux.org/<pkg>.git && cd <pkg>
less PKGBUILD            # MANDATORY: read build script for curl|sh, exfil, weird sources
makepkg -si              # builds + installs via pacman
```
- Follow aur-general list for incident warnings; AUR helpers are convenience, not vetting.
### Android — F-Droid (verified docs + transcript)
- Install client from f-droid.org → search → check permissions + Anti-Features (Tracking hidden by default) + versions
  tab → install; pull-to-refresh for updates. Nearby-share works offline. Extra repos (e.g. IzzyOnDroid): add URL in
  Settings → Repositories; each repo is a separate trust decision. Obtainium (seen on AlternativeTo) tracks upstream
  releases directly — verify per use.
### Developer registries
```bash
npm view <pkg> time,versions,dist-tags,repository,maintainers   # vet before install
npm install <pkg> && npm audit && npm audit fix                 # audit runs on install too
python3 -m venv env && source env/bin/activate && python3 -m pip install -U pip && pip install <pkg>
cargo add <crate> / cargo audit (audit tool NOT opened → verify)
docker pull ghcr.io/<owner>/<img>:<tag>   # pin tags/digests; public images pull anonymously
```

---

## Sheet 4 — Vetting checklist (score each axis 0–5; total → trust level)

1. **Provenance (is it real?)** official repo/site linked both ways (site↔repo)? owner org verified / long history?
   fork? of what, how far ahead? typosquat/lookalike check (name, URL, publisher id, npm scope, bundle id).
2. **Health** last commit + last release dates, cadence (releases/yr), contributors, open/closed issue ratio + median
   response time, archived? CI green? (signals from repo page, /releases, /issues, /graphs/contributors).
3. **License** exact SPDX from LICENSE file (link it): allows personal/commercial/modify/redistribute? copyleft scope?
   CLA? "free" ≠ OSS; "fair-code"/SSPL/BSL ≠ OSI-approved — say which. Never guess; quote + link.
4. **Security** SECURITY.md? signed releases/checksums (verify hash!)? `npm audit`/OSV/GHSA hits? install-script review
   (PKGBUILD, postinstall, curl|sh)? Android permissions vs function + F-Droid Anti-Features? telemetry documented?
   Pre-run: multi-engine scan (e.g. VirusTotal) + Sandbox/VM for anything below HIGH.
5. **Fit** platform, skill level, hardware/RAM, offline?, account required?, language/Persian-RTL?, import from X?
6. **Cost & sustainability** free/freemium/paid/donation; company-backed vs single maintainer (bus factor); pricing page
   opened? student/nonprofit/trial/official free tier?
- **Trust level:** HIGH (≥24, official + healthy + clean) · MEDIUM (16–23, usable with noted caveats) · LOW (8–15, only
  sandboxed/last resort, warnings bold) · **DO NOT USE** (<8 or any critical red flag: malware hit, dead + no fork,
  license forbids the use, impersonation confirmed).

---

## Sheet 5 — License cheat sheet (common cases; always link the project's LICENSE file)

| License | Use/modify/share | Commercial | Copyleft trigger | Note for Scout |
|---|---|---|---|---|
| MIT / BSD-2/3 / ISC / Apache-2.0 | yes | yes | none (Apache: patent grant) | safest recommendations |
| GPL-2.0/3.0 | yes | yes | distribute derivatives → same license | fine for users; flag for devs embedding |
| LGPL-2.1/3.0 | yes | yes | modifications to the lib itself | OK for dynamic linking |
| AGPL-3.0 | yes | yes | network use = distribution | self-hosting OK; SaaS-ifying triggers share |
| MPL-2.0 / EPL-2.0 | yes | yes | file-level | middle ground; note per-file scope |
| CC0 / Unlicense | yes | yes | none (public-domain-ish) | fine; not for code ideally |
| CC-BY / CC-BY-SA | yes | yes | SA = share-alike (for docs/media) | don't recommend NC/ND builds as "open" |
| SSPL / Elastic License / BSL | limited | restricted | source-available, NOT OSI open source | label "source-available", never "open-source" |
| "Fair-code" (e.g. n8n-style) | varies | varies | varies | open + read the actual license text |
| Freeware / "free for personal" | no modify/redist | no (usually) | n/a | NOT open-source; state limits |
| No license file | ALL RIGHTS RESERVED by default | no | n/a | DO NOT recommend code reuse; use-only if binary + trusted |

---

## Sheet 6 — Security red flags (any critical flag → DO NOT USE or sandbox-only)

**Critical:** multi-engine malware hit · confirmed typosquat/impersonation (name/URL/publisher/scope) · curl|sh or
obfuscated install script · postinstall exfil · secrets/keys in repo · removed README + mass file replace (hijack) ·
"free premium unlock / crack / keygen" bundling · asks for admin/root + phones home undocumented · Android permissions
absurd for function (SMS/contacts for a calculator) · F-Droid `KnownVuln`/`NoSourceSince` on the needed version.
**Suspicious (downgrade to LOW/MEDIUM + warn):** star spike with no history (check contributors/commits) · single
maintainer + no releases, only zips in repo · no SECURITY.md + ignored security issues · telemetry opt-out (not opt-in) ·
forced account for offline-able tool · download only from file-mirror, no checksums/signatures · fork with renamed
branding + added binary blobs · extension with huge permissions (VS Code exts run with full VS Code rights; check
publisher id + ratings + repo link) · mod file from random mirror instead of Modrinth/CurseForge/Workshop (verify author,
version history, comments).
**Hygiene rules:** prefer official site → repo → package manager, in that order; pin versions/digests for installs;
verify SHA-256/PGP where published; scan downloads multi-engine; sandbox/VM unknowns (Windows Sandbox documented path);
Android: F-Droid client + permission review; keep an "uninstall plan" for trials.
