# Merge v.s. Rebase

以下簡單介紹 merge 與 rebase 的比較/差異/適當使用時機。

## Merge

    $ ## 在 master 上，要合併 develop
    $ git merge develop


## Rebase

    $ ## 在 master 上，要合併 develop
    $ git rebase develop


## Differences


- [Git rebase 和 merge 合併操作示範錄影 | ihower](https://ihower.tw/blog/archives/6704)
- [使用 git rebase 避免無謂的 merge | ihower](https://ihower.tw/blog/archives/3843)
- [6.4 Git 工具 - 重寫歷史](http://git-scm.com/book/zh-tw/v1/Git-%E5%B7%A5%E5%85%B7-%E9%87%8D%E5%AF%AB%E6%AD%B7%E5%8F%B2)
- [Merging vs. Rebasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing/)

Merge: generate new commit. unavoidable.

Rebase: no more new commit log. 不照時間排序


|  | Rebase | Merge |
|--|--|
| 摘要 | 若有 conflict ，依照每一個 commit 解。在非主分支上使用 | conflict 一次秀 |


## Conclusion 結論

1. [使用 git rebase 避免無謂的 merge | ihower](https://ihower.tw/blog/archives/3843)

> 所以到底何時該用 merge? 何時可以 rebase?
>
> - 如果你修改比較多，預期會有較多的 conflict，建議用 merge (不過，如果是多次大範圍的主題式修改，那是不是應該一開始就多開一個 branch 來做呢?)。
>
> - 如果修改範圍較小，不太預期有 conflict，則建議可以加上 rebase 參數。


2.

> 自己的 branch 先 rebase master branch and test again before creating new Pull Request
>
> -- AppleBoy 吳柏毅
