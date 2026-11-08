# Changelog Generator

Automatically creates user-facing changelogs from git commits by analyzing commit history, categorizing changes, and transforming technical commits into clear, customer-friendly release notes. Turns hours of manual changelog writing into minutes of automated generation.

## Overview

This repository contains the original AITMPL skill instructions and its published companion resources.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-changelog-generator-skill.git ~/.claude/skills/changelog-generator
```

On Windows, use `%USERPROFILE%\.claude\skills\changelog-generator` as the destination.

## Usage

Claude Code can load this skill when a request matches its description. Invoke directly with `/changelog-generator` when appropriate.

## Repository structure

```text
changelog-generator/
├── SKILL.md
├── README.md
└── LICENSE
```

## Runtime requirements

- No build step is required for the instruction file.
- Check any API credentials, service configuration, and Python package requirements before using examples.
- Scripts and tests have not been executed as part of this import.
