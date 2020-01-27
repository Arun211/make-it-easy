## Steps to move repositories between different GitHub hosting

### Assumption

  - Target repository is created already and necessary permissions are added to push

### Steps

  - Clone existing to local repository.

    ```
      git clone --mirror git@github.com:Arun211/myproject.git
    ```

  - Switch to downloaded repository directory

    ```
      cd myproject.git/
    ```

  - Add target repository (Remember, we assumed that we have target repository) as remote repository. Here I use name `upstream`

    ```
      git remote add upstream git@github.mycompany.com:mycompany/companyproject.git
    ```

  - To confirm, display all remote repositories (Not a mandatory step)

    ```
      git remote -v
    ```

  - Push to new repository

    ```
      git push upstream --mirror
    ```

### Documentation for --mirror

    > Set up a mirror of the source repository. This implies --bare.
    > Compared to --bare, --mirror not only maps local branches of the source to local branches of the target, it maps all refs (including remote branches, notes etc.)
    > and sets up a refspec configuration such that all these refs are overwritten by a git remote update in the target repository.
