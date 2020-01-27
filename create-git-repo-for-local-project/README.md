## Add any existing project to GitHub via CLI

- Create a new repository on github.com

- Change the current working directory to your local project in your terminal

- Initialize the local directory as a Git repository using

  ```
    git init
  ```

- Add/Select all the files in current working directory to stage it for initial commit

  ```
    git add .
  ```

- Commit all staged files

  ```
    git commit -m 'First commit'
  ```

- Copy remote repository URL from GitHub repository created in first step and add it as remote repository for current project

  ```
    git remote add origin <Copied GitHub remote repository URL>
  ```

- Push committed changes in local repository to GitHub

  ```
    git push -u origin master
  ```

## Issues

- if there is any issues, like below, due to different commit history (mostly happens when new repository is created with readme.md)

  ```
    ! [rejected]        master -> master (fetch first)
    hint: Updates were rejected because the remote contains work that you do
    hint: not have locally. This is usually caused by another repository pushing
    hint: to the same ref. You may want to first integrate the remote changes
    hint: (e.g., 'git pull ...') before pushing again.
  ```

  Run below commands

  ```
    git pull --allow-unrelated-histories origin master
    git push -u origin master
  ```

  or try running

  ```
    git push -u -f origin master
  ```
