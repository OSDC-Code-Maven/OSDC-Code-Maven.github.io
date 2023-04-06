# Pass on the favor

Have you just received a Pull-request or have you just received a useful issue? Has someone just contributed to your open source project?

Would you want to "return the favor" or would you rather "pass on the favor"?

> "Pay it forward" is an expression for when the recipient of an act of kindness does something kind for someone else rather than simply accepting or repaying the original good deed. However "Pass on the favor" or "Pass on the kindness" might be a better expression here as no payment is involved.

We believe that a small contribution to an Open Source project of someone else can go a long way. You might already put a lot of energy in your projects,
but a contributing to someone else can have a network effect. It will help the recipient of the contribution and we can ask that person to pass on the favor
and contribute to yet another project.

On this page you'll find a collection of ideas on the types of contributions you could make. Most of them are rather small that don't need a lot of time from you
and most of them don't require any (deep) involvement in the project.

When you open the pull-request or maybe even better when it gets accepted we would ask you to add a comment to the pull-request mentioning this project
and inviting the recipient of your pull-request to "pay it forward". You can either link to this page or the [issue](https://github.com/OSDC-Code-Maven/OSDC-Code-Maven.github.io/issues/5)
that explains it.

## What is a valuable contribution?

You can do many different thing to contribute to an open source project. Your contribution can be small or it can big. Everyone can contribute based on their current capabilities and the available time they have.
* It can be changing some META data of the project.
* It can be opening an issue, a well explained issue. It can be commenting on an issue.
* It can be adding Continuous Integration (CI) (e.g. GitHub Actions) to the project.
* It can be improving the documentation. (e.g. by adding an example, by explaining how to set up the development environment, etc.)
* It can be adding a test.
* It can be fixing a bug.
* It can be adding a new feature.
* ... There are many other forms you can contribute, these are just some of the more common ones.

Contributing a feature or fixing a bug will need a much deeper understanding of the project and will probably require a lot more time than writing a test or writing a usage example. Updating the META data of the project usually does not require hardly any understanding of the projects.


## Which projects to contribute?

When talking about contribution to an open source project many people immediately think about one of the well-known high-profile project. Indeed contributing to such a project might sound cooler, but it is also usually a lot harder. Partially it is because well know and big projects probably have already fixed all the simple issues so in order to contribute you will have to be rather involved in the project. These projects also tend to have much stricter rules on how a contribution - especially code-contribution - should look like. Many of these projects are owned by some corporation and they will make you sign an agreement before you can contribute code.

There are millions of relatively small and new project that have tons of small issues you can help fixing. So unless you really have am itch to scratch with a specific project, you'll be better off contributing to one of the lesser known projects.


## How to find projects and ideas to do?

Let's collect a few examples and how to find a project where you can contribute.

## Remove unnecessary files

* Find repositories that include files that should not be committed to git. (e.g. generated files, caches etc.) Remove them, create a `.gitignore` file explain how it works.
* See this article: [Billions of unnecessary files in GitHub](https://dev.to/szabgab/billions-of-unnecessary-files-in-github-i85)


## Add meta data to Python projects

* [PyDigger](https://pydigger.com/) - link to VCS field.
    * [Add author field](https://pydigger.com/docs/author)
    * [Add or fix the license field](https://pydigger.com/docs/license)
    * [Add the summary field](https://pydigger.com/docs/summary)
    * [Link to VCS](https://pydigger.com/docs/vcs) (GitHub, GitLab, ...)

## Add meta data to Ruby projects

* [Ruby Digger](https://ruby-digger.code-maven.com/)

## Add meta data to Perl projects

* [CPAN Digger](https://cpan-digger.perlmaven.com/)
    * [Include VCS link in META data](https://perlmaven.com/how-to-add-link-to-version-control-system-of-a-cpan-distributions)
    * [Add license to META data](https://perlmaven.com/how-to-add-the-license-field-to-meta-files-on-cpan)
    * [Add contributors to META data](https://perlmaven.com/how-to-add-list-of-contributors-to-the-cpan-meta-files)

## Add instruction of local development

We believe that if we make it easier for others to contribute to our open source projects then there is a higher chances some will do so.
So it can be very valuable to include instruction on how to do that.

* How to set up the local development environment. Natively or inside a Docker container.
* How to run the tests locally.
* What are the recommendation on how to send a pull-request.

See a few articles about this:

* [Local development environment for the data.table R project](https://dev.to/szabgab/local-development-environment-for-the-datatable-r-project-5fhb)
* [Setup local development environment for R-yaml](https://dev.to/szabgab/setup-local-development-environment-for-r-yaml-5ejc)
* [Setup local development environment and run tests of PHP Twig](https://dev.to/szabgab/setup-local-development-environment-and-run-tests-of-php-twig-34d3)

## Configure GitHub Actions (Continuous Integration / CI)

* For Python you can find projects that do not have a working CI on the stats page of the [PyDigger](https://pydigger.com/) project.
* For Perl that would be the [CPAN Digger](https://cpan-digger.perlmaven.com/)
* For Ruby you can find gems at [Ruby Digger](https://ruby-digger.code-maven.com/)
