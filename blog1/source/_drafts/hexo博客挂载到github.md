---
title: hexo博客挂载到github pages
tags:
---
# 1.按照**github pages**的[官方文档](https://docs.github.com/en/pages)教程建立自己的github网站。
# 2.按照**hexo**的[官方文档](https://hexo.io/zh-cn/docs/)安装hexo。
# 3.重点来了，如何将hexo生成的静态网页自动推到github上？(有坑)
- 安装插件hexo-deployer-git:
```
npm install --save hexo-deployer-git
```
- 修改blog根目录里的_config.yml文件:（有坑）

网上教程需要修改
```
deploy:
  type: git
  repo: your git website repository
  branch: your branch
```
实测还需要修改
```
url: website
root: your webstie root
```
修改完成执行命令即可
```
hexo clean 
hexo g 
hexo d
```