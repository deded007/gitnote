
+ git extention記錄密碼

win+r，在运行中输入：%USERPROFILE%
找到其中的.gitconfig文件，找到
[credential]
 helper = store

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


+ 更新現在的分支

>git merge --no-ff "upstream/[branchname]"

>git pull --rebase upstream [branchname]

--

+ 合併分支

>git rebase upstream/[branchname]

盡量用這個，與主線常同步更新

>git merge --no-ff "upstream/[branchname]"

二條線差異很大，衝突很大時用這個

--

+ 捉全部的remote repository

>git fetch --all

--


G   H   I   J
 \ /     \ /
  D   E   F
   \  |  / \
    \ | /   |
     \|/    |
      B     C
       \   /
        \ /
         A
A =      = A^0
B = A^   = A^1     = A~1
C = A^2  = A^2
D = A^^  = A^1^1   = A~2
E = B^2  = A^^2
F = B^3  = A^^3
G = A^^^ = A^1^1^1 = A~3
H = D^2  = B^^2    = A^^^2  = A~2^2
I = F^   = B^3^    = A^^3^
J = F^2  = B^3^2   = A^^3^2
