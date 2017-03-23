---
title: make-static-blog-on-github-pages-from-scratch
date: 2017-03-22 14:35:04
tags:
---

## Procedure 
1. initiate a repo in github
2. hexo init
3. install dependency
4. set travis to auto deploy

<!--more-->

## install hexo
To install hexo, first we should install nodejs. On macOS, we could install npm with brew `brew install node`
then we should install hexo.
```bash
npm install -g hexo-cli
hexo init blog
cd blog
npm install
npm install hexo-deployer-git --save
```

choose a theme, here I recommend you take a look at hexo-next-theme, override necessary configuration in \_config.yml.
```bash
git submodule add https://github.com/iissnan/hexo-theme-next.git themes/next
```
Change theme config

## Push to GitHub
1. Create a github repo
2. git add origin `git remote add origin THE_URL_OF_GITHUB_REPO`
3. git push `git push -u origin master`

## Using travis to auto deploy
1. create a github token
2. encrypt your token in travis
3. write your own .travis.yml

## solve conflict of render engine between hexo and mathjax
```bash
npm uninstall hexo-renderer-marked --save
npm install hexo-renderer-kramed --save
```

## create a new post
```bash
hexo create [post] post
hexo generate
hexo deploy
hexo server # See the render result in localhost
```
