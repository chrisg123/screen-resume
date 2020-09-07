# screen-resume
Prompt to resume detached GNU screen session

Tip:
Add something like this to your .bashrc to auto-start screen when a terminal opens and prompt to resume any detached GNU screen sessions.

```
if [[ ! $TERM =~ screen && ! $TERM =~ eterm ]]; then 
    source "$HOME/scripts/screen-resume/screen-resume"
    screen_resume; resumed="${?}"
    [[ ! "${resumed}" -eq 0 ]] && screen
fi
```
