---
title: Technical Writing and Documentation
layout: default
nav_order: 2
---

# Technical Writing and Documentation

**Author**: Alan Jian

For our processes at the CEC to improve, we need to build towards **comprehensive**, **shareable**, **end-to-end** knowledge of existing models, code, and projects. But how? As with most important technical practices, most coding guides, coursework, and education omit the core tenets of **technical writing**, despite it being one of the most important skills in domains like software engineering and data science.

By the end of this section, you should have a solid understanding of technical writing and documentation, and how to establish the foundations of a great documentation culture within your team.

## Expanding our Definition of Documentation [(The Linux Information Project)](https://www.linfo.org/documentation.html)

We’ll start by reading this high-level overview of what documentation is from arguably one of the most successful and influential software projects in the world: Linux! Now, **don’t skip this, even if you think you know what documentation is**. Though it might seem extremely obvious what documentation is, it’s important to see the myriad ways in which documentation show up and get a flavor for how the culture of *open-source computing* affects our understanding of documentation.

With that, go and skim through the above reading, paying attention to:

- How the Linux software team defines documentation
- The various forms of documentation
- Why *open source culture* is foundational to how documentation should be maintained

Remember that definition!

{: .tip}
**Documentation**: any communicable material that is used to describe, explain or instruct regarding some attributes of an object, system or procedure, such as its parts, assembly, installation, maintenance and use.

The emphasis here is on the word **any**: that includes in-line comments in code, screen captures, directory structures, even the way we name variables in code!

## Gentle Introduction to Style Guides [(Google Style Guide)](https://google.github.io/styleguide/)

Given the sheer breadth of documentation formats, and its importance to the development pipeline, many organizations choose to standardize their approaches to documentation using something called a **style guide**. Take a look at the above style guide adopted by the engineers at Google, **paying close attention to the Markdown Style Guide**. After you’re done, navigate to the **Python Style Guide**, and read through **Sections 1 and 2.1 carefully**. Notice the usage of a Linter, which we’ll discuss in a moment. Once you’re done, breeze through the rest of the document, **paying attention to how Section 2 and 3** differ from one another.

{: .note}
**CL** stands for **changelog**: essentially, they’re referring to a group of changes to the codebase. For those familiar with GitHub, you can basically substitute CL with **PR (pull request)**.

{: .note}
The point of this reading isn’t that we need an organization-wide guide, especially for an organization as decentralized as the CEC. The point is to highlight the format and structure of style guides that have *proven track records of success*.

Let's talk about the Python Style Guide first. There were a few important details here that you should’ve noticed:

- **Algorithmic enforceability**: At the lowest level, these docs provide a set of hard, fast, checkable standards, whose review can be automated.
  - In Section 2.1, they discuss a standard, customizable **Linter** (which helps check the code for potential bugs and flag style issues) that makes writing compliant code easier. Think of this tech as an extension to auto-correct: it can flag things like spacing issues, line-length issues, and if enabled, can actually auto-correct entire documents with a click of a button.
  - Folks at Google consider these standards to be so important that they enforce it as a rule for their repositories: **that means you cannot push new code to the codebase unless it complies with these rules**.
- **Stylistic Considerations**: Notice here that with every rule comes with pros and cons. That’s because to build a style guide, there will be benefits and trade-offs that need to be discussed with fellow colleagues. The guiding question in every section of the document is **“What sacrifices to simplicity and expressiveness need to be made to prioritize readability?”**

But beyond algorithmically enforceable rules and stylistic considerations, we notice that, in addition to hard rules about naming conventions, capitalization, and code organization, guides like the **Markdown guide** also contain *high-level principles* that practitioners are meant to follow. That’s because maintaining good documentation is about more than being nitpicky about punctuation: it’s about **creating a culture of maintainability** and utilizing **design thinking** which we’ll explore in this next resource!

## Creating a Culture of Maintainability [(Agile Documentation)](https://agilemodeling.com/essays/agileDocumentationBestPractices.htm)

If this is the first time you’ve heard of Agile, count your lucky stars: the Agile methodology is an iterative approach to project management that emphasizes flexibility and collaboration by breaking work into small, manageable cycles. It primarily got its start in Silicon Valley as a strategy for managing software development, and mentioning it gets a good groan out of most software engineers.

Now, even if you know enough about Agile to despise it, don’t worry: we’re only here for its thoughts on documentation. What Agile does well is that it treats documentation as a **deliverable** that needs to be built **as part of the development process**.

