# Toolkits
常用命令,工具使用方式的集合

## genSSHKey
一键生成各个端的sshkey
```bash
# window
ssh-keygen -t rsa -C "1619249966@qq.com"
cat C:\Users\dongn\.ssh\id_rsa.pub
# ubuntu
ssh-keygen -t rsa -C "1619249966@qq.com"
cat /home/niudong/.ssh/id_rsa.pub
```

## git http2ssh
将git的上传方式从http转成ssh
```bash
# config info 
git config --global user.name "Niudong-ubuntu"
git config --global user.email "1619249966@qq.com"
# change config(.git/config)
url = http://xxx.com/Name/project.git -> url = git@xxx.com/Name/project.git
```

## submodule
git子仓库操作
```bash
# load submodule
git clone <仓库地址> --recursive  # 递归的方式克隆整个项目
git submodule update --init --recursive  # 初始化子仓库并更新
# add submodule
git submodule add <仓库地址> <本地路径>  # 添加子模块(git submodule)
# delete submodule
git rm the_submodule
rm -rf .git/modules/the_submodule
```

## keep fork up to date
```bash
# in fork dir
git remote add upstream <原版仓库地址>
git pull upstream master
git push origin master
```
