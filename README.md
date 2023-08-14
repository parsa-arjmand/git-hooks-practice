# Custom Git Hooks

## pre-push:

This pre-push hook checks for the presence of debugging statements in the changed files before allowing a push to proceed. If any debugging statements such as `console.log` and `debugger` are found, the push is aborted and an error message is displayed. The following error message is shown: "Error: Found debugging statement in $FILE". $FILE is the file name. 

## prepare-commit-smg:
check format of commmit massage to be correct if true commit will exacute else recive error.
`[type] massage`

## commit-msg:
The commit-msg Bash script is used to ensure that everyone follows the same commit message convention. The commit message must start with a commit semantic enclosed in brackets.
e.g. "[feat] add new feature". 
The allowed semantics are: feat, chore, style, docs, init, fix, refactor, and test.

## pre-commit:

a pre-commit hook that validates commit messages to ensure they follow a specific format and semantic. The hook enforces the use of the following commit message structures:

- [feat] message
- [fix] message
- [docs] message
- [style] message
- [refactor] message
- [test] message
- [chore] message

## Usage 

To use these hooks, follow these steps:

1. Clone this repository to your local machine.

2. Copy this folder from the repository to the `.git/hooks/` directory of your target Git repository.

3. Make sure the hook files are executable. You can do this by running the following command in your terminal or command prompt:

   ```shell
   #for Linux :
   chmod +x .git/hooks/hook_name

    #for Windows:
   attrib +x .git\hooks\hook_name
Replace the hook_name with the name of the correct hook.
