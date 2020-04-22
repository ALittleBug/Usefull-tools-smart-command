# recored git commands

## common commands refer [link](https://www.cnblogs.com/springbarley/archive/2012/11/03/2752984.html) [link2](https://www.yiibai.com/git/git_push.html)
1. **git push**
    
    a.push local commits to remote branch rel-01

    ```shell
        $ git push origin HEAD:rel-01
        $ git push origin :rel-01  ## will detele remomte branch rel-01
        $ git push origin --delete rel-01
    ```
2. **git log**

    a. git log -n xxx
    
    b. git log --since=2018-06-04 or --until=2018-07-04
    
    c. git log --author="Biao"
    
    d. git log --grep="init" #just grep commit msg
    
    e. git log -p #see difference 
    
    f. git log branch_name 
    
3. **git reset**

    a. git reset HEAD -filename ##如果是撤销某个文件或文件夹
    
4. **git rm**

    a.git rm --cached <added_file_to_undo>

5. **apply patch**

    a. git apply --check file.diff and then git apply file.diff  ##refer [link](https://blog.csdn.net/salmon_zhang/article/details/97015801)
