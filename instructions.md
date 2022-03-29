To create a branch that is connected to different remote:

1. fetch the foreign branch from target remote
    ```
    $ git fetch "git@git.gosuslugi.local:pgs2-rtlabs/eddy.git" master
    ```
2. create 'foreign' branch for the remote changes
    ```
    $ git checkout -b foreign FETCH_HEAD
    ```
3. fetch 'foreign' branch with changes
    ```
    $ git fetch origin
    ```

To merge local branch with 'foreign' branch

4. go to your target branch
    ```
    $ git checkout main
    ```
5. merge it with the foreign branch
    ```
    $ git merge foreign --allow-unrelated-histories
    ```


Need to setup the correct origin and upstream

1. add remote and fetch its contents
    ```
    $ git remote add gitlab git@git.gosuslugi.local:pgs2-rtlabs/eddy.git
    $ git fetch gitlab
    ```

2. go to target branch
    ```
    $ git checkout gitlab
    ```

3. Set the upstream to target branch

    ```
    $ git branch --set-upstream-to gitlab/master
    ```

4. The same thing only vice versa must be done with the gitlab clone
