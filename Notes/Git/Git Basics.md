
#### Commands

`git init myproject` - it creates a project folder as well

`git add` - adds all the files to the tracking/staging zone
`git add file.txt` - adds only the *file.txt* to staging instance
`git add file1 file2 file3...` - for multiple files

`git commit -m "message"` - actually commits the files
`git commit -a -m"commit message"` - stages all changes of tracked files (doesn't add new ones)

`git push` - pushes code to a remote server

`git checkout master` - switch to master branch
`git checkout -b branch_name` - create branch if doesn't exist and switch to mentioned branch name

`git fetch` - similar to pull but doesn't merge with the local copy
`git merge branch_name` - merges the current and mentioned branch
`git pull` - combination of *merge* and *fetch*. Fetches changes and merges with current branch


`git log --graph --decorate --abbrev-commit --all --pretty=oneline`

#### Intialization
`git config --global user.name my_name` - set the global user name - has nothing to do with any websites credentials
`git config --global user.email my_email.com` - set the global user name - has nothing to do with any websites credentials