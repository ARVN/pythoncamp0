### UBUNTU 里怎么搞定git SSHkey
-  使用本地终端 输入命令： sudo apt-get install git ，安装git
- 再者你已经创建了github帐号了，也知道哪里填SSHkey，只是还不知道key从哪里来，哪里来呢，本地终端告诉你：在我这里。
- 使用本地终端的SSH 命令 ：ssh -T git@github.com 尝试呼叫（链接） github 的ssh服务器，被拒绝（太苦了它告诉你）：Permission denied (publickey).
- 使用本地终端SSH 命令 ：ssh-keygen -C "yourname@yourcompany.com" -f ~/.ssh/github ，它能生成sshkey，被保存在~/.ssh/github.pub 里。
- 剩下的是终端命令copy它，我忘了命令了，哪位大侠。。补充；
- 笨方法呢——去本地打开主文件夹，打开隐藏文件夹~/.ssh，打开生成的 文件 ：~/.ssh/github.pub 中可以找打它。
- 按官方指导在网页github添加刚才复制出的sshkey 保存后，回到本地终端使用：ssh -T git@github.com 登录，按提示输入 yes 即可成功
- 参考：https://help.github.com/articles/generating-ssh-keys/