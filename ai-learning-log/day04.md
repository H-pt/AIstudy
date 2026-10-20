1. 本地仓库：在自己电脑上的仓库，day03创建的git；  远程仓库：是指上传到github上，无论在自己电脑还是实验室电脑都能会看到
remote:远程仓库调用
origin：远程仓库默认名称
push：把本地上传到远程（写完内容备份时用）
fetch：从远程仓库下载到本地（会从远程下载到origin/main，不会影响自己的main仓库）
pull：把远程仓库的修改下载并同步到自己的仓库（直接同步到自己的main里）
ssh：密钥本地保存  私钥："C:\Users\DELL\.ssh\id_ed25519"
           公钥"C:\Users\DELL\.ssh\id_ed25519.pub"

        你的电脑 D:\AIstudy
   ┌────────────────────────────────────┐
   │                                    │
   │   main          ← 你自己的工作分支   │
   │   origin/main   ← 远程 main 在你本地 │
   │                    的一份"镜像指针"  │
   │                                    │
   └────────────────────────────────────┘
              │
              │  git push / pull
              ↓
   ┌────────────────────────────────────┐
   │  GitHub 上的 main                   │
   └────────────────────────────────────┘

你的电脑                           GitHub（云）
┌──────────────┐                  ┌──────────────┐
│ D:\AIstudy   │  ── git push ──> │  远程仓库     │
│ (.git 在这里) │  <── git pull ── │              │
└──────────────┘                  └──────────────┘
   本地仓库                          远程仓库 remote


2.ssh-keygen  ：生成ssh密钥 
例子：ssh-keygen -t ed25519 -C "254477346@qq.com"
-t ed25519 = 密钥类型
-C = 备注，填你 GitHub 绑定的邮箱


ssh -T git@github.com  ：测试连接是否成功

git remote add ： 给Git 的"通讯录"里存一条：给某个远程仓库地址起个外号。 
 例子：git remote add origin git@github.com:H-pt/AIstudy.git
 git remote，列出配置过的远程仓库的名字
 add新建联系人
 origin：外号
 git@github.com:H-pt/AIstudy.git 给该仓库起的外号 
 给git@github.com:H-pt/AIstudy.git这个仓库起外号叫origin
这样可以省去每次都写仓库全称，只写外号即可

git push： 上传远程仓库
git branch -M xxx：强制改名本地分支名为xxx


3.私钥和公钥： 
有私钥可以得出公钥，有公钥得不到私钥
私钥（钥匙）：保存在自己本地，相当于自己电脑的标签
公钥（门锁的膜具）：贴在github，当push私钥后，github会用公钥核对私钥，对了就会上传