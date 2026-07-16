# ICoECIT 2027 — Conference Website

Static website for the **2nd International Conference on Emerging Computing & Intelligent Technologies (ICoECIT 2027)**, organized by **G. Narayanamma Institute of Technology & Science (GNITS), Hyderabad**. Tentative venue: **Taj City Centre, Patna, Bihar**.

Built to replace/refresh the previous Google Sites site for the new edition. Pure HTML + CSS — no build step, no frameworks — so it drops straight onto GitHub Pages.

> ⚠️ **Important status:** The application for ICoECIT 2027 is **currently UNDER REVIEW with the publisher (IEEE) and is NOT yet approved.** Every page carries a persistent status banner saying so. Do **not** remove that banner, add the IEEE logo, or claim IEEE sponsorship until formal approval and a signed agreement are in place (see *IEEE compliance* below).

---

## 1. Site structure

```
ICOECIT 2027/
├── index.html            # Home — hero, about, themes, focus areas, dates
├── call-for-papers.html  # Tracks, topics, submission guidelines
├── committee.html        # Organizing committee (provisional, from 2026)
├── registration.html     # Indicative fees + registration terms
├── venue.html            # Taj City Centre, Patna (tentative) + how to reach
├── history.html          # Past editions — 2026 links to IEEE Xplore
├── contact.html          # Secretariat contact
├── privacy.html          # Privacy Policy
├── terms.html            # Terms & Conditions
├── refund-policy.html    # Refund & Cancellation Policy
├── 404.html              # Not-found page
├── robots.txt
├── .nojekyll             # tell GitHub Pages to serve files as-is
└── assets/
    ├── css/style.css     # single shared stylesheet
    └── img/
        ├── logo.svg      # full horizontal logo (mark + wordmark)
        ├── logo-mark.svg # emblem only (used in header)
        └── favicon.svg   # browser/tab icon
```

All internal links are **relative**, so the site works whether it is served from an
org root (`https://<org>.github.io/`) or a project subpath (`https://<org>.github.io/<repo>/`).

## 2. The logo

A custom SVG aligned to the conference title:

- A **microchip** outline (with pins) = *Computing / Electronics*.
- Inside it, a **rising neural-node network** = *Emerging* + *Intelligent Technologies*.
- Gradient **blue → cyan → violet** = research, technology, innovation.

Deliberately **does not** include the IEEE logo (not permitted before approval).
Edit the SVGs directly to tweak colours/wording, or swap in an official mark later.

## 3. Candidate themes for 2027

Shown on the home page for the committee to pick from. Recommended lead theme first:

1. **★ “Intelligent Horizons: Computing for a Connected Tomorrow”** *(recommended)*
2. “Emerging Frontiers: Where Intelligence Meets Innovation”
3. “Convergence of Minds & Machines”
4. “Computing Beyond Boundaries: AI for a Sustainable Future”
5. “Next-Gen Intelligence: From Edge to Everywhere”
6. “Smart Systems, Smarter Society”

## 4. IEEE compliance notes (please read)

Based on IEEE conference-organizer guidance, until the conference is formally approved
and the agreement/MOU is signed:

- **No IEEE logo** anywhere on the site, publications or promotions.
- **Do not imply an IEEE relationship** or guarantee IEEE Xplore indexing.
- **Name the financial sponsor** (GNITS) clearly — done on every page.
- Keep the **“under review — not yet approved”** banner visible everywhere.

Once approval + a signed agreement arrive:

1. Update the red status banner text (or remove it) on **every** page.
2. Add the IEEE / IEEE-section logo where permitted, with the correct
   “Technically Co-Sponsored by …” wording.
3. Confirm **dates** (currently mirroring 2026), add **fees** (search for `TBA`), and
   activate the conference-specific **Microsoft CMT** submission link on the CFP page.

## 5. Content that is provisional / needs confirming

- **Dates** — set to mirror the ICoECIT 2026 timeline: Submission **30 Oct 2026**,
  Acceptance **1 Dec 2026**, Camera-ready & registration **10 Dec 2026**,
  Conference **28–29 Jan 2027**. Shown as indicative pending approval.
- **Fees** — set from the official fee sheet (`fEES.xlsx`): Indian categories ₹8,000–₹16,000,
  non-Indian authors $200, extra pages ₹500/₹800 per page, certificates ₹500/₹800. Shown as
  subject to confirmation pending approval. Registration only via the payment-gateway link in
  the acceptance email; papers only via Microsoft CMT.
- **Committee** — carried over from ICoECIT 2026; reconfirm names/roles for 2027.
- **Submission portal** — **Microsoft CMT** (`cmt3.research.microsoft.com`). The
  conference-specific CMT submission link is to be activated on approval.
- **Secretariat email** — `icoecitconferencesecetary@gmail.com`, kept exactly as on the
  existing site **per organiser instruction** (do not change the spelling).

## 6. Preview locally

No build needed. From this folder:

```bash
# Python 3
python -m http.server 8080
# then open http://localhost:8080
```

or just double-click `index.html`.

## 6b. SEO

Every page includes: an optimized `<title>` and meta description, conference/IEEE-relevant
`keywords`, a `canonical` URL, Open Graph + Twitter Card tags (share image at
`assets/img/og-image.png`, 1200×630), and JSON-LD structured data — an `Event` (+ `Organization`,
`WebSite`) on the home page and `BreadcrumbList` on inner pages. `sitemap.xml` and `robots.txt`
(with a `Sitemap:` line) are at the root; `404.html` is `noindex`. Keywords stay truthful and do
**not** claim IEEE sponsorship (the "under review" status is preserved everywhere).

After launch: submit `sitemap.xml` in **Google Search Console** and **Bing Webmaster Tools**, and
regenerate the OG image with `assets/img/` if branding changes.

## 7. Deploy to GitHub Pages (org: icoecitconferencesecretary)

Intended to live under the GitHub account/organisation **`icoecitconferencesecretary`**.

```bash
git init
git add .
git commit -m "ICoECIT 2027 website (under-review edition)"
git branch -M main
# create the repo under the org, e.g. using the GitHub CLI:
gh repo create icoecitconferencesecretary/icoecit-2027 --public --source=. --remote=origin --push
```

Then in the repo: **Settings → Pages → Build and deployment → Source: “Deploy from a branch” → `main` / `/ (root)`**.

- Project-page URL: `https://icoecitconferencesecretary.github.io/icoecit-2027/`
- For a root org-page instead, name the repo `icoecitconferencesecretary.github.io`.
- To use a custom domain (e.g. `icoecit.org`), add a `CNAME` file containing the domain
  and set the DNS records per GitHub Pages docs.

---

© ICoECIT 2027 · G. Narayanamma Institute of Technology & Science. Website content is
provisional pending publisher approval.
