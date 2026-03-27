Push all modified indexing repos to GitHub.

## Steps

1. Scan all directories in `/home/daniel/repos/indexing-repos/`
2. For each directory that is a git repo:
   a. Check `git status` for uncommitted changes
   b. If there are changes, stage and commit them with a descriptive message
   c. Push to origin
3. Report summary:
   - Repos with changes pushed
   - Repos already clean
   - Any push failures

Do NOT force push. If a push fails due to upstream changes, report it rather than trying to resolve automatically.
