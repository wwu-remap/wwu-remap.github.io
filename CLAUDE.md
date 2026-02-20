# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ReMAP documentation website for WWU (University of Munster). Built with MkDocs and the Material theme, deployed to GitHub Pages at https://wwu-remap.github.io.

## Commands

- `mkdocs serve` — Local dev server with live reload
- `mkdocs build` — Build static site
- `mkdocs gh-deploy --force` — Build and deploy to GitHub Pages (handled automatically by CI on push to main/master)

## Architecture

Documentation source lives in `docs/` as Markdown files. `mkdocs.yml` configures the site (name, theme, navigation). GitHub Actions (`.github/workflows/ci.yml`) automatically deploys on push to main/master by installing `mkdocs-material` and running `mkdocs gh-deploy`.

## Dependencies

Requires Python 3.x with `mkdocs-material` (which includes mkdocs). Install with `pip install mkdocs-material`.
