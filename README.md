# Custom Git Hooks

## pre-push

This pre-push hook checks for the presence of debugging statements in the changed files before allowing a push to proceed. If any debugging statements such as `console.log` and `debugger` are found, the push is aborted and an error message is displayed. The following error message is shown: "Error: Found debugging statement in $FILE". $FILE is the file name. 

## prepare-commit-smg:
check format of commmit massage to be correct if true commit will exacute else recive error.
`[type] massage`

## commit-msg
The commit-msg Bash script is used to ensure that everyone follows the same commit message convention. The commit message must start with a commit semantic enclosed in brackets.
e.g. "[feat] add new feature". 
The allowed semantics are: feat, chore, style, docs, init, fix, refactor, and test.
