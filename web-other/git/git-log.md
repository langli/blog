# log日志
---
## `git log`命令显示从最近到最远的提交日志
```bash
$ git log --pretty=oneline // 单行显示日志
$ git log --oneline // 单行显示日志(简写id)
$ git config --global alias.lgone "log --oneline"
$ git log --abbrev-commit # 简写ID
$ git log --stat # 列出各个版本间的改动及行数
$ git log --stat -n #(-n,-1,-2 需要显示的条目数量) // 显示简要的增改行数统计
$ git log -p -n # 展开显示每次提交的内容差异
$ git log  --author=Ivan  # 查找指定作者的日志

```
查看 git log 后退出 -> 直接输入: `q`

### 查看提交历史，设置样式并增加别名
```bash
$ git log
$ git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --stat"   // 定义历史记录格式的别名, 以后只需 git lg 即可
$ git lg  // 使用上面的别名
$ git lg -5 // 只显示5条提交记录
```

### git log 指定日期
```git
<!-- 在指定日期以前的提交记录，前30条记录 -->
$ git log --until=2015-11-20 -30  
$ git log --before=2015-11-20 -30  
```
```git
<!-- 在指定日期以后的提交记录 从今天开始显示，前30条记录  -->
$ git log --since=2015-11-20 -30  
$ git log --after=2015-11-20 -30

<!-- 日期倒序排列 从2015-11-20开始显示，前30条记录 -->
$ git log --reverse --since=2015-11-20 -30
$ git log --pretty=oneline --reverse --since=2015-11-20  // 单行并倒序显示

```
### 指定ID号查看日志
```bash
$ git lgone 108de63 --stat
$ git lg 108de63 --stat
```
### 查看指定文件的log
```bash
$ git log -- branches/webapp/v1.1/html/new/app/view/goodsDetails.js
```
### 综合应用
```bash
$ git log --reverse --stat --since=2015-11-20 --abbrev-commit  # 从2015-11-19以后的所有记录倒序排列并缩写ID
$ git lg --stat --since=2015-11-19 --until=2015-11-20  # 从2015-11-19 到 2015-11-20的提交记录
$ git lgone --stat --after=2015-11-19 --before=2015-11-20  # 从2015-11-19 到 2015-11-20的提交记录 同上
```
### 重定向输出内容
```bash
git log >> log.txt
```
