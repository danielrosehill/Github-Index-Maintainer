# Github Index Maintainer

A Claude Code-powered maintenance tool for Daniel Rosehill's GitHub repository indexing system.

## What This Does

Daniel maintains 700+ public GitHub repositories organised into a hierarchy of indices:

- **[Master Index](https://github.com/danielrosehill/Index)** — the front page with category and timeline views
- **[Index of Indices](https://github.com/danielrosehill/Index-Of-Indices)** — lists all topic-specific subindices
- **Subindices** — domain-specific collections (e.g. [Agents](https://github.com/danielrosehill/Agents-Index), [MCP Projects](https://github.com/danielrosehill/MCP-Projects-Index), [Voice Apps](https://github.com/danielrosehill/Voice-Apps-Index))

This repo provides Claude Code slash commands and subagents to automate the maintenance of that system.

## Slash Commands

| Command | Description |
|---------|-------------|
| `/pull-repos` | Fetch all public repos from GitHub API into a timestamped snapshot |
| `/review-new` | Classify unreviewed repos into subindices (interactive) |
| `/update-subindex` | Update a specific subindex with new repo entries |
| `/create-subindex` | Create a new subindex repo from template |
| `/sync-indices` | Commit and push all modified indexing repos |
| `/full-refresh` | End-to-end: pull, review, update, and push |

## Subagents

| Agent | Purpose |
|-------|---------|
| `repo-fetcher` | Paginated GitHub API fetch with snapshot diffing |
| `repo-classifier` | Classifies repos into subindices by name/description analysis |
| `index-updater` | Updates subindex READMEs matching existing badge/table format |

## Usage

Open Claude Code in this directory and run any slash command:

```
/pull-repos
/review-new
/full-refresh
```

## Licence

CC BY 4.0
