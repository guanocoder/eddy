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

