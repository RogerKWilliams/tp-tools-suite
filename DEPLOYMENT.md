# Deployment Runbook

This document captures the manual setup steps for getting the TP Tool Suite live
on the personal domain. Run these once; subsequent deploys are automatic via
GitHub push.

---

## Prerequisites

- Personal domain registered (you have one — just need DNS access)
- Vercel account (free tier is sufficient)
- All six GitHub repos pushed and public:
  - `tp-tools-suite` (landing page — this repo)
  - `crt-builder`
  - `ec-builder`
  - `frt-builder`
  - `prt-builder`
  - `tt-builder`

---

## Steps

### 1. Create Vercel projects

For each of the 6 repos, repeat:

1. Vercel dashboard → **Add New → Project**
2. Import from GitHub — select the repo
3. Framework auto-detects:
   - Vite tools (crt, ec, frt, prt, tt): Vercel detects "Vite" automatically — accept
   - Landing page (`tp-tools-suite`): select **"Other"** — it's a plain HTML/CSS site
4. Click **Deploy**

The first deploy creates a default `.vercel.app` URL (e.g. `crt-builder-xyz.vercel.app`).
Note each URL — you'll need them when filling in placeholders (Step 4).

### 2. Configure custom domains

Recommended domain pattern — **subdomains** (simplest, one Vercel project per tool):

| Subdomain              | Vercel project  |
|------------------------|-----------------|
| `tp.<domain>`          | tp-tools-suite  |
| `crt.tp.<domain>`      | crt-builder     |
| `ec.tp.<domain>`       | ec-builder      |
| `frt.tp.<domain>`      | frt-builder     |
| `prt.tp.<domain>`      | prt-builder     |
| `tt.tp.<domain>`       | tt-builder      |

In Vercel, for each project:

1. Project → **Settings → Domains → Add Domain**
2. Enter the subdomain (e.g. `crt.tp.yourdomain.com`)
3. Vercel shows the DNS records you need — keep this page open

### 3. DNS configuration

At your domain registrar, add a **CNAME record** for each subdomain:

```
crt.tp    CNAME    cname.vercel-dns.com.
ec.tp     CNAME    cname.vercel-dns.com.
frt.tp    CNAME    cname.vercel-dns.com.
prt.tp    CNAME    cname.vercel-dns.com.
tt.tp     CNAME    cname.vercel-dns.com.
tp        CNAME    cname.vercel-dns.com.
```

DNS propagation typically takes a few minutes to a few hours. Vercel's domain settings
page will show a green checkmark when the domain is verified and the SSL certificate
is issued (usually automatic within minutes of DNS resolving).

### 4. Fill in placeholder URLs

Once all domains resolve, update the placeholder URLs in source files, then commit and push.
Vercel auto-redeploys on push.

**`tp-tools-suite/index.html`** — replace these six placeholders with live tool URLs:

| Placeholder         | Replace with              |
|---------------------|---------------------------|
| `<CRT_TOOL_URL>`    | `https://crt.tp.<domain>` |
| `<CRT_GITHUB_URL>`  | GitHub URL for crt-builder |
| `<EC_TOOL_URL>`     | `https://ec.tp.<domain>`  |
| `<EC_GITHUB_URL>`   | GitHub URL for ec-builder  |
| `<FRT_TOOL_URL>`    | `https://frt.tp.<domain>` |
| `<FRT_GITHUB_URL>`  | GitHub URL for frt-builder |
| `<PRT_TOOL_URL>`    | `https://prt.tp.<domain>` |
| `<PRT_GITHUB_URL>`  | GitHub URL for prt-builder |
| `<TT_TOOL_URL>`     | `https://tt.tp.<domain>`  |
| `<TT_GITHUB_URL>`   | GitHub URL for tt-builder  |
| `<SUITE_GITHUB_URL>`| GitHub URL for tp-tools-suite |

**Each tool's `README.md`** — replace `<TOOL_URL>` and `<LANDING_PAGE_URL>`.

**Each tool's footer disclaimer** (in source) — replace any remaining GitHub URL
placeholders with the real URLs.

### 5. Smoke test live deploys

After URLs resolve and placeholder commits are pushed:

**Landing page (`tp.<domain>`):**
- [ ] Page loads and looks correct
- [ ] All five "Open tool" links resolve to the correct tool
- [ ] All four CLR prompt download links work (downloads `.md` files)
- [ ] Mobile view is readable (test at ~375px width)

**Each tool (`crt.tp.<domain>`, etc.):**
- [ ] Page loads, app is interactive
- [ ] Footer disclaimer is visible with correct links
- [ ] Export produces a JSON file with `"schemaVersion": 1`
- [ ] Import works (load the JSON you just exported)

**Cross-tool chain** (quick sanity check — full test documented in CP4):
- [ ] CRT export → FRT import: UDEs appear in FRT setup panel
- [ ] EC export → FRT import: injection appears in FRT
- [ ] FRT export → PRT import: injections appear as IO candidates
- [ ] PRT export → TT import: IOs appear as source references

### 6. Announce

Share the landing page URL (`https://tp.<domain>`) in the Commoncog forum thread
for the workshop series.

Timeline:
- Mention the suite is coming in **W1 (May 23)**
- Confirm it's live before **W2 (May 30)**

---

## Troubleshooting

**Domain not resolving after 30+ minutes:** Double-check the CNAME record at your
registrar — it's easy to miss the trailing dot on `cname.vercel-dns.com.` (some
registrars add it automatically; others don't).

**Vercel shows "Invalid configuration":** For `tp-tools-suite`, make sure the
framework is set to "Other" (not Vite). The site has no build step; Vercel serves
`index.html` directly.

**Tool import not working cross-browser:** The import uses the File System Access API
(with a `<input type="file">` fallback). If import fails on Safari, use the file-input
fallback by clicking the secondary import button.

**SSL certificate pending:** Vercel issues certificates automatically after DNS
resolves. If it stays pending more than 1 hour, go to Project → Settings → Domains
and click "Verify" to trigger a fresh check.
