1. Modify some clos refer [link](https://www.runoob.com/linux/linux-comm-awk.html)
    
    a. git status | awk '$1 ~ /delete/ {print $2}' | xargs git rm
