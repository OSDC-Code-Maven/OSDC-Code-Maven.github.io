# Beginner Python

See the general explanation about [progress pathes](/pathes).

These are specific steps for people who have already learned some Python, but don't have much experience in it.o

On this page you'll find a number of assignments that you can follow in order to step-by-step get into contribution to Python-based Open Source projects.

I'd recommend doing each one of the steps several times till you get familiar with the process. Then move on to the next step.
At any time if you have questions, feel free to ask in our [chat](/chat).

One thing I noticed is that people new to open source are looking for **open issues with clear instructions**. The thing is, that it is very rare to find an issue that is already known, that someone already wrote clear instructions and that it easy enough for a beginner to tackle. There are various lists of "awesome first issues", but in my experience those tend to be a lot more demanding than what I'd expect to be a a "first contribution". Easy issues are usually implemented rather quickly. Especially in popular projects. So instead of that we will find places of improvement that have not been reported yet.

## Start by practicing the pull-requests without the need to write code.

I know you are eager to write programs, but in order to contribute you also need to know how to use git and GitHub (or GitLab) properly. I think it is better to separate these two tasks and first practice the Pull-Request part.

In order to do this you need to find a project that does not need programming. I maintain a list called [Awesome for non-programmers](https://github.com/szabgab/awesome-for-non-programmers) that lists projects just like that.

The OSDC community has a number of such projects of its own. Contributing to these projects have the advantage that we can be reached via the [chat](/chat) as well.

* You could help with the content of this web site. [source](https://github.com/OSDC-Code-Maven/OSDC-Code-Maven.github.io)
* Data collection: [Open source companies](https://osdc.code-maven.com/open-source-by-organizations/) that has a separate [GitHub repo](https://github.com/OSDC-Code-Maven/open-source-by-organizations/)

## Change meta-data of projects

In the [PyDigger](https://pydigger.com/) project we collect information about Python projects. Part of this information is meta-data about each PyPI distribution.
Some of the projects are missing some meta-date or have them incorrectly. Check out these items:

* Missing [author field](https://pydigger.com/docs/author).
* Missing or incorrect [license field](https://pydigger.com/docs/license).
* Missing [link to VCS](https://pydigger.com/docs/vcs).

Each one of these changes is small and does not require any understanding of the project. So these are what we can consider "low-hanging-fruits".

## Learn how to set up the local development environment of open source projects

* Assumption: you already know how to *run* tests in Python.

* The [Flask](https://github.com/pallets/flask) has clear instructions.
* TODO: find more projects with clear instructions and add them here. Record videos and link to them.

* Find a relatively new Python project that does not have instruction yet.
* Check the [recently updated python projects](https://github.com/topics/python?l=python&o=desc&s=updated)
* Find one that does not have many stars (too many stars means the project is popular so it probably already has instructions)
* Clone the repository
* Try to run the tests of the project. If you can't figure out how, ask for help in our [community](/chat) and/or open an issue on the project explaining what you did and asking for help.
* Once you figured out the steps to set up the local development environment and run the tests, add this description to the README file of the project and send this as a contribution.

## Write tests for a project

For this we already assume you know how to write tests in the format that `pytest` can run. It is also useful to know how to generate the test coverage report.

* Find a project that does not have any tests or that does not have a lot of tests.
* You might find them among the [recently updated python projects](https://github.com/topics/python?l=python&o=desc&s=updated) that don't have many stars as in the previous section. You can also continue working on the projects that you have already worked on in the previous section.
* Write a simple test that checks part of the project that has not been tested yet. Send a pull-request with that test.

## Setting up GitHub Actions (Continuous Integration) for a project

While setting up and configuring complex CI/CD processes is a different expertise than programming Python, the needs of most of the open source projects are simple
and knowing how to do that can be considered part of the job of the programmer. Just as most people would take their car to a garage to get it fixed, but can fill petrol in the car
themselves can change tires or can check the level of water and oil. Configuring a basic CI for a project is relatively easy and it is another great contribution to any open source
project.

In the [PyDigger](https://pydigger.com/) project we have a list of projects [on GitHub without any CI](https://pydigger.com/search/has-github-no-ci).
Pick one, configure GitHub Actions and send a pull-request with that.


