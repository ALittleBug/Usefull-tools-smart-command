1. find with exclude some dirs refer [stack overflow link](https://stackoverflow.com/questions/4210042/how-to-exclude-a-directory-in-find-command)

    a.find ./ -type f  -not -path "./.git/*" -not -path "./models/*" |xargs grep  uff

2. find without recursion refer [link](https://stackoverflow.com/questions/3925337/find-without-recursion)

    a.find . -name “*.txt” -maxdepth 1
2. delete the find files
    find ./ -name *~ -delete

