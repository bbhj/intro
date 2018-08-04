如何参与贡献:
========================

- Github 提交 PR, 地址: github.com/airdb/docs
- Github 提交 issues, 地址: github.com/airdb/docs/issues
- 写邮件给 info@airdb.com

Github 如何提交 PR
========================

- step 1:

  Fork GitHub 上的 Repository 到贡献者的 Repository

- step 2:

  clone 代码到本地 git clone github.com/airdb/docs

- step 3:

  检查当前 Git Repository

    git remote  -v
    origin    https://github.com/airdb/docs (fetch)
    origin    https://github.com/airdb/docs (push)

- step 4:

  新建立贡献者 Git Repository 的连接

    git remote add pullrequest https://github.com/deanchina/docs

- step 5:

  新建工作分支

    git checkout -b devel

    git branch
    * devel
      master

- step 6:

  修改文件

- step 7:

  提交到贡献者 Github 上

    git add .
    git commit -m"pull request"

- step 8

  发起 PR (Pull Request)
  登录 GitHub Repository 点击Pull Requests, 再点击New pull requests按钮
