--------
layout:     post
title:      "我的Git配置备忘 "
subtitle:   "针对常用的git设置和操作，添加备忘录。持续更新..."
date:       2019年10月30日19点39分
author:     "Allan Cao"
header-img: "img/post-bg-2015.jpg"
tags:
    - Memo
--------

# Git备忘
## Git 连接到[github或码云](https://gitee.com/PHDWu/CASESM3D/tree/stable_master/)   

1. Git 全局设置

   `git config --global user.name "NAME" `


    `git config --global user.email "XXX@gmail.com"`


2. 创建 git 仓库:
    `mkdir myrepo`
    `cd myrepo`
    `git init`

3. 本地branch关联远程branch：
    `git commit -m "first commit"`
    `git remote add origin https://gitee.com/XXX/YYY.git`
    `git push -u origin master`(选定的分支)

    `git fetch`  

4. 其他命令

    `git add .`

    监控工作区的状态树，使用它会把工作时的所有变化提交到暂存区，包括文件内容修改(modified)以及新文件(new)

    `git commit -m "for init"`

     这个命令将处于中间状态的文件（暂存区的文件)提交到版本库中,这时才算真正完成了一次提交过程

    `git pull origin master --allow-unrelated-histories`

    取回远程主机某个分支的更新，再与本地的指定分支合并

    `git push --set-upstream origin dev`

    链接并push远程分支

    `git log -p [File name]` 

    查看文件修改

    `git merge dev`

    合并dev分支到当前分支（只是本地仓库操作，针对远程仓库需要再一次push）

    `git checkout dev`

    切换本地分支到dev

    `git branch -d testing `

    删除本地testing分支

    
    **5. 注意事项**

    **commit之前先pull，避免冲突。**

    比较文件夹：diff -urNa  D1 D2

    git diff HEAD^ ：查看pull下来的文件有那些具体的修改 

    git merge --abort : 退出合并    

    git merge -X ours/-X theirs testing：选择对于冲突的合并（哪个分支）

    find . -type f -exec dos2unix {} +    : 修改换行格式 Dos → Unix
    


> ## [相关Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)
​     
