# Contributing to Tadukooverse
Firstly, thanks for taking the time to contribute!

The following is a set of guidelines for contributing to Tadukooverse and its projects, which are hosted in the 
[Tadukooverse Organization](https://github.com/Tadukooverse) on GitHub. These are mostly guidelines, not rules. Use your best judgment, 
and feel free to propose changes to this document in a pull request.

#### Table of Contents
[Code of Conduct](#code-of-conduct)

[I Just Have a Question](#i-just-have-a-question)

[What Should I Know?](#what-should-i-know)
* [Vision](#vision)
* [Main Projects](#main-projects)
	* [Tadukoo Util](#tadukoo-util)
	* [Tadukoo Engine/Launcher](#tadukoo-enginelauncher)

[Additional Notes](#additional-notes)
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

### Main Projects
> **Note**: These projects are in early development, so the information here is subject to change without notice. Also note that these projects are not yet transferred to the Tadukooverse organization, but will be soon.

#### Tadukoo Util
Tadukoo Util is meant as a collection of utility libraries for very common use. They can be used in conjunction with Tadukoo Engine/Launcher, or can be used separately in other programs if desired. This collection is not meant as a full smorgasbord of all libraries, but is just meant to include the most common libraries to be reused in most projects (e.g. common null-safe string/boolean checks, multimaps, view utilities, etc.)

#### Tadukoo Engine/Launcher
Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. By using the launcher/engine combo instead of having completely standalone programs, any libraries used by multiple programs only need to be stored once and loaded as needed. This saves memory on the host machine by not having a library duplicated within the actual program jars.

Tadukoo Launcher provides a list of programs that are installed or may be downloaded. Once a program is selected, the launcher will download it along with its required libraries. Then the libraries and program will be loaded into memory and launched.

Tadukoo Engine provides the proper interfaces that programs should use to allow the launcheer to connect to and load them. In addition, the engine and launcher come with standard libraries from Tadukoo Util by default so they don't need to be downloaded separately later.

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
