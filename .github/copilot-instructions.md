---
applyTo: "**"
---

# Project Instructions

This repository is for a simple Astro website for a student-run ice popsicle stand.

## Product Goals

- Build a clean, responsive single-page or small multi-section Astro site.
- Use `donkey.png` as the logo image near the top of the page.
- Reserve a large hero area directly below the header for the logo.
- Include an intro paragraph section below the hero.
- Add a carousel or slider section farther down the page.
- One carousel slide must show `popsicle.jpg` with pricing text for `$0.5` and `$1 for 2 popsicles`.
- Another slide must provide a placeholder for a picture and 3-5 sentences describing the popsicle.
- The footer must include a placeholder area for team information.

## Astro Implementation Guidelines

- Prefer Astro components and layouts over framework-heavy solutions unless they are clearly needed.
- Keep the page simple, readable, and mobile-friendly.
- Use semantic HTML for header, main, section, and footer content.
- Keep styling focused on the school fair theme and the product photos.
- Treat `donkey.png` and `popsicle.jpg` as local static assets from the repository.
- If a carousel is implemented, choose the lightest reliable approach that keeps the page easy to maintain.

## Content And Editing Rules

- Preserve the existing content placeholders when possible so the owner can fill them in later.
- Do not invent brand facts, team details, or product claims that are not already provided.
- Use clear placeholder copy where the user is expected to add text later.
- Keep changes small and focused on the requested feature.

## Azure Deployment Guidelines

- Target Azure App Service for deployment unless the repository explicitly switches to a different Azure hosting model.
- Use GitHub Actions for CI/CD.
- Authenticate Azure deployments with a service principal only when that is the chosen org standard.
- Store Azure credentials as GitHub secrets or environment variables, never in source control.
- Prefer `azure/login` and `azure/webapps-deploy` in the workflow when deploying to Azure App Service.
- Use these secret names if they fit the workflow: `AZURE_CLIENT_ID`, `AZURE_TENANT_ID`, `AZURE_SUBSCRIPTION_ID`, and `AZURE_WEBAPP_PUBLISH_PROFILE` only if publish-profile deployment is intentionally chosen.
- If SPN authentication is used, the workflow must fail fast when any required secret is missing.
- Build the Astro site before deployment and deploy the compiled output only.

## Quality Bar

- Keep the site accessible, including alt text for images and sufficient color contrast.
- Ensure the layout works on desktop and mobile widths.
- Avoid unnecessary dependencies.
- Prefer straightforward code that a student team can maintain.