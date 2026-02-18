---
title: Git Basics
layout: default
parent: Foundations of Git and GitHub
nav_order: 1
---

# Git Basics

**Author**: Alan Jian

## Getting Set Up

If some of y’all read ahead to [Section 1.5](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), you’ll notice that this is the setup section! We’re going to skip it. This book is designed for software engineers to develop a deep understanding of Git, so it skims over important setup details, assuming that the reader can fill in the blanks. Instead, we’ll bounce over to the resources from CS61B, my old intro course from Berkeley (Go Bears!), since it eases students more gently into setting up Git and GitHub. Go ahead and follow the directions in [this link](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to get Git and Git Bash setup on your computer. 

{: .note }
If you’re still feeling a little uncomfy around the terminal, you can use [this reference](https://sp25.datastructur.es/labs/lab01/terminal/) to help you navigate!

Once you’re done, we’ll also need to set up GitHub and connect your local git setup to your GitHub account. Start by navigating to the [GitHub website](https://github.com/), and sign up for an account. Once you’re done, navigate to your Git Bash, and use the following commands to set up your account: 

``` bash
git config --global user.name "<your name>" 
git config --global user.email "<your email>" 
```

## Getting Hands on with Git

Now, let’s move to [chapter 2 of the *Pro Git* book](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). Before you start reading, once again just be aware that these chapters are somewhat dense, and are built for folks who already have some familiarity with programming. You’ll want to bounce back and forth between this reading guide and the chapter to help guide your learning.

A few additional tips before you get started: 

- **Ask for help.** If googling, using AI, or mashing your head against the problem doesn’t get you unstuck, ask your co-workers for help! 
- **Don’t get bogged down by the details.** I’ll point out what you need to focus on and understand. The rest is optional! 
- **Follow along on your own computer.** Students often fall into the rabbit hole of skimming the code. I cannot stress this enough: try the code examples on your computer. Using Git (and the Terminal) is like a muscle; it needs training, and these examples teach you how to get strong! 

Ok ready? Now, go ahead and read Section 2.1 in its entirety, and follow these steps: 

- While you read this section, set up your first repository. You’ll need it for later chapters! 
- When you read the Cloning an Existing Repo section, you can try this with an existing repo that you have access to, but you don’t necessarily have to worry about it.

Once you’re done, read Section 2.2, and follow these steps: 

- Read **Recording Changes to the Repository**: 
  - In that first sentence, having a “checkout or working copy of all of its files in front of you” basically means you’re either
    - Looking at the repository in your file directory
    - Looking at the repository from inside your IDE (like PyCharm, or VSCode, etc.) 
  - This diagram (Figure 8) is a really handy way of representing how the work-flow of Git works: starting from the left-most side of the diagram, trace along the arrows, going from Untracked -> Staged -> Unmodified -> Modified -> Staged.
- Read up to, but not including **Short Status**:
  - If you’re not comfortable following along using a generic README file, you can try it by creating a generic word document. If you do this, make sure the word document is closed! Office 365 apps create weird temp files (they start with tildes) to manage access, and that might confuse you early on! 
  - As you read, think about the diagram you saw earlier (Figure 8), and pay attention to which git commands correspond with which arrow.
- Skip **Short Status**, and skim **Ignoring Files**:
  -  While you’re reading, think of the kinds of temporary files that you might be interested in leaving out of your repository: 
    - `~...xlsx` files are temporary files for Office 365 that just prevent other apps from simultaneously accessing your file.
    - `.ipynb_checkpoints` are just autosaved versions of your current notebook.
    - `__pycache__` are just files meant to speed up python script runs.
  - Ignore the rules for patterns and just skim the stuff on globs. You can just google how to make `.gitignore` files later if you need them.
- Skip **Viewing Your Staged and Unstaged Changes**, and read **Committing Your Changes**
  - Now, don’t follow along with this example. Vim is a pretty crappy text editor, so to avoid using it, you can use the following command instead: 
    - `git commit -m “<your commit msg here>”`
  - The `-m` flag basically means “message”, and it reads whatever you put in quotes! That way, you don’t really need to touch Vim to create a commit!

Go ahead and **skip the rest of Section 2.2 and 2.3**; all you have to know is the `git log` command let’s you view the last few commits that you’ve made. You can always google the details later.

Before we move on, here are a few additional tips that I’ve found helpful in my Git learning journey: 

- Remember the **general workflow**: Instead of hitting “save”, every day, you should be: 
  - **Adding your files with `git add .`**: If you want to add everything in your directory (excluding things you’ve ignored) you can run `git add .` That additional dot represents everything in your current directory! 
  - **Committing your files** with `git commit -m “<your commit msg here>”`. 
- Commit early and often! This is like spamming the save button on important docs. Don’t let a power outage wipe away all your work! A big commit history is annoying, but lost work is a disaster!