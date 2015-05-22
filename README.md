http://git-scm.com/book/zh-tw/v1/

+ 二個版本特定檔案的差異

用difftool 後面接sha1:檔案路徑 git difftool old:path new:path
>git difftool Orgv1:Layouts/website/templates/org/detail.html Orgv2:Layouts/website/templates/org/detail.html AccupassV3

--


+ 加入標籤

輕量級標籤
>git tag [tagname]

含附註標籤
>git tag -a [tagname] -m 'my version 1.4'

--


+ 分享標籤

>git push origin [tagname]

--


+更新現在的分支

>git merge --no-ff "upstream/[branchname]"
>git pull --rebase upstream [branchname]

--



