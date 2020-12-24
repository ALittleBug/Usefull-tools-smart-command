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
  
* Generate core dump file
  * ulimit -c
  * echo "/tmp/core-%e-%p-%t" > /proc/sys/kernel/core_pattern

* Debug vptr/vtable
  * how to check the specify section of ELF file [link](https://stackoverflow.com/questions/1685483/how-can-i-examine-contents-of-a-data-section-of-an-elf-file-on-linux)
  ```
  objdump -s -j .rodata exefile [-EB -EL]
  readelf -x .rodata hello_world.o
  ```
  * how to print the dereference within gdb
  ```
  (gdb) p pp
  $1 = (Point3D *) 0x613c20
  (gdb) p pp->a
  $2 = 44
  (gdb) p /x pp
  $3 = 0x613c20
  (gdb) p /x *pp
  $4 = {_vptr.Point3D = 0x4008a0 <vtable for Point3D+16>, a = 0x2c}
  (gdb) p /x *(int *)0x613c20 ##vptr point to vtable
  $5 = 0x4008a0
  (gdb) p /x *(int *)0x613c28  ## here is the int value a
  $6 = 0x2c
  (gdb) p 0x4008a0
  $7 = 4196512
  (gdb) p /x 0x4008a0
  $8 = 0x4008a0
  (gdb) p /x *0x4008a0  ## vtable point to the actual function address
  $9 = 0x40078c
  (gdb) p /x *(long *)0x4008a0
  $10 = 0x40078c
  
  symbol table:
    69: 000000000040078c    25 FUNC    WEAK   DEFAULT   14 _ZN7Point3D1xEv

  ```
  * print register
    * i r [rax]
    
  * disassemble 
  * nexti/stepi b *address
