```
 /$$    /$$ /$$$$$$ /$$      /$$
| $$   | $$|_  $$_/| $$$    /$$$
| $$   | $$  | $$  | $$$$  /$$$$
|  $$ / $$/  | $$  | $$ $$/$$ $$
 \  $$ $$/   | $$  | $$  $$$| $$
  \  $$$/    | $$  | $$\  $ | $$
   \  $/    /$$$$$$| $$ \/  | $$
    \_/    |______/|__/     |__/
```

# Read from stdin into buffer

_Note: "-" tells vim to read from stdin_

```bash
pnpm lint | vim -
```

# Autocomplete

| Shortcut | Description                |
| -------- | -------------------------- |
| \<C-N\>  | Next suggestion            |
| \<C-P\>  | Previous suggestion        |
| \<C-Y\>  | (Yes) accept suggestion    |
| \<C-E\>  | (Exit) dismiss suggestions |

# Virtual Edit

| Command                | Description           |
|------------------------|-----------------------|
| set virtualedit=insert | Only in insert mode   |
| set virtualedit=all    | In any mode           |
| set virtualedit=       | Reset back to default |

# Window Sizing

| Command   | Description             |
| --------- | ----------------------- |
| \<C-W\>_  | Maximize pane on Y axis |
| \<C-W\>\| | Maximize pane on X axis |
| \<C-W\>=  | Equally size all splits |
| \<C-W\>x  | Swap splits             |
| \<C-W\>r  | Rotate splits           |

# Markdown

| Command      | Mode | Description |
| ------------ | ---- | ----------- |
| \<C-Space\>  | nv   | Toggle todo |
