---
title: Collaboration via GitHub and Git-Flow
layout: default
parent: Foundations of Git and GitHub
nav_order: 3
---

# Collaboration via GitHub and Git-Flow

Now that you have a solid understanding of git’s internal representation, it’s time to discuss **how we can leverage it to superpower our work**. It’s time to talk fold in GitHub, and talk about how Git and GitHub facilitate collaboration.

First, let’s talk GitHub. We’ll skip straight to [Section 5.1](https://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows), and just **read everything up to and including “Centralized Workflow”**.

Now that you finished reading that bit, let me fold in some context, since we’re skipping super far. Right at the start of this reading guide, I provided a definition for Git and GitHub:

- **Git:** a version control system (VCS). Think of this like a super-powered save button that works across directories on all kinds of files.
- **GitHub:** a cloud-based platform (and company) that makes the files stored in Git shareable to a team. They also provide all sorts of services for a fee, sort of like Amazon Web Services.

So far, everything that we’ve discussed is just about **Git**. All of the branching, committing, etc. is about learning how to use this VCS. But now that we have this wonderful representation, we have to figure out how to get it onto our co-workers computers. How do we share and contribute to the same project? 

That’s where **GitHub** comes in. Instead of worrying about getting “…a remote Git repository set up as a focal point for all the developers to share their code”, we can just get a GitHub account and let them do the work for us (this is why we can skip all of **Chapter 4**)!

Take a look at Figure 53. Essentially, GitHub functions as our **shared repository**, and a **source of ground truth**. In other words, it holds the canonical graph representation of our project on the cloud (a.k.a in a server). We can pull the most up-to-date work from our GitHub repository into our own local repositories, and once we make commits and other changes to the project, we push those updates back up to GitHub and update the version control graph so that our co-workers can pull our new changes. 

The question now is: **How do we get our local repository to push/pull to the right shared repository?**

## Working with Shared Repositories in GitHub 

Now, **go back and read [Section 2.5](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)**. There are tons of details here that you can kind of skim, but pay attention to the following details:  

- A **remote repository** (also just called a **remote**) is a version of your project that is hosted on the internet or a network somewhere.
- When you clone a shared repository on GitHub, that shared repository is called the **origin** of your local repository by default.
- When you clone a repository, your **origin** is added as a **remote** by default. 
- `git pull` is just a combination of `git fetch` and `git merge`. In practice, just about **everyone solely relies on `git pull`; You’ll basically never run `git fetch`**. 
- When a local branch is setup to "track" a remote branch, running `git push` and `git pull` on your local branch automatically assumes you’re pushing and pulling to the remote branch

## Git-Flow: A Collaborative Approach to Branch Workflows

Now that you understand shared repositories, GitHub, and git branching, now we can pull it all together, and talk branch workflows, and best practices. 

Remember [Section 3.4](https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows)? Now that we have some context on how shared repositories work, we also have to consider how our branching workflows should change to facilitate collaboration. 

hankfully, this is a solved problem! **Git-Flow** has been an industry standard for over a decade now, and it’s key to understanding how workflow collaboration is organized. **Go ahead now and [read the blog post that popularized/formalized this model](https://nvie.com/posts/a-successful-git-branching-model/), SKIPPING the RELEASE and HOTFIX BRANCHES sections.**

Notice how the Git-Flow model evolves from the notions offered in [Section 3.4 of *Pro Git*](https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows). Long-running branches offer a *protected source of truth* with progressively diminishing stability (i.e `main` and `develop`), with topic/feature branches stemming from `develop` that *nicely silos work, preventing merge conflicts*.

For the purposes of most teams at the CEC, it’s likely that you don’t need all the bells and whistles on display here. For example, for TEFU’s on-road freight model, we’re using a slightly simplified version of this process; essentially, since we’re not serving a web app or anything crazy, we can omit the hotfix and release branches. The two parallel “develop” (usually shortened to “dev”) and “master” (now called “main” to avoid problematic language) branches form the core of our development model, with feature branches being the ones that we directly iterate and work on.

## GitHub as a Platform for Collaboration: Pull Requests 

Phew! That was a lot of information that we just covered. Just one final thing to cover, now that we’re all caught up on the foundations of Git and GitHub! Beyond just hosting our repositories, GitHub is actually a *platform* that has tons of additional features and functionality that can help improve our work. Things like GitHub Actions to automate script running, GitHub Pages to automagically create websites for your project directories, and so much more! 

We’ll close with one last (extremely important!) feature that you need to know about: the **pull request**, or **PR** for short. Now you’re gonna laugh when I tell you what this is: **a pull request is a formal request made through GitHub to merge two branches of your repository**. That’s it! And it’s so easy to make too; to learn more about how to create one, let’s read through GitHub’s [Creating a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) doc.

So why should we care? In a word: collaboration. We’ve talked at length in the last section about the importance of the main branch. It’s the *protected source of truth*, the heart of your project! **If you make changes to your code, you had better check it with a co-worker before you merge to main!** 

This is what makes pull requests so special: it facilitates/enforces communication about changes to your code. For important merges, like when you take your development branch and merge to main, the rest of your team should at least have a chance to review the work before it gets officially incorporated into your final process/model!