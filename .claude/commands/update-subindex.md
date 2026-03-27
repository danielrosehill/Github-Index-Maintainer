Update a specific subindex with new repository entries.

## Usage

Provide the subindex name as an argument, e.g.: `/update-subindex Agents-Index`

## Steps

1. Identify the target subindex from the argument (or ask which one to update)
2. Read the current README.md of that subindex from `/home/daniel/repos/indexing-repos/{name}/`
3. Load the most recent repo snapshot from `data/` and find repos classified for this subindex
4. Compare against what's already listed in the subindex README
5. For new repos not yet in the subindex:
   a. Add them in the correct format (table row with badge link, matching existing style)
   b. Maintain alphabetical ordering within sections
6. Remove any repos marked as `deleted_repo: true`
7. Commit the changes to the subindex repo
8. Report what was added/removed

Preserve the existing formatting style of each subindex — they use badge-style links and markdown tables.
