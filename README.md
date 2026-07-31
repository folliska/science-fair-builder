Hosting the Science Fair Project Builder on GitHub Pages

This is one self-contained HTML file — no server, no API key, no student accounts, nothing to install. It runs entirely in the browser.

Steps
Create a new GitHub repo (or reuse the one you use for your other sims), e.g. science-fair-builder.
Add science-fair-advisor.html to the repo. Rename it to index.html if you want it at the repo's root URL, or keep the name and link to it directly.
In the repo: Settings → Pages → Source → Deploy from a branch → main (root) → Save.
GitHub gives you a URL like: https://yourusername.github.io/science-fair-builder/ (or .../science-fair-advisor.html if you kept the original filename).
Share that link with students — works on Chromebooks, tablets, and phones, no login required.
Editing later

Everything a student sees — topics, starter questions, safety checklist text — lives in two JS objects near the top of the <script> section: STRANDS (topics/ideas per science strand) and SAFETY_ITEMS (the safety checklist). You can edit the text directly in those objects without touching any of the layout/logic code below them.

This version is tailored to your actual rules

The topic bank and eligibility checklist are now built from the SY26-27 ISEF International Rules, the 2026-27 SSEF of Florida Rules Supplement, and the Collier Regional Science & Engineering Fair Rule Book. Some things worth knowing:

Junior Division hard bans: at Collier, projects involving human participants (even self-testing), vertebrate animals, or potentially-hazardous biological agents/tissue cannot compete at CRSEF — so those topic types were removed from the starter idea bank entirely, and the eligibility checklist screens for them if a student builds a custom idea instead.
Allowed exceptions: baker's/brewer's yeast fermentation and bread-mold-with-immediate-disposal are specifically called out as OK.
Pre-approval-required categories (hazardous chemicals rated 2+, controlled substances, firearms, explosives, radiation, lasers, drones, power tools, archeology, and any non-standard use of school grounds) are flagged with a note to talk to the teacher — Collier's process for these can take over a month and forms are due no later than October 9, 2026.
The summary card also reminds students of Collier-specific requirements that are easy to miss: 5+ trials per group, a dated ink data notebook, a 5-source APA bibliography, and display-day rules (no glass, liquids, food, sharps, or visible brand names).

If your rule books update next year, the easiest path is to re-upload the new PDFs/docx here and ask me to refresh the STRANDS and SAFETY_ITEMS objects to match — the rest of the tool (layout, flow, print/download) won't need to change.

No data is stored or sent anywhere

This tool doesn't save anything to a server or database — a student's answers exist only in their browser tab while they're using it, and disappear when they close it (unless they click Print or Download, which saves locally to their own device). There's nothing for you to manage or moderate on the backend.
