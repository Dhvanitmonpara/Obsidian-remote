# Working with directories

| Command                                  | Full form if exist        | Use                                                                 |
| ---------------------------------------- | ------------------------- | ------------------------------------------------------------------- |
| `pwd`                                    | Present working directory | Shows path of present working directory                             |
| `ls`                                     | List (maybe)              | Lists your content                                                  |
| `cd [path]`                              | change directory          | change directory                                                    |
| `cd ..`                                  | change directory up       | Go to upper page of directory                                       |
| `touch [filename]`                       | -                         | To create a new file in your git repo                               |
| `git rm [filename]`                      | Git remove                | To delete file                                                      |
| `git mv [currentfilename] [newfilename]` | Git move                  | For changing file name because moving and renaming is same in linux |

# Git remote repos

| command                            | Full form if exist | Use                                                                                                                                             |
| ---------------------------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| `git status`                       | -                  | shows status of current working directory                                                                                                       |
| `git innit`                        | -                  | For initialize git repo                                                                                                                         |
| `git add [filename]`               | -                  | For put files on staging area                                                                                                                   |
| `git add --a` or `git add .`       | -                  | Put all files on staging area                                                                                                                   |
| `git rm --cached [filename]`       | -                  | Remove from staging area                                                                                                                        |
| `git commit -m "My first repo"`    | -                  | Commit all staged files                                                                                                                         |
| `rm -rf .git`                      | -                  | Remove from tracking repo and delete all files                                                                                                  |
| `git clone [repolink] [filename]`  |                    | For cloning the whole repo in your pc and`[filename]` uses for declaring a saperate name for loacl, you can also clone a repo without adding it |
| `git -a -m "Direct commit"`        | -                  | Skip staging area and commit directly                                                                                                           |

# Working with remote

| command                            | Full form if exist | Use                                                                               |
| ---------------------------------- | ------------------ | --------------------------------------------------------------------------------- |
| `git remote [repolink]`            | -                  | Connects your local directory with git remote repo                                |
| `git push origin [branchname]`     | -                  | Push your local directory to git repo                                             |
| `git remote add origin [repolink]` | -                  | Same command as `git remote [repolink]` just insert `add origin` in command       |
| `git remote`                       | -                  | Shows your all remote repos                                                       |
| `git remote -v`                    | -                  | Shows fetching/pulling and pushing remote repo                                    |
| `git push -u origin main`          | -                  | Same as `git push` but `-u` represents user and `origin main` defines branch name |
|                                    |                    |                                                                                   |

# Git log

| command                                   | Full form if exist | Use                                                                                 |
| ----------------------------------------- | ------------------ | ----------------------------------------------------------------------------------- |
| `git log`                                 | -                  | Shows all commits                                                                   |
| `git log -p`                              | -                  | Shows all commits with changes                                                      |
| `git log -p -3`                           | -                  | If you write -3 after of -p it will show 3 commits according to your written number |
| `git log --stat`                          | -                  | Shows all commits in short                                                          |
| `git log --pretty=full`                   | -                  | Shows all commits in more details in compare to `--stat`                            |
| `git log --pretty=short`                  | -                  | Shows all commits in short                                                          |
| `git log --pretty=oneline`                | -                  | Shows all commits in one line                                                       |
| `git log --since=2 days`                  | -                  | Shows all commits of last 2 days                                                    |
| `git log --pretty=fomat, [writesomething` | -                  | Go to "git scm log preety documentation"                                            |

**Note:** Click on `Q` and `enter` to exit from log page.

# Git ignore

Create `.gitignore` file and put all ignoring files into it (just write file names into it) 

**Pro tip:** Use `*.log` it means ignore all files which has `.log` extension.

# Git diff

| command            | Full form if exist | Use                                                    |
| ------------------ | ------------------ | ------------------------------------------------------ |
| `git diff`         | -                  | Difference between working directory and staging area  |
| `git diff -staged` | -                  | Difference between Last/recent commit and staging area |


# Working with commits

| command                           | Full form if exist | Use                                                                                                 |
| --------------------------------- | ------------------ | --------------------------------------------------------------------------------------------------- |
| `git commit -amend`               | -                  | To change previous commit                                                                           |
| `git restore --staged [filename]` | -                  | Unstage file                                                                                        |
| `git restore [filename]`          | -                  | Restore modification to last commit                                                                 |
| `git checkout -- [filename]`      | -                  | Unmodify repo, it will get your file into last commit status but it will only work on unstaged file |
| `git checkout -f`                 | -                  | It will take your whole working directory into last commit but it is only works on unstaged files   |
|                                   |                    |                                                                                                     |



Git alias commands >>

Git config --global alias.st status
Git config --global alias. Unstage 'restore --staged --'

Branches >>

Git checkout -b [branch name] (create new branch)
Git checkout [branch name] (change branch)

Git branch -d [branchname] (delete branch and If you didn't merged this branch git will give you warning)
Git branch -D [branchname] (it will directly delete and throws no error)

Git branch --merged (shows already merged branches)
Git branch --no-merged (shows non merged branches)

Git branch (shows all branches)
Git branch -v (shows last commits of all branches)

Git merge [another branch] (merge your current branch with another branch)

Merge conflicts >>

Accept one change from vs code and then run "git add ." and commit it.

Branch pushing >>

Git push origin [branchname] (jis branch ko push kr rhe ho ushi branch me rehkar push kro for eg. Bugfix ko push kr rhe ho to bugfix me reh kr hi kro)

Git push origin [branchnameOnLocal]:[branchnameOnRemote] (mtlb local wali branch remote pe dusre naam se push krne ke liye)

Git push -d origin [branchname] (delete remote repo)