# Perl


## How to select a Perl project to contribute to?

* [CPAN Digger](https://cpan-digger.perlmaven.com/)


## What and how to contribute to a Perl project?

* Testing
    * [Testing articles](https://perlmaven.com/testing)
    * [Testing book](https://perlmaven.com/perl-testing/)
    * Test::More
    * Generate test coverage report  [Devel::Cover](https://metacpan.org/pod/Devel::Cover)
* Linting
* code formatting
    * [Perl::Tidy](https://metacpan.org/pod/Perl::Tidy)
* Fuzz testing
* Mutation testing
* Code complexity analyzis
* Refactoring
* Setting up CI
    * GitHub Actions
    * GitLab pipelines
        * [examples](https://perlmaven.com/gitlab-ci)
        * [video](https://perlmaven.com/gitlab-pipelines-and-ci-for-perl-developers)
* Updating the GitHub actions if necessary
* Add [dependabot](https://docs.github.com/en/code-security/dependabot/) for GitHub Actions.
* Add dependabot for the code-base.
* Code reading

See also [this issue](https://github.com/OSDC-Code-Maven/OSDC-Code-Maven.github.io/issues/5) about the goals.

## Projects

* [JSON::Schema::Validate](https://metacpan.org/pod/JSON::Schema::Validate)
    * 2025.12.01
    * [Showcase: Localised JSON Schema validation in Perl](https://www.reddit.com/r/perl/comments/1p80dne/showcase_localised_json_schema_validation_in_perl/)
    * PR: [add .gitignore file](https://gitlab.com/jackdeguest/json-schema-validate/-/merge_requests/1) - Waiting 🕰️
    * PR: [Setup CI - GitLab pipeline](https://gitlab.com/jackdeguest/json-schema-validate/-/merge_requests/2) - Waiting 🕰️
    * [Open issue](https://gitlab.com/jackdeguest/json-schema-validate/-/issues/4)
    * Also check out the GitLab pipeline of the [Wanted module](https://gitlab.com/jackdeguest/Wanted/)

* [Net-Async-Redis-XS](https://metacpan.org/dist/Net-Async-Redis-XS)
    * 2022.12.02
    * Article: [Add GitHub Action CI to the Net-Async-Redis-XS Perl module](https://dev.to/szabgab/day-2-add-github-action-ci-to-the-net-async-redis-xs-perl-module-9oo)
    * PR: [Add GitHub Actions for CI](https://github.com/team-at-cpan/Net-Async-Redis-XS/pull/1) - Merged ✅

* [Win32-Wlan](https://metacpan.org/dist/Win32-Wlan)
    * 2022.12.05
    * Article: [CI for Win32-Wlan Perl module](https://dev.to/szabgab/ci-for-win32-wlan-perl-module-2jnp)
    * PR: [Add GitHub Actions to run the tests on every push](https://github.com/Corion/Win32-Wlan/pull/4) - Merged ✅

* [RDF::KV](https://metacpan.org/pod/RDF::KV)
    * 2022.12.07
    * Article: [Be pragmatic setting up CI for the RDF::KV](https://dev.to/szabgab/be-pragmatic-setting-up-ci-for-the-rdfkv-56kc)
    * PR: [Add GitHub Actions](https://github.com/doriantaylor/p5-rdf-kv/pull/3) - Waiting 🕰️

* [Perl::Efl](https://metacpan.org/dist/pEFL)
    * 2022.12.08
    * Article: [Adding CI to Perl::Efl - sometimes you need to do some extra work](https://dev.to/szabgab/adding-ci-to-perlefl-sometimes-you-need-to-do-some-extra-work-i1d)
    * PR: [Add GitHub Actions](https://github.com/MaxPerl/Perl-Efl/pull/1) - Merged ✅

* [Mojo-UserAgent-Cached](https://metacpan.org/dist/Mojo-UserAgent-Cached)
    * 2022.12.09
    * Article: [CI for Mojo-UserAgent-Cached and Plack-Middleware-Greylist](https://dev.to/szabgab/day-9-ci-for-mojo-useragent-cached-and-plack-middleware-greylist-4b3p)
    * PR: [Add GitHub Actions](https://github.com/nicomen/mojo-useragent-cached/pull/6) - Merged ✅

* [Plack-Middleware-Greylist](https://metacpan.org/dist/Plack-Middleware-Greylist)
    * 2022.12.09
    * Article: [CI for Mojo-UserAgent-Cached and Plack-Middleware-Greylist](https://dev.to/szabgab/day-9-ci-for-mojo-useragent-cached-and-plack-middleware-greylist-4b3p)
    * PR: [Add GitHub Actions](https://github.com/robrwo/Plack-Middleware-Greylist/pull/3) - Merged ✅

* [Log::Any](https://metacpan.org/dist/Log-Any)
    * 2022.12.14
    * Article: [CI for the Log::Any Perl module](https://dev.to/szabgab/ci-for-the-logany-perl-module-5bl2)
    * PR: [Add GitHub Actions](https://github.com/preaction/Log-Any/pull/94) - Merged ✅

* [Marpa::R2](https://metacpan.org/pod/Marpa::R2)
    * 2022.12.16
    * Article: [Moving from Travis-CI to GitHub Actions for Marpa::R2](https://dev.to/szabgab/day-16-moving-from-travis-ci-to-github-actions-for-marpar2-21cj)
    * Issue: [CI: Does Travis-CI still work for you?](https://github.com/jeffreykegler/Marpa--R2/issues/289)
    * Issue: [IO::Select and other modules in the IO package report version 1.49 whle IO itself is 1.50](https://github.com/Perl/perl5/issues/20609)
    * Issue: [cpan/engine/read_only/tests/* files missing](https://github.com/jeffreykegler/Marpa--R2/issues/291)
    * PR: [Add GitHub Actions](https://github.com/jeffreykegler/Marpa--R2/pull/292) - Rejected ❌

* [Plack-Middleware-LogAny](https://metacpan.org/dist/Plack-Middleware-LogAny)
    * 2022.12.19
    * Article: [CI for Plack-Middleware-LogAny](https://dev.to/szabgab/day-19-ci-for-plack-middleware-logany-4f4i)
    * PR: [add github actions](https://github.com/XSven/Plack-Middleware-LogAny/pull/1) - Waiting 🕰️

* [MIME-Types](https://metacpan.org/dist/MIME-Types)
    * 2022.12.24
    * Article: [CI for perl5-MIME-Type](https://dev.to/szabgab/day-24-ci-for-perl5-mime-types-1nf)
    * PR: [Add GitHub Actions](https://github.com/markov2/perl5-MIME-Types/pull/14) - Merged ✅

* [Data::Alias](https://metacpan.org/dist/Data-Alias)
    * 2022.12.25
    * Article: [CI for Data::Alias in Perl - including threaded perl](https://dev.to/szabgab/day-25-ci-for-dataalias-in-perl-including-threaded-perl-5feh)
    * PR: [Add GitHub Actions](https://github.com/mvduin/perl-Data-Alias/pull/3) - Merged ✅



