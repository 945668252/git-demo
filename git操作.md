# 工作需求

## 初始化仓库后，只有一个master，如何创建dev？

创建dev，并切换到dev

```
git checkout -b dev
```

连接远程仓库，origin是仓库地址

```
git push origin dev
```



# 看别人的操作

项目开始执行流程 
git branch -a (查看所有分支) 
0、克隆代码 git clone 地址 
1、拉取线上 master 最新代码: git pull origin master 
2、切换到开发分支: git checkout dev 
3、合并 master 本地分支（master）: git merge master 
4、开始开发 
5、开发结束 
6、查看当前文件更改状态: git status 
7、把所有更改代码放到缓存区: git add -A 
8、查看当前文件更改状态 : git status 
9、缓存区内容添加到仓库中: git commit -m '本次更改注释' 
10、把代码传到 gitLab 上: git push origin dev 
11、若代码到达上线标准则合并代码到 master,切换分支到 master: git checkout master 
12、拉取 master 最新分支: git pull origin master 
13、合并分支代码到 master(若有冲突则解决冲突): git merge dev 
14、把当前代码上传到 gitLab: git push origin master 
15、代码上线后，用 tag 标签标记发布结点(命名规则：prod_+版本_+上线日期) 
git tag -a prod_V2.1.8_20200701
16、tag 标签推到 gitLab 
git push origin prod_V2.1.8_20200701 