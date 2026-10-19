linux一些命令行

一.相对路径和绝对路径（cd之后要加空格）
绝对路径：从根开始的完整地址 例：cd /d/AIstudy
相对路径：从当前位置开始，其中.是当前目录，..是上一级目录 例：cd .. 返回到d盘   cd ./ai-learnning-log进入日志文件夹
注：在输入路径时尽量用tab补全

二.动手训练

1.
pwd             显示当前位置
cd /d/AIstudy   进入AIstudy文件夹
pwd             显示当前位置
ls              现在位置里面有什么内容
cd ai-learning-log 用相对路径进入ai-learning-log文件夹
pwd             显示位置
cd ..           相对路径返回上一级
cd ~            返回主目录
pwd             显示位置

2.
cd /d/AIstudy                        进入AIstudy文件夹
mkdir -p playground/level1/level2    {mkdir创建文件夹，-p在创建多层文件夹时自动补全中间层，有两种形式mkdir -p a/b/c指的是a-b-c嵌套三级  mkdir -p a/b a/c 是a中创建bc两个并列文件夹}
cd playground                        进入playground文件夹
touch hello.txt                      创建文本文件hello
ls -l                            列出长格式（多显示权限、大小、时间）

3.
cp hello.txt hello_copy.txt      cp a b  复制a到创建b
mv hello_copy.txt world.txt      mv a b  有两个用法1.当b不存在时将a改名为b   2.当b是已存在的目录时将a搬进b中  3.当b是已存在的文件时a将覆盖b文件中的内容
ls                               显示当前位置有什么
mkdir backup                     创建backup文件夹
mv world.txt backup/             将world。txt移动到backup文件夹（必须加/代表文件夹）
ls backup                        指定展示backup文件夹里面的内容
rm hello.txt                     删除hello。txt
ls                               展示当前位置有什么

4.
echo "hello linux" > note.txt     echo打印“hello linux”指向（创建）note.txt文件  >单箭头指向时若没有文件就创造文件，若有note.txt文件就覆盖文件内容
echo "second line" >> note.txt     echo打印“second line”指向（创建）note.txt文件  >>双箭头指向时若没有文件就创造文件，若有note.txt文件则在文件下添加内容
cat note.txt                       cat打印整份note文件内容
head -1 note.txt                   head -x note.txt打印note文件中前x行内容
tail -1 note.txt                   tail -x note.txt打印note文件中后x行
grep "second" note.txt             在note文件中查找second并打印他所在行

5.
ls /d/AIstudy | grep "log"          将d盘AIstudy内容接入管道后查找其中含有log的文件名
cat note.txt | grep "hello"         将打印的note文件所有内容接入管道，查找其中的hello
echo "a b c d" | wc -w              打印abcd  wc是统计工具 -w统计单词数目

三.
报错为bash  一般为语法错误 命令拼错或者漏空格了

