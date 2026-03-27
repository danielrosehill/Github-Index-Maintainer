Review unreviewed repositories and classify them into the appropriate subindices.

## Steps

1. Load the most recent repo snapshot from `data/`
2. Filter to repos where `agent_review` is false
3. Load the list of existing subindices from `/home/daniel/repos/indexing-repos/` (directories ending in `-Index`)
4. For each unreviewed repo:
   a. Read the repo's description and name
   b. If needed, check the repo on GitHub (`gh repo view`) for more context
   c. Determine which subindex(es) it belongs in (can be multiple)
   d. Present your classification to the user for confirmation
   e. Mark `agent_review: true` and `agent_review_date` with current timestamp
5. Save the updated snapshot
6. Report summary: how many reviewed, classifications made, any repos that don't fit existing indices

If a cluster of repos suggests a new subindex topic, mention it to Daniel but don't create one without approval.

Process repos in batches of 10-15 to keep reviews manageable. Ask if Daniel wants to continue after each batch.
