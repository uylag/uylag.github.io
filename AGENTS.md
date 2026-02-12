# Repository Guidelines

## Project Structure & Module Organization
This repository is a lightweight static site.
- `index.html`: placeholder root entry page.
- `hitorilink/index.html`: HitoriLink landing/description page.
- `hitorilink/policy/index.html`: privacy policy page (Russian).
- `hitorilink/policy/policy.css`: policy-specific stylesheet.

Keep page-specific assets close to the page that uses them (for example, `hitorilink/policy/`).

## Build, Test, and Development Commands
No build pipeline is required; files are served as static HTML/CSS.
- `python3 -m http.server 8000`: run a local static server from repo root.
- `xdg-open http://localhost:8000/hitorilink/policy/` (Linux): open the policy page.
- `rg --files`: quick inventory of tracked source files.

If you add tooling (formatter/linter/test runner), document commands here and keep them reproducible from repo root.

## Coding Style & Naming Conventions
- Use 4 spaces for HTML/CSS indentation, matching current files.
- Prefer semantic HTML (`section`, `h1`-`h2`, `p`, `ul/li`) and keep heading hierarchy logical.
- Use lowercase, descriptive file names (`policy.css`, `index.html`).
- Keep CSS readable and grouped by selector type; avoid one-off inline styles unless necessary.
- Preserve existing language/content conventions (Russian legal text in policy pages).

## Testing Guidelines
There is no automated test suite yet. Use manual checks before opening a PR:
- Verify pages load from the local server with no missing assets.
- Check layout on desktop and mobile widths (browser responsive mode is enough).
- Validate links, especially email/contact links and policy references.
- Re-open changed pages in a clean tab to catch caching/path errors.

## Commit & Pull Request Guidelines
Based on existing history, use short imperative commit subjects:
- `Add policy`
- `Moved to hitorilink`

PRs should include:
- A brief summary of changed files and why.
- Screenshots for visual/layout changes.
- Manual test notes (which URLs were checked).
- Linked issue/ticket when applicable.

## Additional
Ignore all .md files in .gitignore
