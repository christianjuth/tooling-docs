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
