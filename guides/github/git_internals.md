---
title: Git Internals
layout: default
parent: Foundations of Git and GitHub
nav_order: 2
---

# Understanding Git’s Internal Representation

So far, we’ve just discussed the basics of running and using git, but we haven’t really touched on the actual meat and potatoes of **git’s internal representation**. To do this, let’s walk through [Chapter 3](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) together.

Start by reading through the **introduction** and **Branches in a Nutshell**, stopping before **Creating a New Branch** in [Section 3.1](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell). This section is going to feature a few terms that you might have never seen before, so here’s a quick and dirty glossary to help you through it:

- **Pointer**: If our computers were a neighborhood with information stored in various houses, you can think of a pointer as an address! Pointers allow us to quickly pinpoint locations in our computer that we need access to.
- **Checksum (and SHA-1 hash)**: To dramatically simplify this concept, just think of a checksum as a unique name/label. When you “compute a checksum” for something, you generate a (almost statistically guaranteed) unique name for it.

{: .note}
you’ll notice that they use the default branch name of “master”. **This naming convention has a problematic history, so the standard name (at current time of writing) has been shifted to “main”.**

Now, go ahead and read through the rest of this section. By now, you should be comfortable with the **graph-based representation** of snapshots and pointers under the hood in Git. I cannot stress this enough: when you use Git, **it is not magic**. When you’re debugging issues, the terminal (and even the GitHub app itself) doesn’t always give great visualizations of what’s going on, so **it’s up to the user to have a clear mental model of how your repository looks under the hood**.

If you’ve been following along, you’ll also probably notice that checking out other branches seems to magically change your directory to the snapshot located at that pointer. Imagine that you were working on your model; if you came back to the project a year later, would you remember that your directory doesn’t represent your most up-to-date model? **Having a good mental model also helps you understand where you are within your version history.** It won’t always be obvious what branch, or version you’re at, and you could do serious damage to important processes.

Now, go to [Section 3.2](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) and finish up to **Basic Merge Conflicts**. This is where we get into the bread and butter of git: the merge function.

So what makes merging so integral to our workflow? It allows us to work on the same codebase at the same time. If I’m fixing an issue in one script, and you’re fixing an issue on another, merge allows us to seamlessly adopt both of our snapshots into one, fully updated commit.

But what happens, however, if we work on the same part of the code at the same time, and make differing changes? That’s what creates a **merge conflict**. These can be pretty hairy, and cleaning these up are an absolute pain. Now, go ahead and **finish this section**. Don’t worry too badly about the details here: just having a rough understanding of what git does when it encounters a conflict is good enough. Once again, google is your friend when you run into situations like these!

Finally, go ahead and read [Section 3.4](https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows). These **branching workflows are incredibly important**, because without them, you can imagine how messy these branches can get! With well-organized trees featuring long-running branches and topic branches, we can create easily readable projects with traceable histories. **Keep this Branching Workflow in-mind as we progress through the next two sections: we’ll need to revisit this Workflow and evolve it to handle collaboration!**
