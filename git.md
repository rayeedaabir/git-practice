# Git Knowledge:

Consider coffee vs coffee shop analogy: Git is Coffee, GitHub is Coffee Shop.

Git can run locally or hosted online (GitHub).

### Git has three stages:

1. **Working Directory (Modified)** - all changes are in local storage
2. **Staging Area / Index (Staged stage)** - add files here using `git add`
3. **Local Repository (Committed)** - use `git commit -m message` to commit changes to Git/GitHub.

## Terminal commands:

1. `cd filename` - change directory to "filename"
2. `mkdir filename` - make new directory of "filename"
3. `ls` - shows all files (visible)
4. `ls -la` - shows all files (hidden)
5. `cd ../` - goes back to root directory
6. `cd ..` - goes back (up) one level

## Git Commands:

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
10.

## Global Changes:

1. `git config --global user.email "rayeed.aabir@gmail.com"` - changes email address of user
2. `git config --global user.name "rayeedaabir"` - changes name of user

_Note:_ `--global` for all repositories in machine (PC/laptop), `--local` for specific repository
