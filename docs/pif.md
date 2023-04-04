# Pay It Forward

Have you just received a Pull-request or have you just received a useful issue? Has someone just contributed to your open source project?

Would you want to "return the favor" or would you rather "pay it forward"?

We believe that a small contribution to an Open Source project of someone else can go a long way. You might already put a lot of energy in your projects,
but a contributing to someone else can have a network effect. It will help the recipient of the contribution and we can ask that person to pay it forward
and contribute to yet another project.

On this page you'll find a collection of ideas on the types of contributions you could make. Most of them are rather small that don't need a lot of time from you
and most of them don't require any (deep) involvement in the project.

When you open the piull-request or maybe even better when it gets accepted we would ask you to add a comment to the pull-request mentioning this project
and inviting the recipient of your pull-request to "pay it forward". You can either link to this page or the [issue](https://github.com/OSDC-Code-Maven/OSDC-Code-Maven.github.io/issues/5)
that explains it.


## Remove unnecessary files

* Find repositories that include files that should not be committed to git. (e.g. generated files, caches etc.) Remove them, create a `.gitignore` file explain how it works.
* See this article: [Billions of unnecessary files in GitHub](https://dev.to/szabgab/billions-of-unnecessary-files-in-github-i85)


## Add meta data to Python projects

* [PyDigger](https://pydigger.com/) - Add missing author, license, description, and link to VCS field.

## Add meta data to Ruby projects

* [Ruby Digger](https://ruby-digger.code-maven.com/)

## Add meta data to Perl projects

* [CPAN Digger](https://cpan-digger.perlmaven.com/)
    * [Include VCS link in META data](https://perlmaven.com/how-to-add-link-to-version-control-system-of-a-cpan-distributions)
    * [Add license to META data](https://perlmaven.com/how-to-add-the-license-field-to-meta-files-on-cpan)
    * [Add contributors to META data](https://perlmaven.com/how-to-add-list-of-contributors-to-the-cpan-meta-files)

## Add instruction of local development

We believe that if we make it easier for others to contribute to our open source projects thent there is a higher chances some will do so.
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
