# notex-devops

A compact DevOps utility/demo project and learning sandbox. This repository contains a minimal static site (`index.html`) and supporting guidance so you can experiment with CI/CD, static-site deployment, and small automation examples.

## Table of contents

- [Project overview](#project-overview)
- [Quick demo / preview](#quick-demo--preview)
- [Prerequisites](#prerequisites)
- [Install & run (local)](#install--run-local)
- [Recommended workflow](#recommended-workflow)
- [Project structure](#project-structure)
- [Contributing](#contributing)
- [Troubleshooting](#troubleshooting)
- [Roadmap](#roadmap)
- [License & contact](#license--contact)

## Project overview

`notex-devops` is intentionally small so it can be used as:

- A sandbox for learning CI/CD (GitHub Actions, GitLab CI, etc.)
- A demo for static site deployment (GitHub Pages, Netlify, S3 + CloudFront)
- A base to add automation (linters, tests, deploy scripts)

The repository currently contains a single static HTML page (`index.html`) and this README. You can expand it with scripts, CI config, and deployment workflows as needed.

## Quick demo / preview

To preview the site locally (no build step required), run a lightweight HTTP server from the repository root.

On macOS with Python 3:

```bash
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

You can also open `index.html` directly in a browser for a one-off check.

## Prerequisites

- Python 3 (for the built-in static server) or Node.js (optional)
- Git to clone and manage the repository

Optional (for future automation):

- Node.js + npm (for build tools)
- Docker (for containerized previews)
- Deploy CLIs (Netlify, AWS CLI, etc.)

## Install & run (local)

1. Clone the repository:

```bash
git clone https://github.com/devonepao/notex-devops.git
cd notex-devops
```

2. Serve the site locally:

```bash
python3 -m http.server 8000
```

Visit http://localhost:8000 in your browser.

3. (Optional) Serve with Node's `http-server`:

```bash
npm install -g http-server
http-server -p 8000
```

## Recommended workflow

1. Create a branch for your work: `git checkout -b feat/your-change`
2. Make changes to `index.html` or add assets
3. Add linting or formatting tools (HTMLHint, markdownlint)
4. Add CI checks that validate on push/pull request
5. Merge to `main` and deploy to your chosen host

## Project structure

```
index.html        # main static file / demo page
README.md         # this file
```

When you expand the repo, consider these folders:

- `.github/workflows/` — CI config
- `ci/` — helper scripts
- `docs/` — documentation

## Contributing

Contributions are welcome. Please:

1. Fork the repo
2. Create a branch with a descriptive name
3. Open a PR and describe what you changed and why

Small, useful contributions:

- Add a simple CI workflow example
- Add a `Makefile` with common tasks (serve, lint)
- Add a `LICENSE` (MIT recommended)

## Troubleshooting

- If the server won't start, ensure the selected port is free or choose another port (e.g., `python3 -m http.server 9000`).
- If browser shows stale content, try a hard refresh (Cmd+Shift+R) or clear cache.

## Roadmap

Suggestions to increase value:

- Add CI workflow templates (GitHub Actions/GitLab CI)
- Add a GitHub Pages or Netlify deploy action
- Add a Dockerfile for containerized testing
- Add linters and basic tests if adding scripts

## License & contact

This project does not include a license file yet. Add a `LICENSE` (for example MIT) if you want to allow reuse.

For help or to collaborate, open an issue or submit a PR.

---

If you want, I can also add a GitHub Actions workflow example, a `Makefile`, or a `LICENSE` file—tell me which and I'll implement it.
