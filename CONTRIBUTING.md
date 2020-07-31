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
