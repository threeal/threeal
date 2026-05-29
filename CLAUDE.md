# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a GitHub profile repository. The primary content is `README.md`, which serves as the public-facing portfolio page. The repository also generates a GitHub Pages site with a snake contribution animation.

## Formatting

All files (Markdown, YAML, JSON) are formatted with [dprint](https://dprint.dev/):

```sh
dprint fmt    # format files
dprint check  # check formatting without modifying files
```

The Lefthook pre-commit hook runs `dprint fmt` automatically before every commit and fails if the formatter makes changes.

## CI

- **ci.yaml** — runs the Lefthook pre-commit hook across all files on pull requests and pushes to `main`; fails if `dprint fmt` produces any changes
- **deploy.yaml** — generates the snake contribution animation (via Platane/snk) and deploys to GitHub Pages; triggers daily, on push to `main`, or manually
