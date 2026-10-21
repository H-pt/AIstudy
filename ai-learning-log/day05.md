
1.解释器：运行代码的程序（机床）
包：相当于其他人写好的库（零件）
环境：解释器加一堆包 （车间）

注意：每个项目/每个学习阶段都应该装他们独立的环境
现在因为我在做本科毕设时安装Anaconda的时候，不知道，所以把他命名为了 bisheruanjian
base
E:\bisheruanjian\Anaconda这个路径（这是base基本路径）
grad 
E:\bisheruanjian\Anaconda\envs\grad （这是毕设装的环境）
sonar-reader  E:\bisheruanjian\Anaconda\envs\sonar-reader（这是声纳仿真装的环境）
今天新装的E:\bisheruanjian\Anaconda\envs\aistudy


2.conda init bash ：在gitbash里初始化conda，初始化完成后必须重新进入gitbash

conda create:创建环境  例子：
conda create -n aistudy python=3.11 -y
  ↑      ↑     ↑    ↑       ↑        ↑
  │      │     │    │       │        └─ 自动确认，不弹 y/n 询问
  │      │     │    │       └─ 要哪个版本的 Python（范围约束）
  │      │     │    └─ 环境的名字
  │      │     └─ name 的缩写（-n = name）
  │      └─ 子命令：创建
  └─ 主程序
 这样就创建出E:\bisheruanjian\Anaconda\envs\aistudy

conda activate：切换当前终端使用哪个环境。
本质是修改 PATH 环境变量，让 `python` 这个名字指向新环境的解释器。
例子：conda activate aistudy 这样就激活了刚才创建的aistudy的环境

which python：是检查python这个名字最终会执行哪个文件/检查当前python在哪个环境
注意：每次装包之前，应该用which python检查一下是否要安装的到这个路径下
  
pip install：从官方仓库里下载包，安装到当前激活的环境里面
例子：pip install numpy pandas matplotlib jupyter 下载后面这几个包

conde env list列出所有环境及其路径
例子： 输出
conda environments:         
base
E:\bisheruanjian\Anaconda
aistudy                E:\bisheruanjian\Anaconda\envs\aistudy
grad                   E:\bisheruanjian\Anaconda\envs\grad
sonar-reader           E:\bisheruanjian\Anaconda\envs\sonar-reader










