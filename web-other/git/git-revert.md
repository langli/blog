# revert 还原操作
revert是撤销某次提交，但是这次撤销也会作为一次提交进行保存(这样就不会丢失原来修改过，但是没有提交的内容？)。
```bash
$ git revert 83281a8e9aa1ede58d51a6dd78d5414dd9bc8548 还原提交 对应的id //作为一次新的修改需重新提交
$ git show 83281a8e9aa1ede58d51a6dd78d5414dd9bc8548 查提交类型, 合并或者普通提交
$ git revert -m
$ git revert f138976 // 撤销f138976提交，并生成一份新的提交记录(会自动提交 commit)
$ git revert -n f138976 // 撤销f138976提交，不自动提交
```
#
