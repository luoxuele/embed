# 1. gcc编译过程
|column1|column2|column3|
|-|-|-|
|预处理器：cpp|gcc -E|.ic文件|
|编译器 gcc|gcc -S|.s汇编文件|
|汇编器 as|gcc -c|.o二进制文件|
|链接器 ld|gcc |可执行文件|

ESc?哈哈

|||||
|-|-|-|-|-|
|||||

# 2. gcc 常用参数
|-o||
|-|-|
|-D||
|-O||
|-Wall||
|-g||

# 3. 静态库的制作和使用
1.制作


 gcc main.c lib/libMyCalc.a -Iinclude
 gcc main.c -Iinclude -L lib -l MyCalc -o myapp




