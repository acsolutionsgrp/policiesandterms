# policiesandterms.com

Centralized SMS policy hosting for One I.T. Pro managed clients.  
Each client gets a subdomain: `clientname.policiesandterms.com`

---

## Live Client Pages

| Client | Privacy Policy | Terms & Conditions |
|--------|---------------|-------------------|
| Crescent Home Health Care | `crescenthomehealthcare.policiesandterms.com/privacy-policy` | `crescenthomehealthcare.policiesandterms.com/terms` |

---

## Folder Structure

```
/
├── index.html                          ← Root landing page
├── _redirects                          ← Cloudflare redirect rules
├── crescenthomehealthcare/
│   ├── privacy-policy/
│   │   └── index.html
│   └── terms/
│       └── index.html
└── [nextclient]/
    ├── privacy-policy/
    │   └── index.html
    └── terms/
        └── index.html
```

---

## Adding a New Client

1. Copy the `crescenthomehealthcare/` folder
2. Rename it to the new client's slug (e.g., `careforsoul`)
3. Find & replace all instances of "Crescent Home Health Care" and "crescenthomehealthcare.com"
4. Update the Last Updated date
5. Push to GitHub — Cloudflare Pages deploys automatically
6. Add a wildcard CNAME in Cloudflare DNS (already set up if using `*.policiesandterms.com`)

---

## Cloudflare Setup

### DNS
- Type: `CNAME`
- Name: `*` (wildcard)
- Target: Your Cloudflare Pages project URL (e.g., `policiesandterms.pages.dev`)
- Proxy: ON (orange cloud)

### Pages Project Settings
- Build command: *(leave empty)*
- Build output directory: `/`
- Root directory: `/`

---

## Managed by
**One I.T. Pro**  
support@oneitpro.com  
oneitpro.com
