1. Modify some clos refer [link](https://www.runoob.com/linux/linux-comm-awk.html)
    
    a. git status | awk '$1 ~ /delete/ {print $2}' | xargs git rm

2. Use awk to calculate the cols sum with specific tags
    
    a. cat file | awk '$3~/^800*/ {print $2}' | sed 's/.$//' |awk '{sum += $1};END {print sum}'
    ```
                                                 0       1280K 10000001      4      3      0      0      0      1 ffffffc1d465a000
                                             0       3776K 10000001      2      1      0      0      0      1 ffffffc1d465a200
                                             0        384K 10000001      2      1      0      0      0      1 ffffffc1d465a300
                                             0        256K 10000001      3      1      0      0      1      1 ffffffc1d465a600
                                             0          4K 10000001      2      1      0      0      0      1 ffffffc1d465a700
                                             0         64K 10000003      3      1      0      0      1      1 ffffffc1d465a900
    ```

3. awk with substr
    
    a. shell deepstream-app -v(DeepStreamSDK 5.0.1) | awk '$$1~/DeepStreamSDK/ {print substr($$2,1,3)}'
