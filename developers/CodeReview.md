# A flow for PR review

**note:** The following assumes a "feature-branch git flow" (simillar to what is described in [this article](https://nvie.com/posts/a-successful-git-branching-model/))

## Starting a new feature branch

Once you made your first commit to your new feature branch, push it to the remote and start a "WIP" PR.  
WIP stands for Work In Progress.   
This lets others (product owner, project manager, reviewer ...) know that this work isn't ready yet, but that it exists and is in progress.

**Prefix the title of your PR with `[!WIP!]`** to make this clear.  
e.g. for a PR from the branch `feature/add-new-form-fields` into the main branch  
"`[!WIP!] Add new form fields`"

**Assign a reviewer to your PR**

Ideally the main branch (master, or develop, or release-branch - depending on your exact flow) should be protected. This way accident can't happen (accidental push on a "main" branch).  

Whether or not it's the case, you should make sure your PR and feature-branch meet some requirements before it is ready to be merged.

### creating a PR
[Creating a PR on bitbucket](https://confluence.atlassian.com/bitbucket/create-a-pull-request-to-merge-your-change-774243413.html)
## Requirements
### green build

Ideally CI test should be run for every new commit pushed to a feature-branch concerned by an open PR towards the main branch.

**Keep the feature-branch that is concerned by a open PR always clean (lint, test, build should all be green).**

### Keeping your branch up to date with the PR's target branch

Creating a WIP PR soon in the development of your feature branch has several advantages.  
Besides allowing other to follow your progress, it will allow you to **monitor the conflict(s)** - if any - that could result in the attempt to merge your feature-branch in the target branch .


Visit the page of your PR regularly to monitor the ability of your feature-branch to be merge without conflict.
If you see conflicts you should solve those localy by merging the target branch in your feature-branch (do not forget to pull the target branch from the remote as the conflicts status displayed on the PR page is the result of what the remote knows about, not what you have locally on your machine, always make sure those are aligned).

Ask a colleague if you're not certain how to handle this.


**Keep the feature-branch that is concerned by a open PR always free of conflicts (should be ready to be merged in the target branch).**


### Readying your PR for review


Once you consider your new feature is ready and the feature-branch can be merged, **remove the [!WIP!] prefix** from the title of your PR.


#### Review process


Reviewer(s) will review and either "approve" or to "request changes".
They can also comment or ask question without requesting changes before approving the PR.


Once the PR has been approved and all the criteria for merging are met (conflict free, green build, reviewed and approved)

You can click the merge button and go celebrate the acceptance of your feature branch 🍾.


## How can I still work freely with all those crazy rules 🤔 ?`



Sometimes, lint rules and the app building without error becomes secondary, the first objectif is to have sometihng working.

In order for you to still be able to have some space in your work and save your changes on the remote without compromising your PR or triggering ci run you know would fail, you can work on what could be called a feature-feature-branch or a beta-feature-branch. (for a feature-branch named `feature/add-new-form-fields` for which you have started a PR, you can work a branch `feature/add-new-form-fields-beta`)

This way you can still save your work without worying about it being commented on in the open PR.

And since the feature-branch is not protected, you can decide when it is time to merge your beta-feature-branch back into your feature-branch and start getting the new code reviewed.

Try to work in small unit and keep the PR as up to date as possible on your beta-feature-branch if you are working on one.