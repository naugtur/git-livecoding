# git-livecoding
a tool to show commits from history as if they were about to be made

## Usage

`gitnext` skips one commit forward and displays it as unstaged changes on a detached head
`gitback` goes back one commit and does the same

### Livecoding without typing

Create history to go through step-by-step  
Go through the livecoding without typing the code and risking typos  
Still be able to show changes step by step in your IDE

#### In terminal
```bash
git checkout -f INITIAL_REF_TO_START_WITH
gitnext
# show the code as if the next commit was written but not committed yet
gitnext
# switch to a newer commit and display it like it's just been written
# someone asked a question about the previous state, go back
gitback
# return to clean state
git checkout -f main

```

#### VSCode tasks

 - Copy the tasks and scripts from `.vscode` to your project's `.vscode`
 - Set these keybindings for convenience

```
 {
    "key": "ctrl+shift+.",
    "command": "workbench.action.tasks.runTask",
    "args": "gitnext"
},
{
    "key": "ctrl+shift+,",
    "command": "workbench.action.tasks.runTask",
    "args": "gitback"
},
```
