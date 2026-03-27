Pull a fresh snapshot of Daniel's public GitHub repositories and save it as a timestamped data file.

## Steps

1. Use the GitHub API (`gh api`) to fetch ALL public repos for user `danielrosehill`
2. For each repo, extract: URL, Name, Description, Creation Date, Last Update
3. Save as JSON to `data/repos-YYYYMMDD.json` in this repository
4. Compare against the most recent previous snapshot (if any) and report:
   - New repos since last pull
   - Deleted repos (present before, missing now — mark `deleted_repo: true`)
   - Count summary
5. Ensure each repo entry has the tracking fields: `agent_review` (default false), `agent_review_date` (null), `deleted_repo` (false)
6. Carry forward `agent_review` and `agent_review_date` values from the previous snapshot for repos that were already reviewed

Important: Only pull PUBLIC repos. Use pagination to get all repos (Daniel has 700+).
