# Git Hooks Practice Documentation

## pre-push

This pre-push hook checks for the presence of debugging statements in the changed files before allowing a push to proceed. If any debugging statements such as `console.log` and `debugger` are found, the push is aborted and an error message is displayed. The following error message is shown: "Error: Found debugging statement in $FILE". $FILE is the file name. 
