# Development Guidelines
Below are some development guidelines and best practices when working on OpenDive software and hardware.
This doc covers general guidelines on documentation, version control, and tools.   

Blockchain specific readme's can be found here:

## Blockchain-specific Guidelines

- [Solana](https://github.com/OpenDive/dev-guidelines/blob/main/SOLANA.md)
- [Polkadot](https://github.com/OpenDive/dev-guidelines/blob/main/POLKADOT.md)
- [Avalanche](https://github.com/OpenDive/dev-guidelines/blob/main/AVALANCHE.md)
- [EVM Web3](https://github.com/OpenDive/dev-guidelines/blob/main/STANDARD_EVM.md)

## Table of Contents
- [Project Naming Conventions](#project-naming-conventions)
- [Software](#project-structure)
	- [Styleguides](#styleguides)
	- [Documentation](#documentation)
	- [Dependency Management](#dependency-management)
	- [Version Control](#version-control)
	- [GitHub](#github)
	- [Software Releases](#software-releases)
	- [Tools](#tools)
	- [Middleware and Frameworks](#middleware-and-frameworks)
- [Hardware](#hardware)

## Using Git and GitHub
We use [Git](https://git-scm.com/) for version control system [(VCS)](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control), and GitHub as the application to interact with Git and to store our repositories.   
There are two way to interact with Git (i.e. commit, push, merge etc). The first one is through any command line interface (CLI). The second one is through the [GitHub Desktop Application](https://desktop.github.com/) available for Windows and Mac, other applications are available but we request that our engineers use GitHub's Desktop  Application.   

Using a commmand line interface or GitHub's desktop application you'll be able to record your code into a repository through `commmits`, get the latests code changes from other teammates by `pulling`, and manage `merging` your code.

### Version Control
Below are some rules to follow when working with a version control system such as Git:

#### 1. MAKE SURE THE BUILD SUCCEEDS BEFORE COMMITTING CODE.
Broken code should not be committed.

#### 2. CREATE FEATURE BRANCHES. ISOLATE CODE THAT WILL CREATE OR CHANGE A FEATURE.    
Creating a branch does not affect other team members working on a different branch. This is desireable because a feature under development can create instability in the codebase.

#### 3. ALWAYS PULL DOWN THE LATEST CHANGES BEFORE BEGINNING TO CODE. 
This means that even before you start coding, you must perform a `pull`. In the CLI this command is `git pull origin [branch-name]`.   
This also means that you must keep you local version of the repository up to date. This is crucial if you’re working on a feature branch that may take more than a few hours to close, don’t let your branch diverge too far from the master branch.   
To elaborate if you create a feature branch called `feature-1` from the `develop` branch, make sure the perform a `pull` on the `develop` branch daily or as needed. Below we highlight this flow through commands.  

```
# Create a new feature branch called "feature-1" from the "develop" branch"
git checkout -b feature-1 develop
# Begin coding for sometime

# Perform a pull on develop
git pull develop

# Continue coding. Review any conflicts or merges
```

#### 4. USE MEANINGFUL AND SUCCINCT GIT MESSAGES.
You are writing the commits not for yourself, rather for the rest of the team.   
“A commit message shows whether a developer is a good collaborator”. **A project’s long-term success rests (among other things) on its maintainability** and being able to review others’ commits and pull requests with ease.  
This drives efficiency.

Here's an example of adequate commit messages:
```
5ba3db6 Fix failing CompositePropertySourceTests
84564a0 Rework @PropertySource early parsing logic
e142fd1 Add tests for ImportSelector meta-data
887815f Update docbook dependency and generate epub
ac8326d Polish mockito usage
```

- [A Successful Git Branching Model](http://nvie.com/posts/a-successful-git-branching-model/)

**Git Messages**

When [committing](http://dont-be-afraid-to-commit.readthedocs.io/en/latest/git/commandlinegit.html) code into a Git repository, you will have to write a message describing your code changes.  
It is crucial that we make these messages concise and consistent. A well-crafted commit message can tell other developers right away why your code changes matter or why they took place.  
  
Chris Beams has a great [post](https://chris.beams.io/posts/git-commit/) that summarizes the importance of a well-crafted commit message, along with the rationale behind it. Below are the seven rules he writes in his post, check out his post for more information.
    
**The seven rules of a great Git commit message**  
1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

- [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)

### Gitignore

[What is .gitignore?](http://stackoverflow.com/questions/27850222/what-is-gitignore-exactly/27850270)

- A collection of useful [.gitignore templates](https://github.com/github/gitignore)
- The [Ignoring Files chapter](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Ignoring-Files) of the Pro Git book.
- The [Ignoring Files article](https://help.github.com/articles/ignoring-files/) on the GitHub Help site.
- The [gitignore(5)](https://git-scm.com/docs/gitignore) manual page.

### GitHub
- [Referencing / closing issues using keywords](https://help.github.com/en/articles/closing-issues-using-keywords)

### Software Releases
- [GitHub: Creating Releases](https://help.github.com/en/articles/creating-releases)
- [Drupal: Release Types](https://www.drupal.org/node/467020)
- [Drupal: Release - rc, alpha, beta, dev](https://drupal.stackexchange.com/questions/99612/what-does-rc-stand-for-when-to-use-alpha-beta-and-dev-instead)
- [Drupal: Release Naming Conventions](https://www.drupal.org/node/1015226)
- [StackOverflow: Release Title is Same as Release Version](https://softwareengineering.stackexchange.com/questions/345006/why-popular-repositories-use-release-version-as-a-release-title-in-github)


## Project Naming Conventions
Different frameworks and languages have different naming conventions

**NodeJS**   
Lowercase snakecase. E.g. OpenEra Node project:   
```
openera-frontend/
```

**Unity**   
Capital camelcase / pascalCase. E.g. OpenEra Unity plugin
```
OpenEraWalletPlugin
```

## Software

One's profession should not be measured by the actions that are taken, but rather by the end-goal and the means of achieving such goal.

Anyone can program, not everyone can develop scalable, robust, and maintainable software. Let's aim for that...

You may find a list of useful books and [resources here](https://github.com/kPatch/awesome-developer-resources/blob/master/README.md#software-engineering).

### Styleguides

- [Arduino](https://www.arduino.cc/en/Reference/StyleGuide)
- [Ada]()
- [C](http://www.maultech.com/chrislott/resources/cstyle/indhill-cstyle.pdf)
- [C++](https://google.github.io/styleguide/cppguide.html)
- [Java](https://google.github.io/styleguide/javaguide.html)
- [JavaScript](https://github.com/feross/standard)
- [MATLAB](https://sites.google.com/site/matlabstyleguidelines/)
- [Python](https://google.github.io/styleguide/pyguide.html)
- [Solidity](http://solidity.readthedocs.io/en/develop/style-guide.html)

### Documentation

Self describing, terse code should be the norm. But, often times the complexity .... 

- [Beginners Guide To Docs](http://www.writethedocs.org/guide/writing/beginners-guide-to-docs/)
- [RTFM? How to write a manual worth reading](https://opensource.com/business/15/5/write-better-docs)

### Dependency Management

- [Gradle](https://gradle.org)

### Middleware and Frameworks

#### ROS
- Check what packages are available before development. http://www.ros.org/browse/list.php
- Packages vs Nodes
  - https://answers.ros.org/question/9133/packages-vs-nodes/
  - https://answers.ros.org/question/11835/when-should-i-split-my-code-into-multiple-packages-and-whats-a-good-way-to-split-it/
- Standard Units of Measure and Coordinate Conventions
  - http://www.ros.org/reps/rep-0103.html

## Hardware
### Motors
- Dynamixel
- Standard servo
### Tools
