```
  /$$$$$$  /$$$$$$ /$$$$$$$$
 /$$__  $$|_  $$_/|__  $$__/
| $$  \__/  | $$     | $$   
| $$ /$$$$  | $$     | $$   
| $$|_  $$  | $$     | $$   
| $$  \ $$  | $$     | $$   
|  $$$$$$/ /$$$$$$   | $$   
 \______/ |______/   |__/   
```

# Helpful Commands
| Command                  | Description                                              |
| ------------------------ | -------------------------------------------------------- |
| git merge-base HEAD main | Where did my current branch and main last share history? |

# Worktrees

| Command                                      | Description                   |
| -------------------------------------------- | ----------------------------- |
| git worktree add \<path\>                    | Add worktree                  |
| git worktree add \<path\> -b \<branch-name\> | Add worktree branch specified |

## Troubleshooting

If the upstream is not setup correctly when trying to pull or push, make sure the following command returns what is shown below. This seems to happen with the gitHub cli.

```bash
git config --get remote.origin.fetch

+refs/heads/*:refs/remotes/origin/*

```

if it does not run the following


```bash
git config remote.origin.fetch "+refs/heads/*:refs/remotes/origin/*"
```

# Renaming a branch

> If the renamed branch is the head branch of an open pull request, this pull request is closed. 

https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository/renaming-a-branch


```bash
# Rename your local branch
git branch -m old-branch-name new-branch-name

# Push the new branch to GitHub
git push origin new-branch-name

# Delete the old branch from GitHub
git push origin --delete old-branch-name
```

# Lint Changed Files

```bash
git diff --name-only --diff-filter=ACMR "$(git merge-base HEAD main)"..HEAD \
  | rg '\.(js|jsx|ts|tsx)$' \
  | xargs -r pnpm exec eslint -f checkstyle \
  | reviewdog -f=checkstyle -reporter=local -filter-mode=added -diff="git diff $(git merge-base HEAD main)..HEAD"
```

## Scope To One App Or Package

This example only lints changed JS/TS files under `apps/perch-webapp`:

```bash
git diff --name-only --diff-filter=ACMR "$(git merge-base HEAD main)"..HEAD \
  | rg '^apps/perch-webapp/.*\.(js|jsx|ts|tsx)$' \
  | xargs -r pnpm exec eslint
```

## Notes

- `--diff-filter=ACMR` includes added, copied, modified, and renamed files.
- This assumes filenames do not contain spaces or other unusual whitespace.
