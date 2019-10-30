The purpose of this document is to explain our desired workflow.

## Commiting new code

Commits should not happen directly on the master branch. When you need to contribute new code, fix a bug or a typo, etc., you need to do the following steps:

1. Create your own branch locally. Pushing it to the repo is fine, if you want to back up your work.

```
git checkout -b new-feature
```

2. Create commit(s) on that branch.

```
git commit -a -m "Commit title"
```

3. When you think you are ready with the changes, rebase on top of the master branch, so that no conflicts happen.

```sh
git fetch origin # Fetch latest changes from the repository
git rebase origin/master
```

At this point, several conflicts might turn up. git will print a line for each conflict it finds, conflicts are marked with `<<<<<`, `>>>>>>` and `======` in the source files. For each such conflict, fix it, then add the fixed file to the commit(`git add path/to/file`). Finally do `git rebase --continue` to move on to the next commit.

4. Open a new Pull request and check that any automatic checks (if they exist) are not failing. Wait for review.

```
git push --set-upstream origin new-feature
```

Go to the Github website, go to branches, click on "New Pull request".

5. If reviewer requests changes, then fix your code/whatever, create and push new commits.

6. When the reviewer accepts changes, they can be merged into master, and the branch should be deleted to avoid cluttering the repo with old branches.

## Work distribution

At the beginning of each phase, the work needs to be distributed by the phase leader. To make sure everyone knows what everybody is doing, the phase leader can do the following:

1. Open issues for the various work items for the current phase. For example, "Write requirements for the command line inteface".
2. Assign the responsible person to the issue.
3. The assigned person could open multiple (sub)issues and PRs related to the task while working on it.
4. When a person is ready with the given issue, just add "Fixes #N" comment in the PR containing the necessary changes. The issue will be automatically closed.
