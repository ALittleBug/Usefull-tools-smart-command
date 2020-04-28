* check thread details in a process

    * refer [link](https://unix.stackexchange.com/questions/892/is-there-a-way-to-see-details-of-all-the-threads-that-a-process-has-in-linux) and 
    [link for top](https://www.golinuxcloud.com/check-threads-per-process-count-processes/#3_Using_pstree_command)
    
    >In top, by default we will not be able to see thread count per process. But when running top, it is possible to change which fields to display and add this column to print thread count per process can be added manually.
    ```shell
    Press f
    This will show a list of fields that top can display. The fields that are displayed in bold are the ones that top will display.
    Use the down arrow to navigate to “nTH” (Number of Threads).
    Press to select “nTH“
    Press ‘s‘ to sort on number of threads.
    Press ‘q‘ to display the data of threads count.
    ```
