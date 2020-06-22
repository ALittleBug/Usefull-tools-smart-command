## how to use gdb

* refer [link](http://www.brendangregg.com/blog/2016-08-09/gdb-example-ncurses.html)

  * bt
* gdb tutorial
  * refer [link](https://www.cs.umd.edu/~srhuang/teaching/cmsc212/gdb-tutorial-handout.pdf) [video](https://www.youtube.com/watch?v=bWH-nL7v5F4)
  ```
  layout next
  ```
* debug segfault
  ```
  1.genetate core dump file
  2.bt
  3.f n
  4.p args
  ```
  
* how to go the previous line of gdb
  * `reverse-step` `reverse-next` refer [link](https://stackoverflow.com/questions/1206872/how-to-go-to-the-previous-line-in-gdb)
  
* Useful tips for gdb
  * refer [link](https://wizardforcel.gitbooks.io/100-gdb-tips/examine-memory.html)
  
* Debug stuck process
  * [Link 1](https://superuser.blog/debugging-stuck-process-linux/) and 
  [stack overflow link](https://stackoverflow.com/questions/3035134/debugging-utilities-for-linux-process-hang-issues)
