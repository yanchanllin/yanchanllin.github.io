---
layout: post
title:      "Project Collaboration #2"
date:       2019-11-21 15:07:54 -0500
permalink:  project_collaboration_blog_ii
---


After you enter the right directory ready to make change to the project, for best practice setup another url call upstream that link to the origin repository from the group, once we make changes or updates someone elses contributions; merges got accepted. Then your repository will outdated because our commit history is different. We want to make sure everything is in sync with the original repository with the master branch. 

There are few ways to do that you can delete the fork and re-fork it; that can be one way. However, it's a bad idea with many gems installed or on the terminal "git remote add upstream git@github.com:yanchanllin/book-fellow-backend.git" this is an example for your collaboration project url. git remote -v will show the new upstream urls. 

Now you can pull from original group account by "git pull upstream master" to update your GitHub repository, then "git checkout -b demo_branch" to create a new branch for making code changes, after changes "git status", git add "  ", git commit -m"message", git push origin demo_branch (this is the branch you made changes in). 

Once you are done push that go back to your GitHub repository will see your created branch, go to that branch to click on "new pull request" to merge in with master.

