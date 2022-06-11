GE526 : A Dataset of Open Source Game Engines

The GE526 dataset is a collection of 526 open source game engines mined from GitHub. 
It primarily consists metadata of game engine repositories, such as commits, pull requests, and issues of the respective game engines.
This dataset was curated using Git CLI and Github API, the entire process automated using Python.

#File Structure

Root/
├── Readme.txt/
├── Data/
│   ├── Release Data.csv/
│   ├── Repository Data.csv/
│   ├── Pull Requests Data.csv/
│   ├── Pull Request Comments Data.csv/
│   ├── Issues Data.csv/
│   ├── Issue Comments Data.csv/
│   └── Commit Data.csv/
└── RepoList_104/
    └── Repos_list(Based_on_Gitlog_Thresholds)/


This Readme.txt file is present in the root of the dataset. 
The dataset contains seven files in CSV format which be found in the "Data" folder located in the root directory. Note: The CSV files are encoded in ‘latin-1’ format.

`Repos_list(Based_on_Gitlog_Thresholds)` file is the list of game engines filtered based on a threshold value of following metrics extracted from Git Logs. This file can be found in the "RepoList_104" folder located in the root directory.

1. The Commit Frequency
2. Integration Frequency
3. Committer Frequency
4. Integrator Frequency
5. Merge Frequency

Note: This file only contains limited metrics along with the url. 
(The repositories mentioned in this file may have been filtered due to presence of inconsistent data from the original dataset.)

---

- "Repository Data.csv": Contains information about the repository such as the creator and the date of creation, along with other metadata.

## Fields = [Id, owner, name, url, stars, forks, description, created_at, languages, size, commit_frequency, cimmitter frequency, integrator frequency, integration_frequency, Merge frequency, commits, releases, last_commit, Pull Requests open and closed, Issues open and closed]

---

- "Commit Data.csv": Contains information compiled from the commit logs.

## Fields = [repo_id, commit_hash, parent_hash, author_name, author_email, author_date, committer_name, committer_email, committer_date]

---

- "Release Data.csv": Contains metadata pertaining to different releases and their tags.

## Fields = [repo_id, id, title, tag_name, target_commitish, is_draft, pre_release, created_at, author, published_at, url, upload_url, html_url, tar_url, zip_url]

---

- "Pull Requests Data.csv": Contains information about the pull requests in the repository.

## Fields = [repo_id, id, additions, deletions, assignee, assignees, base, body, closed_at, comments, comments_url, created_at, commits, commits_url, deletions, head, merge_commit_sha, merged, merged_at, merged_by, html_url, labels, milestone, number, state, title, updated_at, url, user]

---

- "Issues Data.csv": Information about the repository such as the creator and the date of creation, along with other metadata.

## Fields = [repo_id, id, body, closed_at, closed_by, comments, comments_url, created_at, labels, state, title, updated_at, url, user, assignee, assignees]

---

- "Pull Request Comments Data.csv": Contains information about the comments made by users and collaborators for each pull request.

## Fields = [repo_id, id, body, created_at, commit_id, position, path, original_position, diff_hunk, pull_request_url, issue_url, updated_at, url, user]

---

- "Issue Comments Data.csv": Contains information about the comments made by users and collaborators for each issue.

## Fields = [repo_id, id, body, created_at, commit_id, position, path, original_position, diff_hunk, pull_request_url, issue_url, updated_at, url, user]
