# Our Coding Flow

We follow a PR-Based coding flow. \
It's based on a "feature-branch git flow", similar to what is described in [this article](https://nvie.com/posts/a-successful-git-branching-model/))

We know this PR-based flow might be confusing to newcomers. \
But as you get used to it, it turns out it helps you organise your work, and greatly improves our code quality. 

## The Flow in Brief

1. The Developer work on a /feature/branch and open a PR for it
2. The Developer ensure the PR is Ready to Be Reviewed
3. The Developer ask for a Review
4. The Reviewer reviews it
5. The Developer tackles needed changes
6. The Reviewer approves it
7. The Developer merge and close the PR.

## The Flow in Detail

### Start a New Feature

To start working on a new feature : 

- [Clone or create the repository](./NewProject.md)
- Create a new branch named **feature/my-feature**
- Commit and push the first commit on this branch
- Start a Pull Request from **feature/my-feature** to **develop**.

You should name it "[WIP] My Feature" (for _Work In Progress_), so that others know your work is not ready to be reviewed yet.

On every commit, the CI will test and deploy your code. 
On the description of the PR, the CI will give you a link to a prod-like deployment of your code that you can share with anybody, as well as a few useful reports : 

<img width="763" alt="CleanShot 2020-03-06 at 12 19 06@2x" src="https://user-images.githubusercontent.com/4315469/76079358-c43f9d00-5fa4-11ea-80a7-fc6b9d6cb818.png">

You can simultaneously work on multiple feature : create as many features branch and PR as you will. 
We love "thin" PR : avoid touching hundreds of files in a single PR.

### The Review Process

A PR is ready to be reviewed when :
- The work needed on the feature is done : the feature works completely, you've tested it, and it's nice and shiny
- It's "Green" : All the automated tests passed successfully. 

Once the PR is ready to be reviewed :
- Remove  "[WIP]" from the title
- Request a Reviewer : You've been assigned a Pair-Reviewer on the project, assign her. You can assign the Project Manager for a functionnal review as well. 

![image](https://user-images.githubusercontent.com/4315469/76079861-e84fae00-5fa5-11ea-906b-b2f3a2de7833.png)

Once the PR is approved, the Developer merges it. 

On to the next one ! 






