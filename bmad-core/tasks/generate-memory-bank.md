# Task: Generate Memory Bank

This task generates and maintains a 'memory bank' for the project by analyzing the git history. The output of this task is the `docs/pr_info.json` file.

## 1. Elicit Inputs from user

1.  Ask the user for the **GitHub Repository URL**.
2.  Ask the user for the **Feature Name** to search for in PR titles.

## 2. Load Existing Memory Bank

1.  Check if the file `docs/pr_info.json` exists.
2.  If it exists, load its content into a JSON object.
3.  If it does not exist, initialize an empty JSON object `{}`.

## 3. Find and Process Pull Requests

1.  Use your connection to GitHub to search for pull requests in the provided repository that have the feature name in their title.
2.  For each pull request you find:
    -   Check if the PR number already exists as a key in your JSON object.
    -   If it does not exist, add a new entry for it. The structure for each new PR should be:

```json
"prNumber": {
  "title": "The title of the PR",
  "body": "The body of the PR",
  "commits": [
    "commit_sha_1",
    "commit_sha_2"
  ],
  "changed_files": [
    "path/to/file1.js",
    "path/to/file2.py"
  ]
}
```
    -   Populate the new entry with the PR's title, body, a list of its commit SHAs, and a list of its changed file paths.

## 4. Save and Present the Report

1.  Save the updated JSON object (which includes both old and new data) to a file named `pr_info.json` inside the `docs/` directory. If the `docs` directory does not exist, create it.
2.  Display the full content of the updated `docs/pr_info.json` file to the user.
