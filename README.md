# Git Push Action

A Github Action to push code to git, like [`gitpage`](https://pages.github.com/).

## Environment Variables

- GITHUB_EMAIL: git user email
- GITHUB_USERNAME: git user username
- PUBLISH_REPO: repo url, `https://${{ secrets.GitHub_PAT }}@github.com/owner/repo.git`
- PUBLISH_BRANCH: git branch
- PUBLISH_DIR: dir to publish

## Secrets

- DEPLOY_PRIVATE_KEY: Required your deploy key which has Write access[not use]

## How to Use

```
    - name: Git Push Action For Coding Page
      uses: AnonyStar/git-push@v2
      env:
        GITHUB_EMAIL: "me@xiexianbin.cn"
        GITHUB_USERNAME: "xiexianbin"
        PUBLISH_REPO: https://${{ secrets.GitHub_PAT }}@github.com/owner/repo.git
        PUBLISH_BRANCH: gh-pages
        PUBLISH_DIR: ./public
        # DEPLOY_PRIVATE_KEY: ${{ secrets.DEPLOY_PRIVATE_KEY }}
```
