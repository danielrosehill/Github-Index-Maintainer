# Github Index Maintainer

## Purpose

This repo manages Daniel Rosehill's GitHub repository indexing system. The system organises his ~700+ public repos into a hierarchy of indices for discoverability.

## Architecture

The indexing system has three tiers:

1. **Master Index** — `danielrosehill/Index` — the front page with category views, topic browsing, and timeline views
2. **Index of Indices** — `danielrosehill/Index-Of-Indices` — meta-index listing all subindices
3. **Subindices** — domain-specific indices (e.g. `Agents-Index`, `MCP-Projects-Index`, `Voice-Apps-Index`)

## Key Locations

| What | Where |
|------|-------|
| All indexing repos (local) | `/home/daniel/repos/indexing-repos/` |
| Master Index | `/home/daniel/repos/indexing-repos/Index/` |
| Index of Indices | `/home/daniel/repos/indexing-repos/Index-Of-Indices/` |
| Master Index scripts | `/home/daniel/repos/indexing-repos/Index/scripts/` |
| This maintainer repo | `/home/daniel/repos/github/Github-Index-Maintainer/` |

## Key URLs

- Master Index: https://github.com/danielrosehill/Index
- Index of Indices: https://github.com/danielrosehill/Index-Of-Indices
- Example subindex: https://github.com/danielrosehill/Agents-Index

## Rules

### Data Collection
- Pull **only public repos** from GitHub
- Fields: Repo URL, Name, Description, Creation Date, Last Update
- Add tracking fields: `agent_review` (bool), `agent_review_date` (timestamp), `deleted_repo` (bool)

### Subindex Management
- Only create a new subindex when Daniel asks or when you suggest and he approves
- Repos can belong in multiple indices
- Indices can contain other indices — separate individual repos from related indices in the listing
- Follow the existing subindex template style (badge links to Master Index, table format for repos)

### Naming Conventions
- Index repos: Title-Case-With-Hyphens (e.g. `MCP-Projects-Index`)
- Pattern: `{Topic}-Index` or `{Topic}-Projects-Index`

### Privacy
- If private files are needed, use `/private/` directory (gitignored)
- This repo is public so others can model the pattern

## Slash Commands

| Command | Purpose |
|---------|---------|
| `/pull-repos` | Pull fresh list of Daniel's public repos from GitHub API |
| `/review-new` | Find unreviewed repos and classify them into indices |
| `/update-subindex` | Update a specific subindex with new repos |
| `/create-subindex` | Create a new subindex repo from template |
| `/sync-indices` | Push all modified indexing repos |
| `/full-refresh` | End-to-end: pull repos, review new ones, update indices, push |

## Subindex Template

Subindices follow a consistent format:
- Title badge linking to Master Index
- Brief description of the topic
- Table of repos with badge links to each repo
- Sections separating individual repos from related indices (if applicable)
- CC BY 4.0 licence badge
