# Reflection on Branching, Merge Conflicts, and Pull Requests

During this exercise, I practiced a realistic Git workflow that separates work into focused branches, resolves conflicts carefully, and uses pull requests to review and document changes.

First step: I created a repo on github > version-control-simulation-ervin

## 2 Clone the repo in local env

git clone https://github.com/your-username/version-control-simulation-ervin.git

## 3. I started by creating a feature branch, `feature/header`, from `main` to add a simple header in `index.html`.

git checkout -b feature/header
Then created an index.html file with some html tags
then git add . to stage the file and git commit
Working in an isolated branch helped me keep my changes small and understandable.

## 4 checkout to main branch again

I then created a second branch, `feature/footer`, create an index.html file and add a footer.
then git add . to stage the file and git commit

## 5 To simulate a conflict, I modified overlapping parts of `index.html` in both branches. In the footer of each branch and on the title.

## 6 I merged the footer branch and the header branch in my main branch, And I had a conflict

git checkout main
git merge feature/header
git merge feature/footer

I opened the file, compared both sides, and decided what the final HTML should contain.
The conflict markers clearly separated the versions: `HEAD` (current branch) and the incoming changes. After editing, I staged the file with `git add`, committed the resolution, and confirmed a clean working tree with `git status`.
This step reinforced that conflicts are normal in parallel work and are best handling it manually.

## 7 Pull requests

To practise pull requests I created a new branch `review/main` from main.
I added a new html tag, to the file and, after git add and commit, I pushed this branch `review/main` to origin.
Finally, I opened a pull request from `main` to a review branch, `review/main`.
After reviewing the code, I didn’t find any merge conflicts, and since the new changes were important, I merged the branch into main and closed the pull request.

## Final reflecrion

This exercise taught me the importance of Git and GitHub for collaboration in large projects and big teams, as they allow developers to work in parallel, increase productivity, and reduce the risk of code conflicts.
