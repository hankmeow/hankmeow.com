# 使用命令

## macOS本地环境搭建



## 项目拉取
```shell
git clone --recursive git@github.com:hankmeow/hankmeow.github.io.git  #recursive参数是为了下载./themes/hugo-theme-next子模块

git fetch --all #更新
git checkout -b gh-pages origin/gh-pages #拉取远端的部署分支到本地

git checkout main #切回开发分支
```

## hugo-theme-next依赖更新
```shell
cd ./themes/hugo-theme-next #进入主题的目录
git fetch --all #更新
git tag #显示所有tag
git checkout vXX.XX.XX #切换到指定tag
cd ../../ #返回项目目录
git add ./themes/hugo-theme-next #暂存主题变动
git commit -am "update hugo-theme-next version" #保存变动
git push #推送到远端
```

## 部署 （也可以由github page flow自动处理）
```shell
git add . #暂存
git commit -am "xxx" #保存
git fetch --all #更新
git checkout gh-pages #切换到部署分支
git branch #查看是否切换成功
hugo #构建
git add . #暂存
git commit -am "xxx" #保存
git push #推送
git checkout main #切换开发分支
```