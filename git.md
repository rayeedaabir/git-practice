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

Multiple branches can be created, serves as secure ways to make changes without breaking original code. Commits made in branches are exclusive to that branch only.

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
15. `git diff latestlog earlierlog` - shows commit changes made between two versions (use latest one first)

_Note:_ to see cleaner logs: `git log --oneline`

## Git Branch Commands:

1. `git branch` - shows branches present
2. `git branch development` - creates new branch "development"
3. `git checkout development` - switch to "development" branch
4. `git merge main -m "message"` - merges main branch to development branch
5. `git merge development -m "message"` - merges development branch to main branch (do after `git checkout main`)

_Note:_ use `git log --oneline` to get commit track number, then use said number in `git checkout tracknumber` to get to previous version.

Use `git checkout main` to go to latest version.

## GitHub Push/Pull:

1. `git push origin branch` - pushes branch to GitHub
2. `git fetch` - fetches latest update from GitHub, does not show on local repository
3. `git merge` - merges with local repository
4. `git pull` - pulls and merges latest update from GitHub

_Note:_ use `git pull` to do both fetch and merge. `pull = fetch + merge`

5. `git restore filename.extension` - to restore file from last commit

_Note:_ restore mainly used to restore uncommitted changes in local repository.

- use repository name `git restore myFolder` to restore repository,
- `git restore .` to restore everything.
- `git restore --staged myFolder` or `.` to restore from staged state

6. `git stash` - stash changes before switching branches (used when committing isn't done yet)

_Note:_

- use `git stash pop` to fetch all changes back, removes from stash list.
- Git stores multiple stashes in stack, use `git stash apply` to both get the changes back as well as have stash in stack. (pop removes from list, apply keeps in list, both reverts changes.)
- Use `git stash list` to get list of stashes (has identifier marks)
- Use `git stash drop ID` to drop specific stash ID.

7. `git revert ID` - creates new commit where it brings project from previous commit (creates Commit 3 from taking Commit 1)

_Note:_ `git reset` does not keep changes after commit, deletes all changes. `git revert` creates new commit but keeps faulty commit's updates.

8. `git rebase` - updates commits on another branch to current branch, reduces commit clutter in `git log`

## Global Changes:

1. `git config --global user.email "rayeed.aabir@gmail.com"` - changes email address of user
2. `git config --global user.name "rayeedaabir"` - changes name of user

_Note:_ `--global` for all repositories in machine (PC/laptop), `--local` for specific repository
