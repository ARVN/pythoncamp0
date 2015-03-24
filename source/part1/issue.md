##问题/备注清单

### UBUNTU 里笨办法搞定git SSHkey
-  使用本地终端 输入命令： sudo apt-get install git ，安装git
- 再者你已经创建了github帐号了，也知道哪里填SSHkey，只是还不知道key从哪里来，哪里来呢，本地终端告诉你：在我这里。
- 使用本地终端的SSH 命令 ：ssh -T git@github.com 尝试呼叫（链接） github 的ssh服务器，被拒绝（太苦了它告诉你）：Permission denied (publickey).
- 使用本地终端SSH 命令 ：ssh-keygen -C "yourname@yourcompany.com" -f ~/.ssh/github ，它能生成sshkey，被保存在~/.ssh/github.pub 里。
    - 还有两步要补上！
    - 输入终端命令：eval "$(ssh-agent -s)" 确保终端能使用生成的key;
    - 并使用终端命令： ssh-add ~/.ssh/github.pub 加载进本地文件
- 剩下的是笨方法：去本地打开主文件夹，打开隐藏文件夹~/.ssh，打开生成的 文件 ：~/.ssh/github.pub 中可以找打它。
- 按官方指导在网页github添加刚才复制出的sshkey 保存后，回到本地终端使用：ssh -T git@github.com 登录，按提示输入 yes 即可成功

- 参考：https://help.github.com/articles/generating-ssh-keys/
 
 
###别名
2015-3-18
- 别名的问题，通过别名来指代库链接
	+ git remote add origin git@github.com:ARVN/omooc.py
	+ 其中origin 是git@fichu.com:ARVN/omooc.py 这个库链接的别名/。
- 别名可以任意制定，一个别名对应一个库
	+ git remote add gitbook https;//git.gitbook.com/arvn/omooc.py.git
	+ 其中gitbook 是URL https://git.gitbook.com/arvn/omooc.py.git 的别名 
	+ 而 git remote add origin git@github.com:ARVN/omooc.py 
	+ 其中origin 是git@fichu.com:ARVN/omooc.py 这个库链接的别名/。
- 别名在push/pull 时候减少输入的URL 的次数。
- 明白别名代表URL库的意义后，也减少误解的发生——免得在每次push的时候都遇到 repo不存在的错误显示






###  
