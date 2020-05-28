1. comment multi lines 

    a. refer [link](https://segmentfault.com/a/1190000005172434)
    ```
    多行注释：

    进入命令行模式，按ctrl + v进入 visual block模式（可视快模式），然后按j, 或者k选中多行，把需要注释的行标记起来

    按大写字母I，再插入注释符，例如//

    按esc键就会全部注释了（我的是按两下）

    取消多行注释：

    进入命令行模式，按ctrl + v进入 visual block模式（可视快模式），按小写字母l横向选中列的个数，例如 // 需要选中2列

    按字母j，或者k选中注释符号

    按d键就可全部取消注释
    ```
    ```
	• cancel number
		○ :set nonu
		○ set pastetoggle=<F9>  to avoid auto indent
	• find and replace
		○ :'<,'>s/foo/bar/g
	
	• 对于已保存的文件，可以使用下面的方法进行空格和TAB的替换： 
	TAB替换为空格： 
		○ :set ts=4
		○ :set expandtab
		○ :%retab!
	
	空格替换为TAB：
	:set ts=4
	:set noexpandtab
	:%retab!
	
	• 全选正确的答案是： 
	ggVG 
	
	• 跳转到上/下一次位置
		Ctrl + O
		Ctrl + I
	• 跳转到匹配括号 [link](https://blog.csdn.net/caisini_vc/article/details/38351133)
		<span style="font-size:18px;">vim 括号匹配跳转操作：
 
		% 跳转到相配对的括号
		gD 跳转到局部变量的定义处
		'' 跳转到光标上次停靠的地方, 是两个', 而不是一个"
		mx 设置书签,x只能是a-z的26个字母
		`x 跳转到书签处("`"是1左边的键)
		> 增加缩进,"x>"表示增加以下x行的缩进
		< 减少缩进,"x<"表示减少以下x行的缩进
		{ 跳到上一段的开头
		} 跳到下一段的的开头
		( 移到这个句子的开头
		) 移到下一个句子的开头
		[[ 跳转至上一个函数(要求代码块中'{'必须单独占一行)
		]] 跳转至下一个函数(要求代码块中'{'必须单独占一行)
		C-] 跳转至函数或变量定义处
		C-O 返回跳转前位置 
		C-T 同上 
		nC-T 返回跳转 n 次
		0 数字0,跳转至行首 
		^ 跳转至行第一个非空字符 
		$ 跳转至行尾

	• :'<,'>s:\%u00a0: :g
```
