# My current feature branching workflow.

1. Fork/Create new repo.
2. Clone the fork/new repo to your computer using SSH:

   ```bash
   $ git clone git@example.com:project-name.git
   ```

3. Create new branch and check it out:

   ```bash
   $ git switch -c feature_name  /
   $ git checkout -b feature_name /
   $ git branch feature_name && git switch feature_name
   ```

4. WRITE CODE
5. Add & Commit the code:
   ```bash
   $ git add file_name/ . (to add all files) && git commit -m "My commit massage"  /
   $ git commit -am "My feature is ready" 	(to auto stage all modified files and commit with a message).
   ```
6. Push your branch to Github
   ```bash
   $ git push -u origin feature_name
   ```
   > just for the first push, after that just write `git push`
7. The next day:
   - write code,
   - add, commit & push code
8. when the feature is done and ready to be merged to main:

   ```bash
   $ git switch main
   $ git merge --no-ff feature_name (--no-ff is what makes the git graph look the way you'd expect)'
   $ git branch -d feature_name
   $ git push -u origin main
   ```

   &ensp;

#### WHEN WORKING WITH OTHERS / CONTRIBUTING TO OSS/ JUST FEEL LIKE USING THE GITHUB WEBSITE

7.  - Create pull request in GUI
    - Accept / wait for the pull request to be accepted,
    - merge pull request in github (github uses git merge --no-ff. use it too).

    > btw: github will auto delete the feature branch from remote
    > (and local, if using the desktop app) after merging it.

8.  pull changes from github.

    ```bash
    $ git pull
    ```

---

NOTES:

- [feature branching guide](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)
- [this workflow is mainly copied from](https://stackoverflow.com/a/14865661)
- [for different Git merge strategies](https://www.workingsoftware.dev/which-git-merge-strategy-is-appropriate-for-our-team/)
