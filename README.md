# Fahad Badsha Shamim — Plant Science Research Portfolio

A static GitHub Pages portfolio with a browser-based admin dashboard. The site is designed for academic/research audiences and separates the public portfolio from the dashboard editing workflow.

## Public pages

- `index.html` — Home, About, selected research, publications, experience, skills, education and contact
- `research.html` — Research project index
- `research-detail.html?slug=...` — Individual research project pages
- `publications.html` — Selected publications with authentic publication/DOI/PDF resources
- `skills.html` — Skill categories
- `skill-detail.html?skill=...` — Dedicated detail page for each skill
- `experience.html` — Professional experience
- `admin/` — Dashboard

## Content editing

The dashboard can update JSON content through the GitHub Contents API. It includes:

- Research project editor with dedicated detail pages, publication metadata and PDF/external links
- Linked skill categories and individual skill-detail pages
- Media Library for reusable images
- Appearance controls for colours, gradients, typography and scientific background opacity
- Navigation controls
- English, German, Bangla, Spanish and Italian interface translations
- My Profile
- CV Manager with PDF upload, editable DOCX source, profile metadata and reusable cover letter
- Security guidance for fine-grained GitHub tokens and browser sessions

## GitHub Pages

Upload the repository contents to the root of the target repository and enable GitHub Pages from the repository's `main` branch and `/ (root)` folder.

Keep `.nojekyll` in the repository root.

## Dashboard security model

This is a static GitHub Pages dashboard. It does **not** provide server-side authentication. The GitHub token is held in `sessionStorage` only and is never written into repository files. Use a fine-grained token restricted to this repository with the minimum Contents permission required for editing, use a short expiry, and revoke it when finished. Do not use the dashboard from a shared or untrusted computer.

## Research-source policy

Publication metadata and resource links were checked against journal/publisher or indexed publication records where available. The muskmelon entry is explicitly presented as an unpublished exploratory student field trial; missing soil, coordinate, treatment and measurement details are not invented.

## Privacy

Do not store passwords, banking information, identity numbers or other secrets in this repository. Professional contact information may be public by design. The dashboard's My Profile data file is part of the repository, so treat any information placed there as potentially accessible to repository visitors.


### Public-header privacy
The public portfolio header does not expose the admin dashboard, dashboard URL, profile menu, Settings, or CV Manager. The admin remains a separate `/admin/` route and is not linked from the public site.
