# 添加 config 配置文件

## 文件内容如下 在用户.ssh 下

## gitee

Host gitee.com
HostName gitee.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa_gitee

## github

Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa_github

## 验证是否成功

ssh -T git@github.com
ssh -T git@gitee.com

## clone 不同仓库代码

git@github.com:用户名/项目名.git
git@gitee.com:用户名/项目名.git

## 同时 push

修改 .get 文件下 config 文件
[remote "origin"]
url = git@gitee.com:Yedai*YY/项目名称.git
url = git@github.com:Ye-dai-GitHub/项目名称.git
fetch = +refs/heads/*:refs/remotes/origin/\*
