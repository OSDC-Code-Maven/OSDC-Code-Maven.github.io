# Perl

## Events

This material is being used during the events organized in the [Perl-Maven](https://luma.com/perl-maven) group.

## Chat

* [OSDC Zulip](https://osdc.zulipchat.com/)


## How to select a Perl project to contribute to?

* A [perl-based project](https://perlmaven.com/perl-based-open-source-products) that you use.
* [MetaCPAN itself](https://metacpan.org/)
* A module that you use.
* A direct dependency of a project or a module that you use. Listed in one of the files: `Makefile.PL`, `Build.PL`, `cpanfile`, etc.
* An indirect dependency. [Dependency tree of a Perl module on CPAN](https://perlmaven.com/how-to-fetch-the-cpan-dependency-tree-of-a-perl-module).
* Search on GitHub: [A semi-popular, recently updated Perl project](https://github.com/search?q=stars%3A100..1000+pushed%3A%3E2025-10-01+language%3APerl+&type=repositories&ref=advsearch) `stars:100..1000 pushed:>2025-10-01 language:Perl`
* [CPAN Digger](https://cpan-digger.perlmaven.com/)


## What and how to contribute to a Perl project?

* Link to VCS: Make sure [MetaCPAN links to the VCS](https://perlmaven.com/how-to-add-link-to-version-control-system-of-a-cpan-distributions) of the module. If not, try to locate the source of the module and send a PR updating the meta-data of the project. If you can't find it, then you might want to send an email to the author asking if the project has a public repository.
* Testing
    * Try to run the tests locally or better yet in a [Docker container](https://github.com/szabgab/perl-docker-on-ubuntu).
    * [Testing articles](https://perlmaven.com/testing)
    * [Testing book](https://perlmaven.com/perl-testing/)
    * Test::More
    * Generate test coverage report  [Devel::Cover](https://metacpan.org/pod/Devel::Cover)
* CI
    * If there are tests, check if there is a CI?
    * [Perl and CI](https://perlmaven.com/ci)
        * [GitHub Actions](https://perlmaven.com/setup-github-actions)
    * Setting up CI:
    * GitHub Actions
    * GitLab pipelines
        * [examples](https://perlmaven.com/gitlab-ci)
        * [video](https://perlmaven.com/gitlab-pipelines-and-ci-for-perl-developers)
* Dependencies
    * Add [dependabot](https://docs.github.com/en/code-security/dependabot/) for GitHub Actions.
    * I think Dependabot does not support Perl.
* Code formatting
    * [Perl::Tidy](https://metacpan.org/pod/Perl::Tidy)
* Linting
    * [Perl::Critic](https://metacpan.org/pod/Perl::Critic)
    * [Getting Started with Perl::Critic](https://perlmaven.com/getting-started-with-perl-critic)
* Fuzz testing
    * The [App-Test-Generator](https://metacpan.org/dist/App-Test-Generator) distirbution comes with a tool called [fuzz-harness-generator](https://metacpan.org/dist/App-Test-Generator/view/bin/fuzz-harness-generator)
* Mutation testing
    * [Devel::Mutator](https://metacpan.org/pod/Devel::Mutator)
* Code complexity analyzis
    * [Perl::Critic::CognitiveComplexity](https://metacpan.org/pod/Perl::Critic::CognitiveComplexity)
    * [Analizo::Metric::StructuralComplexity](https://metacpan.org/pod/Analizo::Metric::StructuralComplexity)
    * [Perl::Lint](https://metacpan.org/pod/Perl::Lint) has [Perl::Lint::Policy::Subroutines::ProhibitExcessComplexity](https://metacpan.org/pod/Perl::Lint::Policy::Subroutines::ProhibitExcessComplexity)
    * [Perl-Metrics-Lite](https://metacpan.org/dist/Perl-Metrics-Lite)
* Code reading
* Refactoring

See also [this issue](https://github.com/OSDC-Code-Maven/OSDC-Code-Maven.github.io/issues/5) about the goals.

* [Adopt a CPAN module](https://neilb.org/2013/07/24/adopt-a-module.html)
* Take over a CPAN module.

## Projects

* Eugen Konkov asked for help with PRs to [DBIx::Class](https://metacpan.org/pod/DBIx::Class).

* [Doubly-Linked-PP](https://metacpan.org/dist/Doubly-Linked-PP)
    * 2026.01.07
    * PR: [add meta-data to allow MetaCPAN to link to public repository](https://github.com/ThisUsedToBeAnEmail/Doubly-Linked/pull/1) - Waiting 🕰️

* [Net-Clacks](https://metacpan.org/dist/Net-Clacks)
    * 2026.01.07
    * I sent an email to [Rene Schickbauer](https://github.com/cavac) - Waiting 🕰️

* [MetaCPAN::Client](https://metacpan.org/pod/MetaCPAN::Client)
    * 2026.01.06
    * Issue: [Reference {"relation" => "eq","value" => 14646} did not pass type constraint "Int"](https://github.com/metacpan/MetaCPAN-Client/issues/130) - Fixed ✅

* [Exception-Reporter-Summarizer-PlackRequest](https://metacpan.org/dist/Exception-Reporter-Summarizer-PlackRequest)
    * 2026.01.06
    * Issue: [Why is the repo not included in META.json?](https://github.com/wolfsage/Exception-Reporter-Summarizer-PlackRequest/issues/2) - Waiting 🕰️

* [Geo-IP2Proxy](https://metacpan.org/dist/Geo-IP2Proxy)
    * 2026.01.05
    * PR: [add meta-data to allow MetaCPAN to link to the repository](https://github.com/ip2location/ip2proxy-perl/pull/1) - Waiting 🕰️

* [Common-CodingTools](https://metacpan.org/dist/Common-CodingTools)
    * 2025.12.26
    * PR: [Add links to VCS](https://github.com/richcsst/Common-CodingTools/pull/1) - Waiting 🕰️
    * PR: [Add .gitignore](https://github.com/richcsst/Common-CodingTools/pull/2) - Waiting 🕰️
    * PR: [Add GitHub Actions](https://github.com/richcsst/Common-CodingTools/pull/3) - Waiting 🕰️
    * PR: [Add test](https://github.com/richcsst/Common-CodingTools/pull/4) - Waiting 🕰️

* [JSON::Schema::Validate](https://metacpan.org/pod/JSON::Schema::Validate)
    * 2025.12.01
    * [Showcase: Localised JSON Schema validation in Perl](https://www.reddit.com/r/perl/comments/1p80dne/showcase_localised_json_schema_validation_in_perl/)
    * PR: [add .gitignore file](https://gitlab.com/jackdeguest/json-schema-validate/-/merge_requests/1) - Waiting 🕰️
    * PR: [Setup CI - GitLab pipeline](https://gitlab.com/jackdeguest/json-schema-validate/-/merge_requests/2) - Waiting 🕰️
    * [Open issue](https://gitlab.com/jackdeguest/json-schema-validate/-/issues/4)
    * Also check out the GitLab pipeline of the [Wanted module](https://gitlab.com/jackdeguest/Wanted/)

* [SVG](https://metacpan.org/dist/SVG)
    * 2025.11.11
    * As I am a maintainer of this project I could commit and push directly:
    * [add a test case to check loading attributes and trying to load bad attribute](https://github.com/manwar/SVG/commit/7d459c311342172d6b06d189454dfc5760cfaa7d) ✅
    * [add a test case for creating new instance from an existing one](https://github.com/manwar/SVG/commits/master/) ✅

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
    * PR: [Add GitHub Actions](https://github.com/jeffreykegler/Marpa--R2/pull/292) - Rejected ❌ (it will be setup later)

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


## Notes

* In the Dist::Zilla world [Dist::Zilla::Plugin::GithubMeta](https://metacpan.org/pod/Dist::Zilla::Plugin::GithubMeta) adds the META information based on a github remote called 'github' or 'origin'.


