# UEM Jaipur Research & Innovation

[![Static Site](https://img.shields.io/badge/Type-Static%20Website-0ea5e9?style=for-the-badge)](https://uem-jaipur-research.uem.edu.in)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38BDF8?style=for-the-badge&logo=tailwindcss)](https://tailwindcss.com)
[![Firebase Hosting](https://img.shields.io/badge/Firebase-Hosting-DD2C00?style=for-the-badge&logo=firebase)](https://firebase.google.com/products/hosting)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=for-the-badge&logo=githubactions)](https://github.com/features/actions)

A modern research landing page for UEM Jaipur that presents the university's innovation ecosystem, high-impact thematic research clusters, infrastructure, publications, and collaboration opportunities.

## Purpose

This website was created to establish a polished digital presence for the university's research and innovation portfolio. It communicates the institution's interdisciplinary focus across AI, engineering, health sciences, sustainability, and Indic knowledge systems, while helping visitors understand:

- the breadth of research themes and clusters
- institutional strengths and infrastructure
- collaboration and funding opportunities
- the university's innovation and research identity

The site is designed for researchers, academic partners, industry collaborators, students, and funding stakeholders who want an overview of UEM Jaipur's research ecosystem.

## Website overview

The page is a single-page, responsive marketing site with the following sections:

- Hero banner and institutional positioning
- Research performance metrics
- Thematic research clusters (16 areas)
- Infrastructure and high-tech instrumentation highlights
- Research impact and collaboration messaging
- Calls to action for partnership and proposal discussions

## Stack

This project is a static front-end website built with:

- HTML5
- Tailwind CSS via CDN
- Google Fonts
- Lucide icons
- Firebase Hosting for deployment
- GitHub Actions for automated deployment

## Project structure

```text
.
├── index.html              # Main landing page content and styling
├── 404.html                # Firebase-friendly 404 page
├── logo.webp               # Brand logo asset
├── favicon.ico             # Browser icon
├── apple-touch-icon.png    # Apple touch icon
├── android-chrome-*.png    # Android app icons
├── site.webmanifest        # PWA manifest
├── CNAME                   # Custom domain configuration
├── firebase.json           # Firebase Hosting config
├── .firebaserc             # Firebase project target
├── .github/workflows/      # Deployment automation
├── .gitignore              # Ignore rules for local setup
└── README.md               # Project documentation
```

## Deployment details

The site is deployed on Firebase Hosting.

### Firebase configuration

- Project target: `uem-jaipur-research-groups`
- Hosting public directory: `.`
- Custom domain: `https://uem-jaipur-research.uem.edu.in`

Configured files:

- `firebase.json`
- `.firebaserc`
- `CNAME`

### Hosting configuration

The hosting setup uses the root directory as the public deployment target and ignores local files such as Firebase config and dependencies. This is suitable for a static HTML website without a framework build step.

### CI/CD workflow

The repository includes automated deployment workflows under `.github/workflows/`:

1. `deploy-prod.yml`
   - Trigger: push to `main`
   - Deploys to the Firebase live channel

2. `deploy-preview.yml`
   - Trigger: pull request events
   - Deploys a preview channel that expires after 30 days

This means the website is automatically deployed to production on the main branch and to preview URLs for pull requests.

## Local development

Because this is a static site, you can preview it using any simple web server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Firebase deployment commands

If you need to deploy manually from the Firebase CLI:

```bash
firebase login
firebase use uem-jaipur-research-groups
firebase deploy --only hosting
```

## Notes

- No framework build step is required.
- The site is intentionally lightweight and optimized for fast static hosting.
- The design focuses on a premium academic research brand identity and clear community engagement messaging.

## Live site

- Production: https://uem-jaipur-research.uem.edu.in