This one is a bit of a longer reading, but I can’t stress this enough: **read through the entire thing**. A few tips about this resource as you’re reading it:

{: .tip}
Don’t get too bogged down by the details; there are tons of hyperlinks on this website, and you can easily get into a project management rabbit hole.

{: .tip}
Think about how it compares to the principles set forth in the style guide from Google. What sets these principles apart?

As you can probably tell, Agile concerns itself with higher level principles that dictate a **culture**, as opposed to the more specific, actionable steps laid out by the google style guide. In particular, it’s important that documentation at the CEC embodies the following principles discussed in the reading:

1. **Minimally Viable**: As stated in the Agile docs, “The basic trade-off is the ‘security’ of having the document against your trust in its accuracy”. In order to stay current and accurate, huge docs require tons of edits that nobody wants to make. Every additional sentence you write is additional work to revise down the road!
2. **Collaborative**: The primary stakeholder to most documentation are your peers here at the CEC. That means documentation requires the **constant solicitation of feedback**; without it, we run the risk of doing a bunch of work that no one will bother to read or update.
3. **Iterative**: Documentation should be treated as a deliverable in its own right. Every time you revisit a document to look something up, highlight, tweak, and improve the docs so that FAQs and important information pop out straight at the reader.

Thinking about documentation as an **iterative**, **collaborative**, **minimally viable product** with **stakeholders** (e.g. your team, new hires, managers) goes a long way towards making documentation that’s actually readable, actually maintainable, and actually accurate.

## Exploring a Data Science-specific Standard [(Cookiecutter Data Science)](https://cookiecutter-data-science.drivendata.org/)

So far, most of the resources that we’ve looked at are primarily meant for software engineers, and doesn’t really speak to the data-driven development/forecasting that we do here at the California Energy Commission. The Cookiecutter Data Science project is a project organization template *specifically* designed for data practitioners in mind.

First, take a look at the **Directory structure** section of the landing page. The Cookiecutter project suggests a directory structure that facilitates the work that we do as a team, making it easy for other folks to jump in on an on-going project, and know exactly where resources/dependencies are located.

Then, using the navigation bar, navigate to the **Why ccds?** and the **Opinions** sections, and **read both in their entirety**. Notice the specific needs that are surfaced that aren’t covered by Agile Documentation or Google’s Style Guide. In particular, our division has an interest in **reproducibility** of results that necessitates a clear way of understanding what and how steps were taken to generate results.

## Concluding Thoughts and Best Practices

In essence, good documentation starts with agreed upon practices and establishing a good **culture of maintainability**. If we’re trying to write/improve documentation, it starts with a **good style guide**.
From the examples that you can see here, a good style guide contains the following:

1. At the highest level, it contains **guiding principles** for maintaining a **culture of maintainability**. These represent the animus of why and how documentation should be formed.
2. Going down a level, it contains **actionable steps** around documentation improvement and implementation, suggesting *when* and *how* to incorporate documentation writing into existing your existing project workflow.
3. At the lowest level, it contains **exact specifications** around punctuation, naming conventions, directory structure, and style. These are rule-based conventions that are (in most cases) algorithmically enforceable.
Within your unit, evaluate your style guide (if there is one). Does it contain each of these levels of detail? How tightly has it been enforced? Are there pain-points that make it difficult to follow, principles that other members of the team don’t agree with?

Within your unit, evaluate your style guide (if there is one). Does it contain each of these levels of detail? How tightly has it been enforced? Are there pain-points that make it difficult to follow, principles that other members of the team don’t agree with?

### Setting up a Style Guide

In case your team doesn’t have a style guide, here are a few tips to get your team up and running:

1. **Start with a template.** Using some of the resources listed in this reading source as a jumping off point is a quick way to get started.
    1. The Google guide gives some practical steps to start organizing documentation
    2. Many principles in the Agile documentation resource can be official adopted into your team’s practice.
    3. Using the Cookiecutter directory structure with simplifying modifications can aid with data analysis and forecasting work
2. **Establish a culture of maintainability.** In addition to standards, make sure documentation processes are built into the project pipeline. Explicitly define how and when documentation should be iterated upon.
3. **Focus on brevity.** Documentation is composed of living, breathing outputs that are meant to be iterated over time. If you write something, it will eventually need to be updated.
