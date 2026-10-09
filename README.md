# PathForge AI — Complete Static MVP

A polished, responsive student career-planning app built with **HTML, CSS and vanilla JavaScript**. It is intentionally static so it can be deployed directly to GitHub Pages without a build step.

## Included features

- **Persistent demo session:** create a local demo account or sign in, then refresh the browser without returning to login. The active hash route is preserved.
- **Real browser navigation:** pages use URL hash routes; browser Back/Forward and mobile browser navigation move between previous routes.
- **Onboarding and profile:** degree/branch, college, BTech year, graduation year, target role, existing skills, study time and learning preference.
- **Dashboard:** personal focus, progress metrics, recommended next action, learning activity and shortcuts.
- **Roadmap explorer:** role-, skill- and practice-based catalogue, search/filter, four-stage roadmaps, responsive SVG journey, per-topic checklists, stage deliverables and text export.
- **Four-year career plan:** year-by-year themes, milestone suggestions and persistent review checklists.
- **Project lab:** starter project briefs, stack/features/outcomes, status tracking and custom project entries.
- **Internship finder:** links to current third-party job sources plus a locally stored application tracker. It does not invent or claim live openings.
- **Resume studio:** profile-prefilled fields, editable live preview, three starter styles and browser Print → Save as PDF. Resume statements remain user-controlled; no invented achievements.
- **Skill-gap analyzer:** local keyword comparison of a pasted job description with profile skills, completed topics and tracked projects. It is not a hiring score.
- **Guided mentor:** contextual starter answers for common planning questions. It is a rule-based prototype, not a connected LLM.
- **Resource library:** official docs and reputable learning/practice sites.
- **Learning activity:** local learning-action history, contribution-style heatmap and streak calculation. Logins alone do not count as learning.
- **Settings and backup:** JSON export/import, profile editor, local sign-out and clear-data flow.
- Mobile navigation, responsive layout, empty states, confirmations, accessible labels, and reduced-motion support.

## Run locally

1. Extract the ZIP.
2. Open `index.html` directly, or open the folder in VS Code and use **Live Server**.
3. Create a demo account and complete onboarding.

No package installation or build command is required. Google Fonts are loaded from their hosted service when internet access is available; system font fallbacks are included.

## Deploy to GitHub Pages

1. Create a new **public or private GitHub repository** (choose the visibility you prefer).
2. Upload the files from this folder to the repository root: `index.html`, `style.css`, `script.js`, `README.md`, and `.nojekyll`.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select your `main` branch and `/(root)`, then save.
6. Wait for GitHub Pages to finish publishing and open the URL it provides.

This is a static single-page app. Its hash routes (for example, `/#roadmaps`) work without configuring server rewrites.

## Important production limitations

This is a functional **front-end MVP**, not a finished multi-user SaaS backend. The core UI interactions and local persistence are implemented, but the following require server-side services and credentials before treating the app as production-ready:

- **Authentication and cross-device sync:** sign-in is a lightweight local demo session. It does not verify credentials, support a genuine Google OAuth flow, or securely separate users on a shared device. Connect Supabase Auth or Firebase Auth and use per-user database authorization before public use with personal data.
- **Persistent cloud storage:** profile, progress, activity, projects, resume draft, chat and application tracking use this browser's `localStorage`. Data will not automatically sync to another device or browser and can be lost if browser storage is cleared. Use a database with user-scoped policies for production.
- **Live AI mentor:** the current mentor uses guided, rule-based responses. A genuine model needs a backend API that keeps its key secret, validates structured outputs, applies rate limits and handles errors safely. Never place an AI provider key in `script.js` or a public repo.
- **Live internship matching:** job sources open at their providers. The app does not scrape third-party pages or claim their current listings as its own. Automatic matching requires permitted APIs or other lawful access, freshness checks and source citations.
- **Resource accuracy:** resources are reference starting points. Verify course availability, job eligibility, deadlines, technologies and requirements at the original source.
- **PDF export:** resumes are exported through the browser's Print dialog. Select “Save as PDF” and inspect the resulting document for page breaks, links and text overflow.

## Data backup

Use **Settings → Export my data** to download a JSON backup. Importing a valid backup replaces local PathForge app data after confirmation. Treat backups as personal data and store them securely.

## Validation notes

- JavaScript syntax was checked with Node.js (`node --check script.js`).
- The page is dependency-free and routes are driven by the URL hash.
- This environment blocked browser automation navigation, so a full interactive browser test could not be completed here. Run through sign-in, refresh, Back/Forward, topic completion, resume PDF preview and backup/restore in your target browser before public launch.

## Suggested next step for production

Add a Supabase/Firebase backend (auth + database + row-level authorization), then connect the mentor and any permitted internship APIs through server-side endpoints. Keep secrets in server environment variables, never in the GitHub Pages bundle.
