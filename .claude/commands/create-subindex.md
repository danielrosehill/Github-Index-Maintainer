Create a new subindex repository for a given topic.

## Usage

Provide the topic as an argument, e.g.: `/create-subindex Voice-AI`

## Steps

1. Determine the repo name: `{Topic}-Index` (Title-Case-With-Hyphens)
2. Confirm the name and topic with Daniel before proceeding
3. Create the new repo on GitHub:
   ```
   gh repo create danielrosehill/{Name}-Index --public --description "{Topic} related repositories"
   ```
4. Clone it to `/home/daniel/repos/indexing-repos/{Name}-Index/`
5. Create a README.md following the subindex template:
   - Master Index badge link at the top
   - Index Repo type badge
   - GitHub profile badge
   - Licence badge (CC BY 4.0)
   - Brief description
   - Table of repos with badge links
   - Sections for individual repos vs related indices (if applicable)
6. Add initial repos from the latest data snapshot that match this topic
7. Commit and push the new subindex
8. Update the Index-Of-Indices README to include the new subindex entry
9. Commit and push Index-Of-Indices
10. Report what was created and how many repos were added
