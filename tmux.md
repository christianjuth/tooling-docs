```
 /$$$$$$$$ /$$      /$$ /$$   /$$ /$$   /$$
|__  $$__/| $$$    /$$$| $$  | $$| $$  / $$
   | $$   | $$$$  /$$$$| $$  | $$|  $$/ $$/
   | $$   | $$ $$/$$ $$| $$  | $$ \  $$$$/ 
   | $$   | $$  $$$| $$| $$  | $$  >$$  $$ 
   | $$   | $$\  $ | $$| $$  | $$ /$$/\  $$
   | $$   | $$ \/  | $$|  $$$$$$/| $$  \ $$
   |__/   |__/     |__/ \______/ |__/  |__/
```

# Layout management

_Note: M is option on Mac_

## Selecting a layout

| Shortcut | Description                                           |
|----------|-------------------------------------------------------|
| M-<1-7>  | Arrange panes in one of the seven preset layouts.     |
| Space    | Arrange the current window in the next preset layout. |

## Resizing the current layout
| Shortcut | Description           |
|----------|-----------------------|
| M-E      | Size all panes evenly |

## Swap panes in the current window 
| Shortcut | Description                                               |
|----------|-----------------------------------------------------------|
| {        | Swap with the pane having the previous visible pane index |
| }        | Swap with the pane having the next visible pane index     |

# Troubleshooting

| Issue                                                             | Fix                |
|-------------------------------------------------------------------|--------------------|
| Weird line wrapping or trailing `%` when running commands in pane | `stty sane`        |
| Window stops being responsive to terminal window                  | `resize-window -A` |
