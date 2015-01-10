tryrproj
========

Basic experiments with R Studio projects and Git integration.

But not packrat, for now.

I added to github by git init locally, which RStudio can pick up, then by creating a repo of the same name on github and then setting its origin as explained in the github workflow.

```
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/philallen117/tryrproj.git
git push -u origin master
```
This is clunky.
I will try the github-first way again, next time.
My problem was convincing RStudio to accept an existing directory.
I wonder if touching any R file in that directory would be enough.

For pushing, RStudio seemed to be unhappy with name/password, so I

```
git remote set-url origin git@github.com:philallen117/tryrproj.git
```

RStudio picked up the ssh key by default, and pushed successfully, adding github to list of known hosts

I am sure I could have specified ssh when I first set the origin, or equally, when I clone in the github-first approach.
