+++
title = "Git branching with submodules."
date = 2023-06-21T00:00:00+05:30
layout = ""
linkTitle = ""
markup = ""
slug = ""
tags = ["git"]
type = "post"
url = ""
draft = false
+++

## Branching issue with git and submodule {#branching-issue-with-git-and-submodule}

Having submodule many times when I create branches it is much better option if all the submodule will have same branch.

To create a branch for all the submodules in a Git repository and ensure they are synced with the newly created branch, I follow these steps:


### Create branch {#create-branch}

{{< highlight shell >}}
git checkout -b <new-branch-name>
{{< /highlight >}}


### Use git foreach command {#use-git-foreach-command}

{{< highlight nil >}}
git submodule foreach 'git checkout -b <new-branch-name>'
{{< /highlight >}}

This command iterates over each submodule using `git submodule foreach` and executes the `git checkout -b` command to create the new branch within each submodule.


### Push the new branch to the remote repository: {#push-the-new-branch-to-the-remote-repository}

{{< highlight shell >}}
git push origin <new-branch-name>
{{< /highlight >}}

This command pushes the new branch to the remote repository, ensuring it is available for syncing with other collaborators.


### Update and sync the submodules with the new branch: {#update-and-sync-the-submodules-with-the-new-branch}

{{< highlight shell >}}
git submodule update --remote --recursive
{{< /highlight >}}

This command updates the submodules to the latest commit on the new branch and ensures they are in sync with the repository.


#### References {#references}

Git documentation: <https://git-scm.com/doc>

