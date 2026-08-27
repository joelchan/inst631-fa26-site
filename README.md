# INST631 — Fundamentals of Human-Computer Interaction

Public course site for INST631, Fall 2026, University of Maryland (Dr. Joel Chan).

Live at **https://joelchan.github.io/inst631-fa26-site/**

## This repo is generated output

`docs/` is not written by hand. It is staged from a private course repo by a
build script that copies only an explicit allowlist of pages — everything else
in that repo (planning notes, prior-year student work) is never eligible to be
published. Edit the source, not this repo; a hand edit here is overwritten on
the next rebuild.

Pushing to `main` builds the site with MkDocs Material and deploys it to GitHub
Pages via `.github/workflows/deploy.yml`.

## Rebuilding

From the `publish/` directory of the private source repo:

```sh
.venv/bin/python build.py && .venv/bin/mkdocs build
```

Then copy `mkdocs.yml` and `docs/` here and push.
