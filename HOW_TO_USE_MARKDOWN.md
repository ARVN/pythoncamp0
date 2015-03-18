##一个命令行能做很多事
今晚的目标：
- 教大妈在 终端内（命令行方式）使用vim和git完成教程写作以及推送至github/gitbook
- 第二个目标，markdown教程

### 第一步骤
假定你已经
- 在终端里使用 sudo apt-get install git 安装了 git客户端;
- 已经使用命令：git init 对文件夹进行了版本控制的初始化;
- 并使用 git config --global user.name 'uname'添加了用户名 ;
- 和 git config --global user.email 'youremail' 添加了用户邮箱;

- 注册成功github，并使用github帐号登录gitbook并关联上你的github中你创建的repository;

### 第二步骤
- 此时使用 touch 文件名 的方式（touch HOW_TO_USE_MARKDOWN.MD) 在目录上创建一个 “ HOW_TO_USE_MARKDOWN.md文档;
- 进入vim：在此终端上输入 vim 进入vim的命令行窗口;
- 使用：e+文件名（即 “：e HOW_TO_USE_MARKDOWN.md”) 打开刚才创建的文档;
- i键入编辑模式，。。。写完用：wq 保存文档退出 vim
- 使用git add 和 git commit -m“” 和 git push 三个命令push至远程Repo

