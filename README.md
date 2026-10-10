# DishaSetu — Branch-Aware Career & Skills Roadmaps

DishaSetu is a responsive, static learning-planning prototype built with HTML, CSS and vanilla JavaScript. It can be hosted on GitHub Pages without a build step.

## What's included in this build

- **Branch selection during onboarding and profile editing** for CSE, CSE (AI/ML), IT, AI & Data Science, ECE, EEE, Mechanical, Civil, Chemical, Biotechnology, Biomedical, Aerospace, Automobile, Agricultural, Mining, Industrial/Production, Environmental and Other/Custom.
- **Branch-aware Skills Portal and Roadmap Explorer.** The default view recommends domain-relevant skills and roles. Students can switch to all skills/roles at any time; branch selection guides recommendations but does not restrict careers.
- **Expanded catalogue:** 48 career roles and 64 skills/practice paths, including dedicated paths for embedded systems, electronics fundamentals, VLSI, power systems, mechanical CAD/CAE, thermodynamics, robotics, manufacturing quality, civil CAD/BIM, structural engineering, chemical process engineering, biotechnology, biomedical instrumentation, aerospace, automotive/EVs, agricultural engineering, mining, environmental engineering and operations research.
- **Detailed five-phase learning roadmaps** with vertically scrollable curriculum details, connected curved milestone overview on larger screens, phase navigation and a responsive vertical timeline on smaller screens. New engineering curricula have five curated phases, with topics, prerequisites, effort estimates, practice, projects, completion criteria and learning resources.
- **Per-topic states:** Pending, In Progress, Done and Skipped. Done counts toward completed progress; skipped items remain visibly distinct and do not count as completed. Status changes can be reversed and are saved locally per roadmap.
- **Topic-specific resources:** relevant Apna College YouTube searches, GeeksforGeeks article searches and W3Schools tutorials where applicable. Engineering-domain paths point to engineering video searches and NPTEL's course catalogue, with GeeksforGeeks where relevant. Search links are labeled honestly; the app does not fabricate individual video IDs.
- **Branch-aware career plan:** year-wise foundations, domain skills, labs/practical work, specialization, project evidence, internships and career-readiness planning adapt to the selected branch. A student's target career can still be outside their branch.
- **Other workspace tools:** personalized dashboard, projects, internship-source and application tracking, resume studio, job-description keyword analysis, activity view, guided mentor, resource library, settings and local data backup.
- **Premium visual design:** charcoal, warm ivory and gold styling, interactive states, responsive layouts and reduced-motion support.

## Run locally

1. Extract the ZIP.
2. Open the folder in VS Code.
3. Start Live Server from `index.html`, or open the HTML file in a browser.
4. Create a demo account and complete onboarding. Choose an engineering branch and target career.
5. Open **Skills Portal** or **Roadmap Explorer**. Use the branch selector to change recommendations; choose **All skills** or **All roadmaps** to explore beyond your branch.
6. Open a roadmap, select a phase, expand topic groups and test Start / Done / Skip. Refresh and use browser Back/Forward to check route and progress persistence.

No npm packages or build command are needed. Google Fonts are loaded from Google Fonts when internet access is available; system fallbacks are included.

## Resource-link behavior

Apna College links open a YouTube search scoped to the current skill and topic. GeeksforGeeks links search its articles. W3Schools links are included only where a tutorial is applicable. Engineering-domain resources include topic-specific engineering lecture searches and the NPTEL course catalogue. Where a specific video or article has not been verified, the app labels the destination as a search rather than implying it is a verified individual resource. Review links when aligning the learning plan to a course syllabus.

## Deploy to GitHub Pages

1. Create a GitHub repository.
2. Upload `index.html`, `style.css`, `script.js`, `README.md`, and `.nojekyll` to the repository root.
3. Open **Settings → Pages**.
4. Select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Wait for the Pages workflow and open the published URL.

## Important production limitations

This is a deployable **static prototype**, not a production-authenticated SaaS app. Sign-in and profile/progress data use local browser storage; they do not provide secure identity verification, cross-device synchronization or multi-user isolation. The mentor uses guided/rule-based responses and is not connected to a live AI model. Internship shortcuts open external sources; the prototype does not provide a verified live vacancy feed. Before production, connect secure authentication and a backend/database (for example Supabase or Firebase), enforce server-side authorization, protect API keys, and integrate lawful live opportunity sources.

Branch roadmaps are structured study plans, not official university syllabi, licensure requirements or placement guarantees. Specific subjects, lab hours, certifications and industry requirements vary by university, country and specialization. Map each roadmap to the student's actual curriculum and verify important details against primary course documentation and current role requirements.
