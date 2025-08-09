# Task: Generate Memory Bank

This task generates a 'memory bank' for a feature by analyzing the git history of a project. You have access to the GitHub repository through the integrated Model Context Protocol.

## 1. Elicit Inputs from user

1.  Ask the user for the **GitHub Repository URL**.
2.  Ask the user for the **Feature Name**.

## 2. Find Pull Requests

1.  Use your connection to GitHub to search for pull requests in the provided repository.
2.  The search query should look for PRs with the feature name in the title. For example, if the feature name is "New Login Page", search for "New Login Page" in the titles of PRs.

## 3. Process Pull Requests

For each pull request you find, extract the following information:

-   PR Number
-   PR Title
-   PR Author
-   PR Creation Date
-   PR URL
-   PR Description (the body of the PR)

## 4. Extract Review Comments

For each pull request, get all the review comments. For each comment, note the author and the content of the comment.

## 5. Analyze Commits

For each pull request, get the list of associated commits. For each commit, perform the following steps:

1.  Extract the commit SHA, author, and commit message.
2.  Get the diff for the commit.
3.  Analyze the diff to identify changed files and their status (added, modified, deleted).
4.  For each changed file, analyze the patch to identify changes to classes and methods.
    -   Look for lines starting with `+` to identify additions.
    -   Look for lines starting with `-` to identify deletions.
    -   Use regular expressions to identify class and method definitions (e.g., `class ...`, `def ...`, `function ...`).
    -   Categorize the changes as added classes, deleted classes, added methods, and deleted methods.

## 6. Generate the Memory Bank Report

Load the `memory-bank-tmpl.yaml` template from the `bmad-core/templates/` directory.

Use this template to structure the information you have gathered. Populate the template with the data you have collected for the feature, pull requests, comments, and commits.

Save the final output as a new YAML file named `memory_bank_<feature_name>.yaml`.

## 7. Present the Report

Display the full content of the generated YAML report to the user.
