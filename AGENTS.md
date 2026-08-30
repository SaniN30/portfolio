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
- The WORKS tile canvas (js/canvas.js `paintWork`) only ever draws `<video>` elements - there is no
  image-tile code path. To put a photo in a tile slot, convert it to a short looping mp4 (e.g. an
  ffmpeg zoompan "Ken Burns" clip) rather than adding image support to canvas.js. Each tile needs a
  matching pair: a full-res file in assets/tiles/ and a smaller one in assets/tiles-sm/ (used on
  coarse/touch pointers, see canvas.js `COARSE`), same filename in both.
- assets/video/mark.mp4 (the intro "n*" mark) is a baked video, not canvas/DOM text - the glyph is
  a single static raster shape for the whole clip and only the asterisk animates around it (see the
  comment above `#mark` in index.html). To re-letter it: extract all frames, build a mask of
  pixels dark in nearly all frames (that isolates the static glyph from the moving asterisk),
  erase that mask, and darken-composite a freshly rendered letter image back in at the same
  position/size - this preserves the asterisk animation exactly since it's untouched pixels.
  Re-render assets/video/mark-still.webp (frame 0) from the same result; it's the poster image.

## Maintaining this file

Keep this file for knowledge useful to almost every future agent session in this project.
Do not repeat what the codebase already shows; point to the authoritative file or command instead.
Prefer rewriting or pruning existing entries over appending new ones.
When updating this file, preserve this bar for all agents and keep entries concise.
