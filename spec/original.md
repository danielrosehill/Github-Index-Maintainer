The purpose of this repository is to maintain indexing repositories on behalf of the user, Daniel Rosehill.

Note: this repo is open-source so that others can model the pattern, if desired. If we need to stash files that are private, use /private and add to .gitignore - or create a private repository with private files and code.

## Indexing Repos

Daniel creates a lot of Github repositories and has devised an organisation system that you will help to administer. 

It works like this and is designed to organise repositories and pass data onto frontends:

1: The "Master" Index

https://github.com/danielrosehill/Index

This is the "front page" and is periodically updated. It includes category pages and links to indexes.

2: The Subindex

Formerly known as the "Index Of Indices" (!) this repo lists the subindices. Subindices are domain-specific. 

3: The Subindices

Subindices cluster repositories that focus on a common theme: these include Daniel's major intersts (MCP, Voice Agents, Jewish Proejcts) and  some that are more format-based (like Notes Index which bundles together repos which are basically open source notebooks).

E.g.

https://github.com/danielrosehill/Agents-Index

## General Patterns

Indexing repos live here, locally: /home/daniel/repos/indexing-repos

## Recommendations

Create, in this repository, a timestamed index of Daniel's repositories. Important: pull only public repos.

Pull only these fields from Github: Repo URL, Name, Description, Creation Date, Last Update 

Add a field called agent_review and agent_review_date and deleted_repo. The first is a Boolean and you can use it to note if you have reviewed it for whether it's in an index. The second is for a timestamp. The third is a Boolean for if the repo was deleted. 

## Subindex Template

The subindexes follow a templated style, including a link to the master index. 

-

# Q & A 

## When Should I Create A New Subindex

Daniel will tell you or you can suggest when you feel like one is warranted. Bear in mind: Daniel uses subindices to keep track of his *own* projects - so they are an internal organisational tool also!

We do not need (or want) a subindex about every single cluster of repositories. 

## Can A Repository Belong In Multiple Indices?

Yes

## How Should I Create A New Subindex?

- Create a new repo 
- Follow the template 
- Add the repos 
- Push 
- Update the Subindex with the new topic index

## Can Indexes Contain Other Indexes

Yes. 

For example: the AI Projects Index can contain Voice AI Demos. But separate, if doing so, between individual repositories and related indices.

---

## New Repo Protocol

Daniel creates a new repo.

You should:

- Check what it's about 
- Add it into the relevant (index(es)
- Push them 

For a batch of new repos, check which are new versus the existing data index and proceed through this one by one. 








