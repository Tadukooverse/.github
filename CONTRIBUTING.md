---
title: Contributing Guidelines
blurb: Guidelines on how to contribute to Tadukooverse
---

# Contributing to Tadukooverse
Firstly, thanks for taking the time to contribute!

The following is a set of guidelines for contributing to Tadukooverse and its projects, which are hosted in the 
[Tadukooverse Organization](https://github.com/Tadukooverse) on GitHub. These are mostly guidelines, not rules. Use your best judgment, 
and feel free to propose changes to this document in a pull request.

#### Table of Contents
* [Code of Conduct](#code-of-conduct)
* [I Just Have a Question](#i-just-have-a-question)
* [What Should I Know?](#what-should-i-know)
	* [Vision](#vision)
	* [Main Projects](#main-projects)
		* [Tadukoo Util](#tadukoo-util)
		* [Tadukoo Engine/Launcher](#tadukoo-enginelauncher)
* [How Can I Contribute?](#how-can-i-contribute)
	* [Reporting Bugs](#reporting-bugs)
		* [Before Submitting a Bug Report](#before-submitting-a-bug-report)
		* [How Do I Submit a (Good) Bug Report?](#how-do-i-submit-a-good-bug-report)
	* [Suggesting Enhancements](#suggesting-enhancements)
		* [Before Submitting an Enhancement Suggestion](#before-submitting-an-enhancement-suggestion)
		* [How Do I Submit a (Good) Enhancement Suggestion?](#how-do-i-submit-a-good-enhancement-suggestion)
	* [Your First Code Contribution](#your-first-code-contribution)
	* [Pull Requests](#pull-requests)
* [Style Guides](#style-guides)
	* [Java Style Guide](#java-style-guide)
	* [Javadoc Style Guide](#javadoc-style-guide)
	* [Git Commit Style Guide](#git-commit-style-guide)
* [Additional Notes](#additional-notes)
	* [Issue and Pull Request Labels](#issue-and-pull-request-labels)
		* [Type of Issue](#type-of-issue)
		* [Issue Category](#issue-category)
		* [Level of Change](#level-of-change)
		* [Issue State](#issue-state)
		* [Operating System](#operating-system)
		* [Pull Request Labels](#pull-request-labels)

## Code of Conduct
This project and everyone participating in it is governed by the [Tadukooverse Code of Conduct](CODE_OF_CONDUCT.md). 
By participating, you are expected to uphold this code. Please report unacceptable behavior to [tadukooverse@gmail.com](mailto:tadukooverse@gmail.com).

## I Just Have a Question
> **Note:** Please don't file an issue to ask a question. You'll get faster results by using the resources below.

We have an [official website](https://tadukooverse.github.io) for Tadukooverse, which includes an [FAQ page](https://tadukooverse.github.io/about/faq.html) for frequently asked questions.

If chat is more your speed, you can join the Tadukooverse Discord server:
* [Join the Tadukooverse Discord server](https://discord.gg/cWzhbU7)
	* Even though Discord is a chat service, sometimes it takes some time for community members to respond &mdash; please be patient!
	* Use the `#general-questions` channel (in General Tadukooverse category) for general questions about Tadukooverse
	* Use the appropriate "#<project>-questions" channel under the appropriate category for questions specific to a project
		* **Note**: If one does not yet exist, you may ask in the "#general-questions" channel
    * Over time, more channels will be available, check the channel list (more may be listed here in the future)

## What Should I Know?
### Vision
Our vision is to create efficient free and open source software.

In terms of efficiency, we mean both via code efficiency (/speed) as well as memory efficiency, at least as best we can manage with a garbage collected language such as Java.

In terms of it being free and open source, we mean that anyone can do pretty much whatever they want with it (including producing proprietary software) and can make extensions or modifications based on their needs using the open source code.

> **Note**: We have a [Roadmap page](https://tadukooverse.github.io/about/roadmap.html) that shows what we're currently doing to work towards our vision.

### Main Projects
> **Note**: These projects are in early development, so the information here is subject to change without notice. Also note that these projects are not yet transferred to the Tadukooverse organization, but will be soon.

#### Tadukoo Util
Tadukoo Util is meant as a collection of utility libraries for very common use. They can be used in conjunction with Tadukoo Engine/Launcher, or can be used separately in other programs if desired. This collection is not meant as a full smorgasbord of all libraries, but is just meant to include the most common libraries to be reused in most projects (e.g. common null-safe string/boolean checks, multimaps, view utilities, etc.)

#### Tadukoo Engine/Launcher
Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. By using the launcher/engine combo instead of having completely standalone programs, any libraries used by multiple programs only need to be stored once and loaded as needed. This saves memory on the host machine by not having a library duplicated within the actual program jars.

Tadukoo Launcher provides a list of programs that are installed or may be downloaded. Once a program is selected, the launcher will download it along with its required libraries. Then the libraries and program will be loaded into memory and launched.

Tadukoo Engine provides the proper interfaces that programs should use to allow the launcheer to connect to and load them. In addition, the engine and launcher come with standard libraries from Tadukoo Util by default so they don't need to be downloaded separately later.

If you want to read about using the Tadukoo Engine/Launcher or developing programs for it, check out the Tadukoo Engine/Launcher Guide (Coming Soon).

## How Can I Contribute?
### Reporting Bugs
This section guides you through submitting a bug report. Following these guidelines helps maintainers and the community understand your report, reproduce the behavior, and find related reports.

Before creating bug reports, please check [this list](#before-submitting-a-bug-report) as you might find out that you don't need to create one. When you are creating a bug report, [please include as many details as possible](#how-do-i-submit-a-good-bug-report). Fill out the [required template](/.github/ISSUE_TEMPLATE/bug-report.md), the information it asks for helps us resolve issues faster.

> **Note**: If you find a **Closed** issue that seems like it is the same thing that you're experiencing, open a new issue and include a link to the original issue in the body of your new one.

#### Before Submitting a Bug Report
* **Check the Debugging Guide (Coming Soon)**. You might be able to find the cause of the problem and fix things yourself. Most importantly, check if you can reproduce the problem in the latest version of the software and if you can get the desired behavior by changing certain config settings.
* **Check the [FAQ page](/about/faq.html)** for a list of common questions and problems.
* **Determine which [repository the problem should be reported in](/projects.html)**.
* **Perform a [cursory search](https://github.com/search?q=+is%3Aissue+user%3ATadukooverse)** to see if the problem has already been reported. **If it has and the issue is still open**, add a comment to the existing issue instead of opening a new one.

#### How Do I Submit a (Good) Bug Report?
Bugs are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined [which repository](/projects.html) your bug is related to, create an issue on that repository and provide the following information by filling in [the template]((/.github/ISSUE_TEMPLATE/bug-report.md).

Explain the problem and include additional details to help maintainers reproduce the problem:
* **Use a clear and descriptive title** for the issue to identify the problem.
* **Describe the exact steps which reproduce the problem** in as many details as possible. When listing steps, **don't just say what you did, but explain how you did it**.
* **Provide specific examples to demonstrate the steps.** Include links to files or GitHub projects, or copy/pasteable snippets, which you use in those examples. If you're providing snippets in the issue, use [Markdown code blocks](https://help.github.com/articles/markdown-basics/#multiple-lines).
* **Describe the behavior you observed after following the steps** and point out what exactly is the problem with that behavior.
* **Explain which behavior you expected to see instead and why**.
* **Include screenshots and/or animated GIFs** which show you following the described steps and clearly demonstrate the problem.
* **If you're reporting that the software crashed**, include a crash report with a stack trace.
* **If the problem wasn't triggered by a specific action**, describe what you were doing before the problem happened and share more information using the guidelines below.

Provide more context by answering these questions:
* **Did the problem start happening recently** (e.g. after updating to a new version of the software) or was this always a problem?
* If the problem started happening recently, **can you reproduce the problem in an older version**? What's the most recent version in which the problem doesn't happen?
* **Can you reliably reproduce the issue**? If not, provide details about how often the problem happens and under which conditions it normally happens.

### Suggesting Enhancements
This section guides you through submitting an enhancement suggestion, including completely new features and minor improvements to existing functionality. Following these guidelines helps maintainers and the community understand your suggestion and find related suggestions.

Before creating enhancement suggestions, please check [this list](#before-submitting-an-enhancement-suggestion) as you might find out that you don't need to create one. When you are creating an enhancement suggestion, please [include as many details as possible](#how-do-i-submit-a-good-enhancement-suggestion). Fill in [the template](.github/ISSUE_TEMPLATE/feature-request.md), including the steps that you imagine you would take if the feature you're requesting existed.

#### Before Submitting an Enhancement Suggestion
* **Check the Debugging Guide (Coming Soon)** for tips — you might discover that the enhancement is already available. Most importantly, check if you're using the latest version of the software and if you can get the desired behavior by changing certain config settings.
* **Check if there's already [a repository](/projects.html) which provides that enhancement**.
* **Determine [which repository](/projects.html) the enhancement should be suggested in**.
* **Perform a [cursory search](https://github.com/search?q=+is%3Aissue+user%3ATadukooverse)** to see if the enhancement has already been suggested. If it has, add a comment to the existing issue instead of opening a new one.

#### How Do I Submit a (Good) Enhancement Suggestion?
Enhancement suggestions are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined [which repository](/projects.html) your enhancement suggestion is related to, create an issue on that repository and provide the following information:
* **Use a clear and descriptive title** for the issue to identify the suggestion.
* **Provide a step-by-step description of the suggested enhancement** in as many details as possible.
* **Provide specific examples to demonstrate the steps**. Include copy/pasteable snippets which you use in those examples, as [Markdown code blocks](https://help.github.com/articles/markdown-basics/#multiple-lines).
* **Describe the current behavior and explain which behavior you expected to see instead** and why.
* **Include screenshots and/or animated GIFs** which help you demonstrate the steps or point out the part of the software which the suggestion is related to.
* **Explain why this enhancement would be useful**.
* **Specify which version of the software you're using**.
* **Specify the name and version of the OS you're using**.

### Your First Code Contribution
Unsure where to begin contributing to Tadukooverse? You can start by looking through the beginner and help-wanted issues:
* [Beginner issues](https://github.com/search?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3ABeginner+label%3"AHelp+Wanted"+user%3ATadukooverse+sort%3Acomments-desc) - issues which should only require a few lines of code, and a test or two.
* [Help wanted issues](https://github.com/search?q=is%3Aopen+is%3Aissue+label%3A"Help+Wanted"+user%3ATadukooverse+sort%3Acomments-desc+-label%3ABeginner) - issues which should be a bit more involved than beginner issues.
Both issue lists are sorted by total number of comments. While not perfect, number of comments is a reasonable proxy for impact a given change will have.

When you start working on an issue, create a new branch off of the release it's for, named ```<release branch name>-<issue name>``` (e.g. ```v.0.2-Alpha-SNAPSHOT-Tadukoo-Look-&-Feel```). 
For more information about how we use Git branches, check out the [Git Branching Guide](https://tadukooverse.github.io/guides/git-branching.html).

### Pull Requests
The process described here has several goals:
* Maintain quality
* Fix problems that are important to users
* Engage the community in working toward the best possible software
* Enable a sustainable system for Tadukooverse's maintainers to review contributions

Please follow these steps to have your contribution considered by the maintainers:
1. Follow all instructions in [the template](/.github/PULL_REQUEST_TEMPLATE)
2. Follow the [style guides](#style-guides)
3. After you submit your pull request, verify that all [status checks](https://help.github.com/articles/about-status-checks/) are passing<details><summary>What if the status checks are failing?</summary>If a status check is failing, and you believe that the failure is unrelated to your change, please leave a comment on the pull request explaining why you believe the failure is unrelated. A maintainer will re-run the status check for you. If we conclude that the failure was a false positive, then we will open an issue to track that problem with our status check suite.</details>
While the prerequisites above must be satisfied prior to having your pull request reviewed, the reviewer(s) may ask you to complete additional design work, tests, or other changes before your pull request can be ultimately accepted.

## Style Guides
### Java Style Guide
*If you use IntelliJ, you can import [these Java Code Style settings](IntelliJ%20Java%20Code%20Style.xml)*

*If you use Eclipse, you can import [these Java Code Style settings](Eclipse%20Java%20Code%20Style.xml).*

* **Note**: This is not necessarily a full list, as there's probably styling we take for granted and assume is standard. If you have any questions, feel free to ask or search the existing code to figure it out.
* We use tabs, not spaces for indentation
* Braces are used where optional (e.g. if, else, for, etc. - even if the code block is only one line)
* In general, if a space isn't necessary, we don't use it
	* e.g. around parentheses and braces - we do if(<condition>){ - no spaces next to those parentheses or that curly brace
	* Empty code blocks we place a space in-between though: 
	```
	try{
		doSomething();
	}catch(Exception e){ }
	```
* The column limit is 120 (IntelliJ's default). If you go over this limit, break up the statement at logical points
* camelCase is used for methods and fields
* TitleCase is used for class names
* Constants (defined as private/public static final <type>) should be in CONSTANT_CASE
* Always specify @Override
* If IntelliJ gives a warning about it, you should probably change it

### Javadoc Style Guide
Classes, fields, and methods should all be Javadoc'd so that others can understand what's going on.

For classes, we do something similar to the following:
```
/**
 * Custom Cell Renderer used to just have a component draw itself (for use with custom components).
 * This can be used as either a {@link ListCellRenderer} or as a {@link TableCellRenderer}.
 *
 * @author Logan Ferree (Tadukoo)
 * @version 0.1-Alpha
 * @since Pre-Alpha
 */
 ```
 * Note that if there are multiple authors, they can be noted in order of contribution
 * Version is used to denote the most recent version the class was updated during, and since is used for the original version it was created during.
 	* If version and since match, we only include version

For fields, we use a single line for the Javadoc, like so:
```
/** The x position of the Image */
```

For a method, if you're simply inheriting the documentation from the method you're overriding, you can do this on a single line. Otherwise, it should be multiple lines, like the class Javadoc is (but no need for author, version, or since):
```
/** {@inheritDoc} */
```

### Git Commit Style Guide
* Keep the commit name short
* Reference issues and pull requests always in the body of the commit
* Consider including a relevant emoji for what was done (e.g. :art: for UI changes, etc.)
* Include actual details about your change
	* E.g. Don't just say "Added X Class", tell us what that class does
	* E.g. Don't just say "Fixed X Bug", tell us what you changed to fix it, and note any unit tests you added to prevent it in the future

## Additional Notes
### Issue and Pull Request Labels
The following lists the standard labels that typically exist in all repositories of Tadukooverse. If you notice some labels are missing in a particular repository, please open an issue on that repository.

The labels are grouped by purpose, but it's not required that every issue use a label from every group, and an issue may also have multiple labels from the same group (e.g. `Enhancement` and `New Module` may be on the same issue).

> **Note**: We're currently setting up the contributing guidelines, so this list is likely to change.

#### Type of Issue

| Label name | `Tadukooverse`‑org :mag_right: | Description |
| --- | --- | --- |
| `Bug` | [search][search-tadukooverse-org-label-bug] | Confirmed bugs or reports that are very likely to be bugs |
| `Documentation` | [search][search-tadukooverse-org-label-documentation] | Changes to be made to the documentation |
| `Enhancement` | [search][search-tadukooverse-org-label-enhancement] | Feature requests |
| `New Module` | [search][search-tadukooverse-org-label-new-module] | Feature request which might be a good candidate for a new module, instead of extending existing modules |
| `Testing` | [search][search-tadukooverse-org-label-testing] | Changes to be made to test cases (e.g. to cover cases not currently covered) |

#### Issue Category

| Label Name | `Tadukooverse` -org :mag_right: | Description | 
| --- | --- | --- | 
| Crash | [search][search-tadukooverse-org-label-crash] | Reports of the software completely crashing | 
| Performance | [search][search-tadukooverse-org-label-performance] | Related to performance | 
| Security | [search][search-tadukooverse-org-label-security] | Related to security | 
| UI | [search][search-tadukooverse-org-label-ui] | Related to the visual design | 

#### Level of Change

| Label name | `Tadukooverse`‑org :mag_right: | Description |
| --- | --- | --- |
| `Epic` | [search][search-tadukooverse-org-label-epic] | A large multi-faceted issue - these would likely have a list of smaller issues contributing towards them |
| `Small Change` | [search][search-tadukooverse-org-label-small-change] | Represents a minor change that can be completed quickly |

#### Issue State

| Label name | `Tadukooverse`‑org :mag_right: | Description |
| --- | --- | --- |
| `Beginner` | [search][search-tadukooverse-org-label-beginner] | Less complex issues which would be good first issues to work on for users who want to contribute to Tadukooverse |
| `Blocked` | [search][search-tadukooverse-org-label-blocked] | This item is blocked by another issue |
| `Duplicate` | [search][search-tadukooverse-org-label-duplicate] | Issues which are duplicates of other issues, i.e. they have been reported before |
| `Help Wanted` | [search][search-tadukooverse-org-label-help-wanted] | The Tadukooverse team would appreciate help from the community in resolving these issues |
| `Invalid` | [search][search-tadukooverse-org-label-invalid] | Issues which aren't valid (e.g. user errors) |
| `More Info Needed` | [search][search-tadukooverse-org-label-more-info-needed] | More information needs collected for the bug/enhancement |
| `Needs Reproduction` | [search][search-tadukooverse-org-label-needs-reproduction] | Bugs that haven't been able to be reliably reproduced yet |
| `Wontfix` | [search][search-tadukooverse-org-label-wontfix] | The Tadukooverse team has decided not to fix these issues for now, either because they're working as intended or for some other reason |
| `Wrong Repo` | [search][search-tadukooverse-org-label-wrong-repo] | Issues reported to the wrong repository |

#### Operating System

| Label Name | `Tadukooverse` -org :mag_right: | Description | 
| --- | --- | --- |
| `Android` | [search][search-tadukooverse-org-label-android] | Related to running on Android | 
| `iOS` | [search][search-tadukooverse-org-label-ios] | Related to running on iOS | 
| `Linux` | [search][search-tadukooverse-org-label-linux] | Related to running on Linux | 
| `Mac` | [search][search-tadukooverse-org-label-mac] | Related to running on Mac | 
| `Windows` | [search][search-tadukooverse-org-label-windows] | Related to running on Windows | 

#### Pull Request Labels

| Label Name | `Tadukooverse` -org :mag_right: | Description | 
| --- | --- | --- |
| `Needs Review` | [search][search-tadukooverse-org-label-needs-review] | Pull Requests that need to be reviewed | 
| `Needs Testing` | [search][search-tadukooverse-org-label-needs-testing] | Pull Requests that require manual testing | 
| `Requires Changes` | [search][search-tadukooverse-org-label-requires-changes] | Pull Requests that require changes based on review comments | 
| `Under Review` | [search][search-tadukooverse-org-label-under-review] | Pull Requests that are currently being reviewed | 
| `WIP` | [search][search-tadukooverse-org-label-wip] | Pull Requests that are in progress | 

[search-tadukooverse-org-label-android]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AAndroid
[search-tadukooverse-org-label-beginner]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ABeginner
[search-tadukooverse-org-label-blocked]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ABlocked
[search-tadukooverse-org-label-bug]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ABug
[search-tadukooverse-org-label-crash]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ACrash
[search-tadukooverse-org-label-documentation]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ADocumentation
[search-tadukooverse-org-label-duplicate]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ADuplicate
[search-tadukooverse-org-label-enhancement]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AEnhancement
[search-tadukooverse-org-label-epic]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AEpic
[search-tadukooverse-org-label-help-wanted]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AHelp%20Wanted
[search-tadukooverse-org-label-invalid]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AInvalid
[search-tadukooverse-org-label-ios]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AiOS
[search-tadukooverse-org-label-linux]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ALinux
[search-tadukooverse-org-label-mac]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AMac
[search-tadukooverse-org-label-more-info-needed]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AMore%20Info%20Needed
[search-tadukooverse-org-label-needs-reproduction]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ANeeds%20Reproduction
[search-tadukooverse-org-label-needs-review]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ANeeds%20Review
[search-tadukooverse-org-label-needs-testing]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ANeeds%20Testing
[search-tadukooverse-org-label-new-module]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ANew%20Module
[search-tadukooverse-org-label-performance]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3APerformance
[search-tadukooverse-org-label-requires-changes]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ARequires%20Changes
[search-tadukooverse-org-label-security]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ASecurity
[search-tadukooverse-org-label-small-change]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ASmall%20Change
[search-tadukooverse-org-label-testing]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3ATesting
[search-tadukooverse-org-label-ui]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AUI
[search-tadukooverse-org-label-under-review]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AUnder%20Review
[search-tadukooverse-org-label-windows]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AWindows
[search-tadukooverse-org-label-wip]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AWIP
[search-tadukooverse-org-label-wontfix]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AWontfix
[search-tadukooverse-org-label-wrong-repo]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3ATadukooverse+label%3AWrong%20Repo
