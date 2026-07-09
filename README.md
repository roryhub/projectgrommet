# projectgrommet.com

The AI-readable home of **Project Grommet** — a Human–AI collaboration framework for long-form projects. Created by Rory O'Connor; supported by Hub Games.

The site is deliberately plain: its first reader is an AI, not a person. Structure:

- `llms.txt` — entry manifest for AI readers (what to read, in what order)
- `primer.md` — the framework's universal layer, current version (canonical copy lives in the private AI Collaboration folder; this is the published mirror)
- `primer-v1.1.md` — pinned, immutable copy of v1.1
- `project-context-template.md` — the per-project layer, copied into each user's project
- `index.html` — minimal human-facing holding page
- `.nojekyll` — serves the .md files as plain text rather than rendering them
- `CNAME` / `robots.txt` — domain + explicit permission for AI fetchers

Publishing protocol: the primer changes only in the private folder first (changelog → header → filename → this mirror, in one move, with Rory present). Every public change is therefore traceable both here (git history) and there (changelog).

Licence: CC BY-NC-SA 4.0 (provisional).
