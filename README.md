# Service Offering Catalog

A static documentation site for service offerings, published with GitHub Pages.
The initial content is a working draft adapted from the supplied IT consulting
services portfolio. It describes capabilities for scoping, not a record of
completed engagements.

## Structure

- `docs/index.md`: catalog homepage.
- `docs/services/index.md`: service listing.
- `docs/services/*.md`: the 13 service areas.
- `docs/services/automation/*.md`: 14 focused PowerShell automation topics.
- `docs/engagements.md`: engagement models and automation deliverables.
- `docs/priorities.md`: the starting draft's client engagement priorities.
- `docs/_config.yml`: Jekyll site settings and theme.
- `content-source/IT-Consulting-Services.md`: unchanged source draft for reference;
  outside the GitHub Pages publishing folder.

GitHub Pages builds the Markdown in `docs/` into HTML using Jekyll.

## Publish to GitHub Pages

1. Create a GitHub repository and push this repository's `main` branch to it.
2. In the GitHub repository, open **Settings → Pages**.
3. Set **Source** to **Deploy from a branch**.
4. Select **main** and **/docs**, then save.
5. Open the published URL shown in the Pages settings after deployment completes.

Changes pushed to `main` automatically update the site. GitHub Pages must be
available for the repository's visibility and account plan. Treat content in
`docs/` as public unless restricted site access has been explicitly configured.

## Add a service

Create a Markdown file such as `docs/services/example-service.md`:

```markdown
---
title: Example Service
---

# Example Service

Add the service description here.

[Back to services](./)
```

Add a link to it in `docs/services/index.md`:

```markdown
- [Example Service](example-service.html)
```

Use relative links to generated `.html` pages so navigation works under the
repository's GitHub Pages URL. PDFs and images can be added inside `docs/` and
linked by their filenames. Navigation links are maintained manually.

## Content maintenance

Edit the pages in `docs/` directly. The source draft is an archive, not a build
input; changes to it do not regenerate the website. Keep each page's `title`
front matter and relative navigation links when editing.

Preserve the scope notes on the identity-security and licensing pages. In
particular, the draft positions MIM PAM and ESAE/Red Forest as specialist
capabilities for existing environments, not default new-deployment designs.
Pricing, delivery timelines, and claims of completed projects have not been
added. Review the draft before publishing for external distribution.

The catalog contains 31 Markdown pages. No local Ruby/Jekyll runtime was
available during the initial content build; the GitHub Pages deployment remains
the authoritative Jekyll build check.

## Reference

[GitHub Pages documentation](https://docs.github.com/en/pages)
