# Beginner Python

See the general explanation about [progress pathes](/pathes).

These are specific steps for people who have already learned some Python, but don't have much experience in it.

I'd recommend doing each one of the steps several times till you get familiar with the process. Then move on to the next step.
At any time if you have questions, feel free to ask in our [chat](/chat).

One thing I noticed is that people new to open source are looking for *open issues with clear instructions*. The thing is, that it is very rare to find an issue that is already known, that someone already wrote clear instructions and that it easy enough for a beginner to tackle. Easy issues are usually implemented rather quickly. So instead of that we will find places of improvement that have not been reported yet.

## Start by practicing the pull-requests without the need to write code.

I know you are eager to write programs, but in order to contribute you also need to know how to use git and GitHub properly. I think it is better to separate these two tasks and first practice the Pull-request part.

* Data collection: [Open source companies](https://osdc.code-maven.com/open-source-by-organizations/).
* Pick one of the projects from the [Awesome for non-programmers](https://github.com/szabgab/awesome-for-non-programmers) list.

# Learn how to set up the local development environment of open source projects

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


