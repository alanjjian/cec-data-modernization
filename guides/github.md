---
title: Foundations of Git and GitHub
layout: default
nav_order: 2
---

# Foundations of Git and GitHub

**Author**: Alan Jian

Credit given where credit’s due: this reading guide is heavily inspired by the CS61B course taught at UC Berkeley. Many of the readings will come directly from the first few labs/lectures, so if you’re curious about learning more about software development (and data structures), feel free to peruse the [course website](https://sp25.datastructur.es/)! 

## What is Git and GitHub? And why should I use this guide over others? 

First things first: this guide is about two different technologies:  

- **Git**: a version control system (VCS). Think of this like a super-powered save button that works across directories on all kinds of files.
- **GitHub**: a cloud-based platform (and company) that makes the files stored in Git shareable to a team. They also provide all sorts of services for a fee, sort of like Amazon Web Services  

While most quick start guides out there give you a good feel for how to get started with staging, committing, and pushing changes, few of them actually give you a good sense of the *internal graph structure* of Git and industry standard practices around these tools. I cannot stress this enough: **developing a strong baseline understanding of Git internals is key to leveraging this technology to reduce staff hours**. Without it, our knowledge will become fragile: automations, pull requests, protected branches, and other tools that are essential to our work require the foundational understanding that most guides omit for simplicity.

## Understanding Version Control Systems (VCS) 

Before we hit the ground running, skim (or read, depends on how interested you are) **Sections 1.1-1.4** of [*Pro Git* by Scott Chacon and Ben Straub](https://git-scm.com/book/en/v2). This book is an officially endorsed guide and the only one that is featured and hosted right on the official git website! 

The idea here is to get the general *software engineering* context from which Git arises. Notice those two figures (Figure 4 and Figure 5) in **Section 1.3**. That first figure should remind you of a storage solution that we already use (hint: it starts with “Share” and ends with “Point”). Each Excel Workbook, Word Document, PowerPoint, etc. keeps track of its own version history, with no context for how the overall project is moving.

In contrast, in Figure 5, it’s almost as if the project itself has a GIANT save button that allows you to tie file changes together under one unified naming scheme. This shift in perspective is pretty important for both programmers and knowledge workers: in many cases, we care more about the unified product/deliverable rather than the individual file versions.

Take, for example, our work on the IEPR. For most teams with models, we create and iterate upon models that exist across multiple files. With Git, we can navigate to a specific model run, and essentially turn back time, seeing exactly what every contributing script, input, and config file looked like exactly at run time. That means that we no longer have to guess what files looked like during each model run or create separate folders for each run; we can access that snapshot with one click!


