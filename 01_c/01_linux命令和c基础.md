# 1. cd

# 2. pwd
##  pwd - print name of current/working directory

# 3. ls 
## ls - list directory contents
## ls [OPTION]... [FILE]...
|选项|英文|作用|
|-|-|-|
|-a|--all|do not ignore entries starting with .|
|-l|||
|-h|||
|-|
|--|




# 4. 查看文件内容
## cat	nl	head/tail
## cat - concatenate files and print on the standard output
## 

# 5. 文件移动和复制
## cp	mv	

# 6. 创建和删除文件
## touch	rm	mkdir	rmdir

# 7. vi 编辑器的使用
## 1. vi的三种模式
### 命令模式 <---> 编辑模式 a,i,o   esc
### 命令模式 ---> 末行模式  :
### 命令模式 --- 复制，粘贴
### 插入模式 --- 编辑
### 末行模式 --- 保存，退出，查找，替换，列出行号

## 2. vim修改
### tab默认4个空格
vim /etc/vim/vimrc
set ts=4
set expandtab
set autoindent

### 显示行号
set number

## 3. vi拷贝与粘贴
x 删除expurgate
dd	删除行delete
yy	yank复制
pP	粘贴put
u	undo

## 4. vi保存和退出
q! 强制退出
w	write
x	exit保存退出 = wq
w File 另存为，不退出
r File	读取File,插入到光标后

## 5. 光标命令
hjki (左，下上，由)
:N
1G	第一行
G 	最后一行
set number
set nonu




## 6. vi查找
/string
n 向下
N 向上
支持正则	/^the	/ends^

## 7. 替换
:范围s/oldstr/newstr/ 默认范围是当前行
:s/str1/str2/
:s/str1/str2/g 全部替换
:.,$s/str1/str2/g 当前行到最后一行
:1,$s/str1/str2/g	全文
:%s/str1/str2/g		全文
:10,15s/str1/str2/g 	10-15行全部替换






