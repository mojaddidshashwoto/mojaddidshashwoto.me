```markdown
# Mojaddid Shashwoto — Portfolio

This repository contains a single-file, responsive portfolio for Mojaddid Shashwoto.

How to use

- Edit `index.html` to update the content: About, Skills, Projects, and Contact links.
- All styling is included inside `index.html` within a `<style>` tag for quick edits.
- Replace the avatar image URL with your preferred image or host it in the repository under `assets/` and update the `src` attribute.

Deploying

- The repository includes a GitHub Actions workflow that automatically publishes the site to GitHub Pages from the `main` branch when you push.
- After pushing, go to the repository Settings → Pages to confirm the site is published (the workflow creates the Pages deployment).

Customization tips

- Projects: replace the placeholder project titles, descriptions, and the "View Code" / "Live Demo" links with actual URLs.
- Contact: LinkedIn and email are already set to your values; change if needed.
- Fonts: the site uses Inter via Google Fonts; replace or remove as desired.

Quick start — GitHub web UI

1. In your repository on GitHub: click "Add file" → "Create new file".
2. Create `index.html`: paste the full content above and commit to `main`. (If the repo is empty, committing will create the branch.)
3. Create the workflow file at `.github/workflows/pages.yml` and commit.
4. Create `README.md` and commit.
5. After the workflow runs, check Settings → Pages for the published URL.

Quick start — local git

1. Clone the repo:
   - git clone git@github.com:mojaddidshashwoto/mojaddidshashwoto.me.git
   - cd mojaddidshashwoto.me
2. Create and switch to `main` (if not present):
   - git checkout -b main
3. Add files (paste contents into files), then:
   - git add index.html .github/workflows/pages.yml README.md
   - git commit -m "Add portfolio site and Pages workflow"
   - git push -u origin main

Notes

- The workflow deploys the repository root as the Pages site. If you prefer a different publishing source, update the workflow and/or repository Pages settings.
- If you want, I can add real project links (GitHub repo URLs) into the Projects section — provide the links and I will produce the updated index.html you can paste or I can push for you.
```
