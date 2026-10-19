1.工作区----（git add）----暂存区--（git commit）----版本库   工作区是手里拿的，暂存区是购物车里的，版本库是结账后的

2.git init：把当前目录变成一个仓库   今天我在AIstudy目录下输入git init 将AIstudy变成一个仓库
git status看三个区当前的状态  红色代表还没有add到暂存区，绿色代表在暂存区还没有提交
git  add将工作区放进暂存区
git commit -m将暂存区提交存档
git log看历史档案
git diff看看"工作区 vs 暂存区"的差异，还没add的改动有哪些（+是添加的内容  -是删除的内容）

3.gitignore文件是git不会追踪的部分，是不会提交的内容（虚拟环境，缓存文件等）

