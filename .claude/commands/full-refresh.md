End-to-end index maintenance: pull repos, review new ones, update all indices, and push.

## Steps

1. **Pull repos** — Run the /pull-repos workflow: fetch all public repos from GitHub API, save snapshot, identify new/deleted repos
2. **Review new repos** — For any unreviewed repos, classify them into subindices (get Daniel's confirmation for each batch)
3. **Update subindices** — For each subindex that has new repos to add, update its README
4. **Update Master Index** — Run the existing scripts in `/home/daniel/repos/indexing-repos/Index/scripts/` if appropriate, or update manually
5. **Sync** — Commit and push all modified indexing repos

Report progress at each stage. Pause for confirmation before the sync step so Daniel can review changes.
