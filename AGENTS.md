# Project agent memory

This file is the project's committed home for project-intrinsic agent knowledge: build, test, release, architecture, and sharp-edge notes that should travel with the code.

- Add durable project-specific notes here as they are discovered through real work.
- This is not a resume-style personal portfolio template despite the "portfolio" name: it's an
  interactive 3D-intro reel experience (mark video -> WebGL iPod/camera scene -> a video-tile
  "work" canvas) built around director-reel footage. See index.html, js/main.js, js/scene.js.
  User-editable content slots are limited to: page title/meta (index.html head), the about/contact
  page copy and CTA links (index.html #pageAbout/#pageContact, reusing .page__p/.page__cta), and
  the WORKS array in js/data.js (video src + optional label, label is currently unused/unrendered
  in canvas.js). There is no structural place for resume sections (experience, education, skills,
  certifications) without adding new UI - fold that kind of content into the about page's prose
  instead of inventing new sections.

## Maintaining this file

Keep this file for knowledge useful to almost every future agent session in this project.
Do not repeat what the codebase already shows; point to the authoritative file or command instead.
Prefer rewriting or pruning existing entries over appending new ones.
When updating this file, preserve this bar for all agents and keep entries concise.
