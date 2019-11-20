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
|-O|优化|
|-Wall||
|-g|gdb调试|

# 3. 静态库的制作和使用

## 1.制作
gcc *.c -c
ar rcs libMyCalc.a *.o


## 2. 使用
 gcc main.c lib/libMyCalc.a -Iinclude
 gcc main.c -Iinclude -L lib -l MyCalc -o myapp


nm - list symbols from object files

nm lib/libMyCalc.a
nm myapp

T -- 表示在代码区

# 4. 动态库

gcc -fpic -c *.c
gcc -shared -o libMyCalc.so *.o -Iinclude

gcc main.c lib/libMyCalc.so  -Iinclude
gcc main.c -Iinclude -L./lib -l MyCalc -o myapp

查看可执行程序依赖的动态库
ldd myapp

动态库链接失败解决：
1. 放到/lib目录下
2. export LD_LIBRARY_PATH=./lib   临时设置，测试用
3. 把2的方法加入到.bashrc
4. 1. 需要找到动态链接器的配置文件
   2. 动态库的路径写入到配置文件中
   3. 更新
   sudo ldconfig -v
   sudo vi /etc/ld.so.conf
   sudo ldconfig -v


