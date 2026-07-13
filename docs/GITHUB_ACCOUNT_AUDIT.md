# GitHub Account Audit

**Account:** `abdulrahman-517`
**Audit date:** 2026-07-13
**Repositories visible to the connected GitHub integration:** 2

## Executive Summary

The account currently contains a profile repository and one public software project. The profile repository has a strong starting structure, but it contains prohibited organization references, an incorrect location, and several publicly unverified skills. The `q-search` repository has comparatively strong documentation and no exposed secret was found in the inspected current files, but it lacks automated tests and CI, uses permissive CORS configuration, and needs a broader `.gitignore`.

The requested vehicle dealership, Vitamin C blog, Mowasalatna, Aqarnapro, and Haraj Al-Dhad source repositories are not present in the connected account. They can be presented as private-source portfolio work, but their source code, build state, dependency health, and secret exposure cannot be audited until they are uploaded or connected.

## Repository Classification

| Repository | Purpose | Main technology | Status | README quality | Build validation | Security findings | Classification | Recommended action |
|---|---|---|---|---|---|---|---|---|
| `abdulrahman-517/abdulrahman-517` | GitHub profile presentation | Markdown, image assets | Active | Medium; polished but inaccurate | Not applicable | No runtime secrets; profile text contains unwanted organization references and wrong location | Active profile repository | Replace README and banner with the prepared ice-inspired personal portfolio version |
| `abdulrahman-517/q-search` | Arabic-first YouTube search and ranking prototype | Python, FastAPI, HTML, CSS, JavaScript, optional Redis | Active prototype | Strong | Not executed; no CI/tests available | No secret found in inspected head files; permissive CORS and verbose upstream errors require later code hardening | Featured portfolio project | Keep public, improve metadata, remove unwanted organization reference, expand `.gitignore`, add tests/CI later |

## Security Review

### Inspected current files

- Profile `README.md`
- Previous profile banner asset
- Prepared replacement `assets/profile-banner.png`
- Prepared GitHub social preview `assets/social-preview.png`
- Q-Search `README.md`
- Q-Search `.gitignore`
- Q-Search `.env.example`
- Q-Search `config.py`
- Q-Search `main.py`
- Q-Search `requirements.txt`
- Q-Search `assets/q-search-banner.svg`

### Findings

1. No real YouTube API key was found in the inspected current files.
2. `.env` is ignored in `q-search`.
3. `.env.example` uses placeholder values.
4. The existing `.gitignore` is too narrow and should include environment variants, logs, caches, coverage, build output, and editor files.
5. `main.py` uses `allow_origins=["*"]` together with credentials. Production origins should be explicit.
6. Upstream exception text is returned to clients in some 502 responses. Production responses should avoid exposing internal error details.
7. A complete Git-history secret scan was not possible through the current read-only integration. Run Gitleaks or GitHub secret scanning before declaring the history clean.
8. The previously shared SSH private key from other work must never be committed to any repository. Rotate it if it was used beyond a temporary environment or exposed publicly.


## Prepared Ice Visual Identity

The refreshed profile package now uses a personal Arctic identity rather than the earlier teal-and-orange visual system.

### Palette

- Deep polar navy: `#02111F`
- Midnight ice: `#06263B`
- Glacier blue: `#0B3D5A`
- Arctic blue: `#2F91B7`
- Icy aqua: `#79DDEB`
- Frosted light: `#D7F6FF`
- Snow white: `#F8FDFF`

### Prepared assets

- `assets/profile-banner.png` — high-resolution 3:1 GitHub README banner
- `assets/social-preview.png` — 1280 × 640 GitHub repository social preview

The banner uses an iceberg, reflective ocean, and Arctic night sky as a restrained personal visual motif. It contains Abdulrahman Al-Mushajari’s personal identity only and no prohibited organization branding.


## Documentation Accuracy Findings

### Profile repository

- Remove all organization references requested by the account owner.
- Replace the incorrect previous location with Yemen.
- Remove or avoid C#, Docker, and other skills unless supported by connected code or explicitly documented work.
- Add the requested projects while labeling non-public source code truthfully.
- Do not invent direct demo links where none were verified.
- Keep the statistics section restrained and explain that it reflects public repositories only.

### Q-Search

- The README is already strong and product-oriented.
- `MAX_VIDEOS` is configured, but the current `/search` route uses a fixed candidate count of 15.
- Rate-limit variables exist in configuration, but no active rate-limiting middleware was found in the inspected `main.py`.
- The README should distinguish implemented functionality from configuration reserved for later implementation.
- The author section must not include the prohibited organization reference.

## Missing Repository Audit

The following projects are referenced by the owner but do not exist in the connected GitHub account:

- Al-Zandani Car Dealership
- Vitamin C Editorial Blog
- Mowasalatna
- Aqarnapro
- Haraj Al-Dhad
- Donut Store and any additional projects on the external portfolio

Recommended handling:

- Create public repositories only for projects safe to disclose.
- Keep production credentials, private customer data, deployment scripts, WhatsApp sessions, and infrastructure details private.
- For commercial projects, publish a sanitized showcase repository or documentation-only case study when the full code cannot be public.
- Never upload `.env`, database dumps, session folders, SSH keys, or customer assets without permission.

## Recommended Pinning Order

After the repositories are prepared and published:

1. Al-Zandani Car Dealership
2. Aqarnapro
3. Mowasalatna
4. Q-Search
5. Vitamin C Editorial Blog
6. Haraj Al-Dhad

At present, only `q-search` is suitable for pinning as a public software repository.

## Repository Metadata Recommendations

### Q-Search

**Description:**
`An Arabic-first YouTube search interface that re-ranks videos and playlists using documented content-quality signals.`

**Topics:**
`python`, `fastapi`, `youtube-api`, `arabic`, `rtl`, `search`, `nlp`, `redis`, `web-app`

**Website:**
`https://q-search-77si.onrender.com`

### Future projects

Use lower-case, descriptive names without `final`, `test`, or version suffixes:

- `al-zandani-dealership`
- `vitamin-c-blog`
- `mowasalatna`
- `aqarnapro`
- `haraj-al-dhad`

## Build and Link Validation

- Q-Search build was not executed because the connected GitHub integration is read-only and no authenticated local checkout was available.
- The Render demo URL appears in the repository documentation but was not independently validated in this environment.
- The supplied Netlify portfolio URL could not be fetched by the browsing environment; it is retained because it was explicitly provided by the owner.
- Mowasalatna is linked using the owner-provided production path.

## Destructive Actions

No repository was deleted, renamed, archived, privatized, or overwritten. No Git history was modified.
