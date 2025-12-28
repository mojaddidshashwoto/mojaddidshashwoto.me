# Mojaddid Shashwoto — Portfolio

This repository contains a production-ready single-page portfolio for Mojaddid Shashwoto.  
The site is intentionally minimal, professional and performance-focused — suitable for creative professionals, business planners, and consultants.

Contents
- `index.html` — complete single-page site with internal CSS and markup (ready to edit).
- `.github/workflows/pages.yml` — GitHub Actions workflow to automatically deploy the repository root to GitHub Pages on push to `main`.
- `README.md` — this file.

Quick start (web UI)
1. Open the repository on GitHub.
2. Click **Add file → Create new file** and create or update the files:
   - `index.html` — paste the provided HTML.
   - `.github/workflows/pages.yml` — paste the workflow if not present.
   - `README.md` — this file.
3. Commit to the `main` branch. If the repo is empty, the first commit creates `main`.
4. Visit the Actions tab to watch the Pages workflow run. After success, check Settings → Pages for the published URL.

Quick start (local)
1. Clone the repo:
   ```
   git clone git@github.com:mojaddidshashwoto/mojaddidshashwoto.me.git
   cd mojaddidshashwoto.me
   ```
2. Create `main` if needed and add files; then:
   ```
   git add index.html .github/workflows/pages.yml README.md
   git commit -m "Add portfolio site and Pages workflow"
   git push -u origin main
   ```
3. Preview locally (optional):
   ```
   python -m http.server 8000
   # then open http://localhost:8000 in your browser
   ```

What to edit (key areas)
- Hero / Header
  - Update the name, subtitle and CTA labels inside `index.html`.
  - Elements to edit:
    - Hero heading (h1 with id `hero-heading`)
    - Subtitle paragraph(s) directly below the heading
    - Primary and secondary CTA hrefs (`href="#projects"`, `href="#contact"`) if you want to link to external pages or anchors.

- Avatar / Photo
  - Replace the avatar image by updating the `src` attribute of the image inside the `.avatar` element:
    ```html
    <img src="https://avatars.githubusercontent.com/u/251911880?v=4" alt="Mojaddid Shashwoto">
    ```
  - Recommended: host high-resolution photos in an `assets/` folder (e.g., `assets/avatar.jpg`) and use optimized JPEG/WEBP for performance.

- About section
  - Edit the copy inside the About card (the section with `id="about-heading"`). Keep paragraphs concise and outcome-focused.

- Skills
  - Edit `.skill-pill` blocks to reflect the skills you want to highlight. Keep labels short and supporting text one line.

- Projects
  - Replace placeholder project cards in the Projects grid with real projects.
  - For each project card update:
    - `.project-title` — short, descriptive title
    - `.project-desc` — one-sentence impact/summary (focus on outcome & stack)
    - `.project-meta` — concise tech/role info
    - Buttons — replace `href="#"` with the project page or GitHub link

- Contact
  - Update email, LinkedIn, and GitHub links in the Contact card.
  - Ensure emails use `mailto:` format and external links include `target="_blank" rel="noopener"`.

SEO & Social (meta tags)
- Edit the `<title>`, `<meta name="description">`, and Open Graph / Twitter meta tags at the top of `index.html` to reflect updated copy and imagery (OG image should be a proper social-sized image).
- Example:
  ```html
  <meta property="og:title" content="Mojaddid Shashwoto — Photographer & Creative Consultant">
  <meta property="og:description" content="Strategic visual storytelling and disciplined business planning.">
  <meta property="og:image" content="https://example.com/og-image.jpg">
  ```

Favicon
- The page includes a small SVG data-URI favicon by default. Replace with your own `favicon.ico` or `favicon-32x32.png` in the repo root and update the `<link rel="icon">` tag if desired.

Design & accessibility notes
- Typography: the site uses Inter (Google Fonts). You may substitute Poppins or system fonts by updating the `<link>` and `--font-sans`.
- Color palette: neutral base with one accent color (`--accent`). Change the accent color in the `:root` CSS variables if needed.
- Buttons include focus outlines and reduced-motion support for better accessibility.
- All interactive links include meaningful text and ARIA where appropriate.

Deployment details
- The workflow `.github/workflows/pages.yml` uses the official GitHub Pages Actions to upload and deploy the repository root.
- Once files are pushed to `main`, the Actions run automatically and Pages deployment is performed.
- For a custom domain:
  - Add a `CNAME` file at the repository root containing your domain (e.g., `mojaddidshashwoto.me`).
  - Configure DNS:
    - For apex domain (example.com) add A records to:
      - 185.199.108.153
      - 185.199.109.153
      - 185.199.110.153
      - 185.199.111.153
    - For `www` subdomain, add a CNAME pointing to `YOUR_GH_USERNAME.github.io`.
  - After DNS propagation, enable "Enforce HTTPS" in Settings → Pages.

Testing & troubleshooting
- If Actions fails:
  - Open the failed run in Actions → view logs for the step that failed (checkout / upload / deploy).
  - Common issues: syntax errors in workflow, temporary GitHub service issues, or permission restrictions in organization settings.
  - Share step logs if you need help — paste the full error message.

- If Pages is not published:
  - Wait 2–10 minutes after a successful workflow run for the Pages deployment and certificate issuance.
  - Confirm the workflow run completed successfully (all green).
  - Check Settings → Pages for the URL and HTTPS status.

Best practices & tips
- Keep project descriptions outcome-focused: what you shipped and measurable results (percent improvements, conversion, revenue impact).
- Use production images and optimized assets. Avoid embedding large images inline.
- Keep the hero concise and value-driven — visitors decide quickly whether to continue.

Support & next steps
- If you want, I can:
  - Populate the Projects section with real entries if you provide project titles, short descriptions, and links.
  - Generate a professional OG image or simple favicon for branding.
  - Help debug workflow or Pages deployment issues — paste logs and I will assist.

License
- This repository contains your portfolio files. Add a LICENSE file if you want to clarify reuse or distribution.

---

If you want the README adjusted with examples of exact lines to change in `index.html` or a checklist for a recruiter-ready launch (images, OG image, resume link), tell me which items to include and I will update this file.
