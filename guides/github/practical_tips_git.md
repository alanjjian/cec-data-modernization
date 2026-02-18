---
title: Putting it in Practice
layout: default
parent: Foundations of Git and GitHub
nav_order: 4
---

# Putting it in Practice

Congrats! You are now ready to begin your Git and GitHub journey! There is so much still out there to explore in this world of version control: as I alluded to, this guide is a wonderful jumping off point for learning how to use powerful features of GitHub, like GitHub Actions to automate your work, or GitHub Pages to generate websites/documentation for projects. 

Before you go, let’s just talk real quick about a few quick and dirty lessons, resources, and thoughts that aren’t all that easy to fit into the rest of the guide.

## Day-to-Day Workflow

So, let’s put everything we just learned together into a practical workflow! When I start working on a new feature: 

1. **Checkout the `dev` branch**: So my work begins from the correct place.
2. **Pull changes from the repo**: This means I get the most up-to-date version of our code base.
3. **Create a branch with a descriptive name**: This is our `feature` branch that will contain the changes that I want to make. 
4. **Work on, stage, and commit my changes**: This creates a record of the changes that I’ve made. Repeat this step every day until completion! 
5. **Merge `dev` into my feature branch**: this allows me to reconcile differences between `dev` and my feature branch (in case others have pushed to `dev` after I started this feature branch).
6. **Merge my feature branch back into `dev`**: Once I’m finished, I push them back into `dev` and wrap it up.

Once we collect up all the big changes that we want to make to our model, and we’re ready for a real model run, we can then 

1. **Create a pull request from `dev` into `main`**: this is when we finalize, discuss, and double check the work of all collaborators, and an official way to ensure that everyone gets their eyes on the version. 
2. **Accept and Merge `dev` into `main`**: Once everyone agrees on the changes, it goes into main, and is accepted as part of our official record of changes.

## Additional Resources

Beyond the [Pro Git](https://git-scm.com/book/en/v2) textbook, here are a few other resources that you might find useful!

- [Git Cheat Sheet](https://git-scm.com/cheat-sheet): a handy reference to help jog your memory about commands you should know. 
- [GitHub Docs](https://docs.github.com/en): if you want to learn more about the features available to us in GitHub, this is the best place to learn more! 
- [Git Large File Storage](https://git-lfs.com/): while we shouldn’t be storing data in GitHub, sometimes storing large files are unavoidable. That’s where Git LFS comes in! 
- [Hackers Guide to Git](https://wildlyinaccurate.com/a-hackers-guide-to-git/#repositories): a hackier version of the same Pro Git textbook that we used that focused primarily on functions in Git that were outside the scope of this guide. 