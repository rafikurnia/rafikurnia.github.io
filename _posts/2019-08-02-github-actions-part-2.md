---
title: "GitHub Actions Part 2 - main.workflow"
tags: [github-actions]
layout: post
excerpt_separator: <!--more-->
published: true
---

Have you read my first post about GitHub Actions?  
<!--more-->
You may want to read that first before reading this page ;)  
Here it is: [GitHub Actions Part 1 - Introduction (August 1, 2019)]({{absolute_url}}/2019/08/01/github-actions.html)

Before we continue, I forgot to mention in the previous post that by the time I write this page,  
***GitHub Actions is still in Beta stage***.
You can sign up for the beta program: [https://github.com/features/actions/signup/](https://github.com/features/actions/signup/).  
I signed up for [my personal account](http://github.com/rafikurnia) around 1 month ago, but have not got any response yet.

Fortunately, [my organization account](http://github.com/traveloka) has this feature enabled!  
So I can play around with it and share to you through this post..

---

So let's continue!

I was playing around with GitHub Actions to automatically add newly created Issue and Pull Request to a [GitHub Project](https://github.com/features/project-management/) board.
To define the workflow, you can create a `main.workflow` file inside `.github` directory. The directory is in the root.


Here is how the file looks like:

```
workflow "Add new pull requests to projects" {
  resolves = ["adding the pull request to a project"]
  on = "pull_request"
}

action "adding the pull request to a project" {
  uses = "alex-page/add-new-pulls-project@v0.0.4"
  args = ["Curated Terraform Modules", "In progress"]
  secrets = ["GITHUB_TOKEN", "GH_PAT"]
}

workflow "Add new issues to projects" {
  resolves = ["adding the issue to a project"]
  on = "issues"
}

action "adding the issue to a project" {
  uses = "alex-page/add-new-issue-project@v0.0.4"
  args = ["Curated Terraform Modules", "To do"]
  secrets = ["GITHUB_TOKEN", "GH_PAT"]
}
```

If you notice, there are 2 workflows defined there. Also one action for each workflow.

> Next Posts: 
> - [GitHub Actions The Last Part - HCL Template is deprecated (November 28, 2019)]({{absolute_url}}/2019/11/28/github-actions-the-last-part.html)
