# Git Knowledge:

Consider coffee vs coffee shop analogy: Git is Coffee, GitHub is Coffee Shop.

Git can run locally or hosted online (GitHub).

### Git has three stages:

1. **Working Directory (Modified)** - all changes are in local storage
2. **Staging Area / Index (Staged stage)** - add files here using `git add`
3. **Local Repository (Committed)** - use `git commit -m message` to commit changes to Git/GitHub.

### Branching:

Branch in Git is a separate line of development where we can work independently. Once changes are fixed and perfected, they can be merged back into main/master branch.

**Analogy:** perfecting dish in trial kitchen before taking to main kitchen to serve customers.

Multiple branches can be created, serves as secure ways to make changes without breaking original code.

## Terminal Commands:

1. `cd filename` - change directory to "filename"
2. `mkdir filename` - make new directory of "filename"
3. `ls` - shows all files (visible)
4. `ls -la` - shows all files (hidden)
5. `cd ../` - goes back to root directory
6. `cd ..` - goes back (up) one level

## Git Basic Commands:

1. `git init` - start git tracking
2. `git status` - status of git changes
3. `git clone (https)` - clones git repo in directory (remove brackets)
4. `touch filename.extension` - creates filename with extension (one.txt)
5. `explorer.exe .` - shows file in Explorer (Windows) [for macOS, use `open .`]
6. `git add --all` or `git add -A` - adds ALL files in project directory (can also be one specific file only using `git add filename.extension` i.e. `git add one.txt`)
7. `git add .` - adds files from CURRENT directory
8. `git add *` - adds only NEW/MODIFIED files, still shows deleted files

_Note:_`--all` and `-A` for all files, `.` for files in one folder only, `*` for new files

9. `git reset` - resets all changes from `git add` before committing
10. `git commit -m "message"` - commits changes to repository
11. `git reset HEAD~` - resets last commit
12. `git rm filename.extension` - deletes and stages filename directly in one command

_Note:_ if file is modified before deleting, then Git throws errors.

`-f or --force`-forced, `--cached`-cached, `-r`-recursively

- To force delete, use `git rm -f four.txt` (`--force` works as well)
- To make file untracked but not physically deleted: `git rm --cached four.txt`
- To delete folder and subfolders inside: `git rm -r <Folder>`

13. `git reset --hard` - brings back deleted files as well as reset changes
14. `git log` - shows all commits made to repository

_Note:_ to see cleaner logs: `git log --oneline`

## Git Branch Commands:

1. `git branch` - shows branches present
2. `git branch development` - creates new branch "development"
3. `git checkout development` - switch to "development" branch

## Global Changes:

1. `git config --global user.email "rayeed.aabir@gmail.com"` - changes email address of user
2. `git config --global user.name "rayeedaabir"` - changes name of user

_Note:_ `--global` for all repositories in machine (PC/laptop), `--local` for specific repository
