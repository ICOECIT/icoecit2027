# ICoECIT 2027 — Conference Website

Static website for the **2nd International Conference on Emerging Computing & Intelligent Technologies (ICoECIT 2027)**, hosted by **G. Narayanamma Institute of Technology & Science (GNITS), Hyderabad**.

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
├── venue.html            # GNITS, Hyderabad + how to reach
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
3. Fill in confirmed **dates**, **fees** and the **submission-portal URL**
   (search the files for `TBA`, `Date TBA`, `to be announced`).

## 5. Content that is provisional / needs confirming

- **Dates & fees** — currently marked `TBA` (home, registration, venue).
- **Committee** — carried over from ICoECIT 2026; reconfirm names/roles for 2027.
- **Submission portal** — CMT/EDAS link to be added on the CFP page.
- **Secretariat email** — `icoecitconferencesecetary@gmail.com` (kept exactly as on the
  existing site; note the spelling “secetary”. Fix here and in all `mailto:` links if it
  should be `secretary`).

## 6. Preview locally

No build needed. From this folder:

```bash
# Python 3
python -m http.server 8080
# then open http://localhost:8080
```

or just double-click `index.html`.

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
