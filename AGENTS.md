# AGENTS.md

This file provides guidance to AI coding agents when working with code in this repository.

## Project Overview

Public documentation website for ReMAP (Remote Monitoring Application), a smartphone app for continuous assessment of affective symptoms in psychiatric research. Developed at the Institute for Translational Psychiatry, University of Münster. Built with MkDocs Material and deployed to GitHub Pages at https://wwu-remap.github.io.

**This site is public. Do not include implementation details, internal architecture, or study-specific data such as participant numbers or subgroup breakdowns.**

## Setup

Requires Python 3.x with `mkdocs-material`, which includes MkDocs.

```bash
pip install mkdocs-material
```

## Commands

```bash
mkdocs serve              # Local dev server with live reload
mkdocs build              # Build static site
mkdocs gh-deploy --force  # Build and deploy to GitHub Pages
```

GitHub Pages deployment is handled automatically by CI on push to `main` or `master`.

## Architecture

Documentation source lives in `docs/` as Markdown files with HTML for styled visuals. `mkdocs.yml` configures the site and enables Material theme extensions: admonitions, content tabs, superfences, and `md_in_html` for inline HTML blocks.

GitHub Actions (`.github/workflows/ci.yml`) automatically deploys on push to `main` or `master`.

## Commit Guidelines

- Do not add `Co-Authored-By` lines in commit messages.
