# claude-changelog-generator-skill

A Claude Code skill for turning Git commit history into clear, structured, user-facing release notes.

## Overview

Commit messages are written for developers. Changelogs are written for people who use or depend on the product. This skill helps translate implementation-level changes into release notes that explain what changed, why it matters, and whether users need to take action.

It supports version releases, periodic product updates, internal release summaries, and customer-facing announcements.

## Main Capabilities

- Analyze commits within a selected date range or version range.
- Group changes into meaningful categories.
- Identify user-visible features and improvements.
- Summarize bug fixes in plain language.
- Highlight breaking changes and migration requirements.
- Filter internal maintenance noise when appropriate.
- Produce consistent release-note structure.
- Adapt wording to the intended audience and product tone.

## Change Categories

| Category | Typical content |
|---|---|
| Features | New user-visible capabilities |
| Improvements | Better performance, usability, or workflows |
| Fixes | Corrected defects and unexpected behavior |
| Breaking changes | Incompatible behavior or API changes |
| Security | Security-related corrections and hardening |
| Maintenance | Internal work worth communicating when relevant |

## Installation

```bash
git clone https://github.com/Brajesh31/claude-changelog-generator-skill.git ~/.claude/skills/changelog-generator
```

## Usage

Invoke the skill when preparing release notes:

```text
/changelog-generator
```

Provide the repository, version range or time period, release audience, and any changes that must be emphasized or excluded.

## Recommended Workflow

1. Identify the release boundary, tags, or commit range.
2. Inspect commit messages and changed files.
3. Group related commits into user-facing themes.
4. Separate shipped behavior from internal implementation work.
5. Identify breaking changes and required user actions.
6. Draft concise descriptions in plain language.
7. Check every statement against the actual changes.
8. Organize the final changelog by category.
9. Review for omissions, duplication, and misleading claims.

## Example Changelog Structure

```markdown
# Version X.Y.Z

## Added
- New capability and the user problem it solves.

## Improved
- Existing workflow made faster or easier to use.

## Fixed
- Incorrect behavior that has been corrected.

## Breaking Changes
- Incompatible change and the action required.

## Security
- Relevant security improvements.
```

Use only the sections that apply to the release.

## Writing Guidelines

- Describe outcomes, not just internal code changes.
- Keep each entry focused on one meaningful change.
- Use concrete language and avoid vague claims.
- Explain user impact where it is not obvious.
- Include migration steps for breaking changes.
- Do not describe unfinished work as shipped.
- Do not infer product behavior from a commit title alone.

## Validation Checklist

- The commit range is correct.
- All user-visible changes are represented.
- Internal-only changes are handled appropriately.
- Breaking changes are clearly identified.
- Each entry matches the implemented behavior.
- No feature or fix has been invented.
- The tone is consistent across the release.

## Repository Contents

- `SKILL.md`: Main changelog generation instructions.
- `README.md`: Workflow, categories, and writing guidance.

## Maintenance

Keep the release format consistent across versions while allowing the structure to adapt to the product. Prefer accuracy over completeness when a commit does not provide enough evidence to describe its user impact.
