# Git Challenge
There are two branches, `add-echo` and `add-reverse`. The goal of this challenge is to use `git rebase` to bring both commits onto master. When finished there should be no merge commits or branching. For example, `git log` on the `master` branch should look similar to this:
```
/challenge-git master
⚡ git log
61a2c67 feat: add reverse route (David Guttman, 7 minutes ago)
2c2c5d6 feat: add echo route (David Guttman, 10 minutes ago)
dcc4c0b docs: add more instructions (David Guttman, 11 minutes ago)
...
```
## Instructions
How to attempt this challenge:
1) Create a new repo in your account and note the git url
2) Clone this repo
3) Solve the challenge
4) Set your new repo as the origin: `git remote set-url origin ${your repo url}`
5) Push your solution to your repo
You must follow these steps for your solution to be accepted -- forks or other methods will not be considered.

```
## My solution.
git switch add-echo
git pull --rebase origin master
git rebase master
git push
merge with master

git switch add-reverse
git pull --rebase origin master
git rebase master
**resolve conflicts
git rebase --continue
git push
merge with master
```

##Result
```
git log
commit 2bd7712718712115a1527db2eb53321d06e11e19 (HEAD -> master)
Author: David Guttman <david@davidguttman.com>
Date:   Thu Oct 3 16:34:57 2019 -0700

    docs: add more instructions

commit 08d29e7151cdcaf519aae67bb4bffeb7593ed596
Author: David Guttman <david@davidguttman.com>
Date:   Thu Oct 3 16:34:47 2019 -0700

    chore: update deps

commit 744a0f1a5ca3566115320f62c23d76214566f7b5
Author: David Guttman <david@davidguttman.com>
Date:   Mon Mar 5 09:08:50 2018 -0800

    docs: update readme for git challenge

commit 6de04176b50911db13d6cf46d30e1e6b3629bcff
Author: David Guttman <david@davidguttman.com>
Date:   Wed Sep 20 16:11:45 2017 -0700

    fix: change db path to project folder (#21)

    closes #21

commit 8722c121965408c2dd9c76e8f9a73f54ba3f92b9
Author: David Guttman <david@davidguttman.com>
Date:   Wed Sep 20 16:08:56 2017 -0700
:...skipping...
commit 2bd7712718712115a1527db2eb53321d06e11e19 (HEAD -> master)
Author: David Guttman <david@davidguttman.com>
Date:   Thu Oct 3 16:34:57 2019 -0700

    docs: add more instructions

commit 08d29e7151cdcaf519aae67bb4bffeb7593ed596
Author: David Guttman <david@davidguttman.com>
Date:   Thu Oct 3 16:34:47 2019 -0700

    chore: update deps

commit 744a0f1a5ca3566115320f62c23d76214566f7b5
Author: David Guttman <david@davidguttman.com>
Date:   Mon Mar 5 09:08:50 2018 -0800

    docs: update readme for git challenge

commit 6de04176b50911db13d6cf46d30e1e6b3629bcff
Author: David Guttman <david@davidguttman.com>
Date:   Wed Sep 20 16:11:45 2017 -0700

    fix: change db path to project folder (#21)

    closes #21

commit 8722c121965408c2dd9c76e8f9a73f54ba3f92b9
Author: David Guttman <david@davidguttman.com>
Date:   Wed Sep 20 16:08:56 2017 -0700

    feat: log request auth info (#19)

    closes #19

commit 30cdbf2e2c57155f6f70225a3164b663ae18a6c5
Author: David Guttman <david@davidguttman.com>
Date:   Wed Sep 20 16:04:55 2017 -0700

    feat: add 401 status code for unauthorized requests (#17)

commit 3f2732dfc0ea3b0079fc542b609ed814b46b0766
Author: David Guttman <david@davidguttman.com>
Date:   Mon Sep 18 15:22:11 2017 -0700

    fix: remove extra dep check (#15)

commit 3c34209a6c838e306ff0dc6c31edc4a946f9049f
Author: David Guttman <david@davidguttman.com>
Date:   Mon Sep 18 15:13:22 2017 -0700

    feat: add authorization to model endpoints (#13)

commit 09e0d04a629bad8f565e4db2a45c5d66a90d61b1
Author: David Guttman <david@davidguttman.com>
Date:   Mon Sep 18 14:46:13 2017 -0700

    feat: add CORS support (#11)

commit d31a12829b1655c9178f3b81309842f64ef8605c
Author: David Guttman <david@davidguttman.com>
Date:   Mon Sep 18 14:37:04 2017 -0700
```
