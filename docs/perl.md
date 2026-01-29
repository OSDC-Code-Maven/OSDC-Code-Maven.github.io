# Perl

* [Events](#events)
* [Chat](#chat)
* [How to select a Perl project to contribute to?](#how-to-select-a-perl-project-to-contribute-to)
* [What and how to contribute to a Python project?](#what-and-how-to-contribute-to-a-perl-project)
* [Project reports](#project-reports)

## Events

This material is being used during the events organized in the [Perl-Maven](https://luma.com/perl-maven) group.

## Chat

* [Zulip](https://osdc.zulipchat.com/)
* [WhatsApp](https://chat.whatsapp.com/LRrkZsSRDvGLLwppyLnKHy)
* [Telegram](https://t.me/PerlMaven)

## How to select a Perl project to contribute to?

* A [perl-based project](https://perlmaven.com/perl-based-open-source-products) that you use. Not a CPAN module, but an application. It is will be nice to be contribute to one of those, but contributing code to a mature project is difficult. Most likely all the simple problems have been already fixed so what you have now are hard. That means you'll have to invest 10s or even 100s of hours. Not something I'd recommend when you are new to open source contribution.
* [MetaCPAN itself](https://metacpan.org/) is one of those perl-based projects, but of course it has a lot of visibility in the Perl community. Do you know the names of the [contributors](https://metacpan.org/about/contributors)?
* [CPAN Dashboard](https://cpandashboard.com/)
    * See the issues
    * Check my report and fix issues there. [SZABGAB](https://cpandashboard.com/SZABGAB/)
    * Check the report of the other people there and fix their issues.
    * Encourage other CPAN authors to send a PR to the Dashboard so they will be also included.
* A CPAN module that you use. However, most likely the modules you use are also rather mature.
* If you contribute to a module that recently had a relase and is maintained, it is much more likely that your work will get feedback and might be even accepted than if you work on a module that has not been maintained for a while. Take for example [DBIx::Class](https://metacpan.org/pod/DBIx::Class). It is one of the most important modules. It has lots of open PRs and open issues, but it was not touched for 3 years. So if you'd like to improve it you might need to take over the maintainence. That's a much bigger job than sending a single PR.
* A direct dependency of a project or a module that you use. Listed in one of the files: `Makefile.PL`, `Build.PL`, `cpanfile`, etc.
* An indirect dependency. [Dependency tree of a Perl module on CPAN](https://perlmaven.com/how-to-fetch-the-cpan-dependency-tree-of-a-perl-module).
* Search on GitHub: [A semi-popular, recently updated Perl project](https://github.com/search?q=stars%3A100..1000+pushed%3A%3E2026-01-10+language%3APerl+&type=repositories&ref=advsearch) `stars:100..1000 pushed:>2026-01-10 language:Perl`
* Pick a popular project and work on stale PRs. That is PRs where there is already good work, but the original author (of the PR) has vanished.
* Adopting a module, especially one in a custodian account, or by one of the authors listed in the InMemoriam module. Adopting a module comes with responsibilities and it is a lot more work than sending a single PR, but there is not other way to make progress with these modules.
    * See this article on how to [adopt a CPAN module](https://neilb.org/2013/07/24/adopt-a-module.html).
    * [(PAUSE Custodial Account)](https://metacpan.org/search?size=20&q=%28PAUSE+Custodial+Account%29)
    * [Acme::CPANAuthors::InMemoriam](https://metacpan.org/pod/Acme::CPANAuthors::InMemoriam)
    * or one of the modules with special owner as described [here](https://pause.perl.org/pause/query?ACTION=pause_operating_model):
        * [ADOPTME](https://rt.cpan.org/Public/Dist/ByMaintainer.html?Name=ADOPTME)
        * [HANDOFF](https://rt.cpan.org/Public/Dist/ByMaintainer.html?Name=HANDOFF)
        * [NEEDHELP](https://rt.cpan.org/Public/Dist/ByMaintainer.html?Name=NEEDHELP)

* [CPAN Digger](https://cpan-digger.perlmaven.com/) helps you find some low-hanging fruits. Recently released distributions...
    * ... that are missing some data from their META files.
    * ... that have no Continuous Integration set up.
    * ... where you can run generate test coverage report and add tests to improve the safety net of the project.


## What and how to contribute to a Perl project?

* CPAN Digger / MetaCPAN
    * It would be probably better to add these to MetaCPAN, but we can start by adding that to CPAN::Digger.
    * Create a web page with the "river" showing the most relied on distributions. (Contribute to this has the widest impact.)
    * Create a page listing all the modules that have the special PAUSE ids listed above, along with their "river" status.
    * Create a page listing all the modules of authors who have passed away (from the InMemoriam module listed above), along with their river status.
    * Taking over and maintaining these is keeping their work live on.

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
        * Use the [perl-tester](https://hub.docker.com/r/perldocker/perl-tester/) Docker container
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

## Tools

```
docker run -it --rm -v$(pwd):/opt  perldocker/perl-tester:5.42 bash
docker run -it --rm -v$(pwd):/opt --user ubuntu szabgab/perl bash
```

## Project reports

* TODO: Eugen Konkov asked for help with PRs to [DBIx::Class](https://metacpan.org/pod/DBIx::Class).
* TODO: [mojoeye](https://github.com/GwynDavies/mojoeye)
* TODO: [Michael R. Davis (MRDVT)](https://metacpan.org/author/MRDVT) mentioned his modules: [Geo::H3](https://metacpan.org/pod/Geo::H3) and [Geo::H3::FFI](https://metacpan.org/pod/Geo::H3::FFI)

* [Algorithm-SlidingWindow](https://metacpan.org/dist/Algorithm-SlidingWindow) - Joshua S. Day (HAX)
    * 2026.01.26
    * PR: [chore: Make sure the META.json gets the data during release](https://github.com/haxmeister/perl-algorithm-slidingwindow/pull/1) - Waiting 🕰️

* [XML-Sig-OO](https://metacpan.org/dist/XML-Sig-OO) - Michael Shipper (AKALINUX)
    * 2026.01.26
    * PR: [chore: Make sure the META.json gets the data during release](https://github.com/akalinux/xml-sig-oo/pull/3) - Waiting 🕰️

* [CtrlO-PDF](https://metacpan.org/dist/CtrlO-PDF) - Andrew Beverley (ABEVERLEY)
    * 2026.01.25
    * PR: [chore: add GitHub Actions to run the tests on every push](https://github.com/ctrlo/CtrlO-PDF/pull/11) - Merged ✅
    * PR: [Extend the test to compare the PDF to an earlier version of the generated file](https://github.com/ctrlo/CtrlO-PDF/pull/13) - Merged ✅
    * Issue: [Can't use an undefined value as an ARRAY reference](https://github.com/ctrlo/CtrlO-PDF/issues/12) - Waiting 🕰️
    * TODO: Add more tests!

* [JSON-Lines](https://metacpan.org/dist/JSON-Lines)
    * 2026.01.24
    * PR: [Add CI workflow for Perl testing](https://github.com/ThisUsedToBeAnEmail/JSON-Lines/pull/4) by Jonathan - Waiting 🕰️

* [Protocol-Sys-Virt](https://metacpan.org/dist/Protocol-Sys-Virt) - Erik Huelsmann (EHUELS)
    * 2026.01.24
    * Issue: [Warning during tests](https://github.com/ehuelsmann/perl-protocol-sys-virt/issues/1) - Fixed ✅
    * PR: [Add CI workflow for Perl testing](https://github.com/ehuelsmann/perl-protocol-sys-virt/pull/2) by Peter Nilsson - Merged ✅
    * [Video recordings](https://perlmaven.com/meta-data-and-github-actions-video) 🎦

* [MIME-Lite](https://metacpan.org/dist/MIME-Lite) - Ricardo SIGNES (RJBS)
    * 2026.01.24
    * PR: [setup GitHub Actions to run the tests on every push and PR](https://github.com/rjbs/MIME-Lite/pull/18) - Waiting 🕰️
    * PR: [Add gitignore for some generated files](https://github.com/rjbs/MIME-Lite/pull/19) - Waiting 🕰️
    * PR: [Add test case with long subject line](https://github.com/rjbs/MIME-Lite/pull/20) - Waiting 🕰️
    * [Video recordings](https://perlmaven.com/testing-mime-lite-video) 🎦
    * Test Coverage: `cover -test`
    * TODO: shall we remove the `fold` function?
    * TODO: Increase test-coverage
    * TODO: Split the packages to individual files.
    * TODO: remove the `#!/usr/bin/perl` line from the tests

* [App-TimeTracker-Command-Jira](https://metacpan.org/dist/App-TimeTracker-Command-Jira) - Michael Kröll (PEPL)
    * The link to the repository was incorrect. I sent and email to Michael Kröll, the author, who pointed me to the correct repository.
    * The project uses Dist::Zilla and will insert the correct address during the next releases. - Waiting 🕰️
    * PR: [Add GitHub Actions](https://github.com/Geizhals-Preisvergleich/App-TimeTracker-Jira/pull/5) - Merged ✅
    * Issue: [Deprecated dzil plugins](https://github.com/Geizhals-Preisvergleich/App-TimeTracker-Jira/issues/6) - Fixed ✅

* [CPAN dashboard](https://cpandashboard.com/) - Dave Cross (DAVECROSS)
    * 2026.01.20
    * [Remove Travis CI](https://github.com/PerlToolsTeam/dashboard/issues/105) - TODO 🎁

* [Business-Westpac](https://metacpan.org/dist/Business-Westpac) - Lee Johnson (LEEJO)
    * 2026.01.20
    * PR: [Update bugtracker and repository URLs in Makefile.PL](https://github.com/leejo/business-westpac/pull/1) - Waiting 🕰️
    * PR: [chore: Add GitHub Actions](https://github.com/leejo/business-westpac/pull/2) - Waiting 🕰️
    * PR: [chore: remove generated files](https://github.com/leejo/business-westpac/pull/3) - Waiting 🕰️

* [LaTeX-Driver](https://metacpan.org/dist/LaTeX-Driver) - Erik Huelsmann (EHUELS)
    * 2026.01.20
    * The tests run locally have some strange output Because of the lack of `makeindex`. - TODO 🎁
    * I started to setup GitHub Actions, but it failed. We might want to explore this in a meeting. - TODO 🎁

* [XML-Easy](https://metacpan.org/dist/XML-Easy) - James E Keenan (JKEENAN)
    * 2026.01.14
    * [Add GitHub Actions to run the tests on every push](https://github.com/jkeenan/p5-XML-Easy/pull/10) - Merged ✅

* [perldocker/perl-tester Docker image](https://hub.docker.com/r/perldocker/perl-tester/)
    * 2026.01.14
    * Issue: [Update text on Docker HUB](https://github.com/Perl/docker-perl-tester/issues/83) - Waiting 🕰️
    * Issue: [Add threaded perl](https://github.com/Perl/docker-perl-tester/issues/84) - Waiting 🕰️  - TODO 🎁
    * 2026.01.20
    * Issue: [Adding more Dist::Zilla plugins](https://github.com/Perl/docker-perl-tester/issues/85) - Waiting 🕰️ - TODO 🎁
    * PR: [add Dist::Zilla::Plugin::CopyReadmeFromBuild](https://github.com/Perl/docker-perl-tester/pull/86) - Merged ✅
    * PR: [add Dist::Zilla::Plugin::HasVersionTests](https://github.com/Perl/docker-perl-tester/pull/88) - Merged ✅
    * Issue: [buster supports only up to perl 5.40 afterward bookworm is needed](https://github.com/Perl/docker-perl-tester/issues/87) - Waiting 🕰️ - TODO 🎁
    * PR: [Use slim-bookworm for perl 5.42 and later](https://github.com/Perl/docker-perl-tester/pull/89) - Waiting 🕰️

* [DBIx-Class-Async](http://metacpan.org/release/DBIx-Class-Async) - Mohammad Sajid Anwar  (MANWAR)
    * 2026.01.08
    * [Make Meta:CPAN link to GitHub issues](https://github.com/manwar/DBIx-Class-Async/pull/1) - Merged ✅
    * [gitignore some generated files](https://github.com/manwar/DBIx-Class-Async/pull/2) - Merged ✅
    * [Add GitHub Workflow and add test dependencies](https://github.com/manwar/DBIx-Class-Async/pull/3) - Merged ✅

* [JQ-Lite](https://metacpan.org/dist/JQ-Lite) - Kawamura Shingo (SHINGO)
    * 2026.01.08
    * During our meeting MANWAR created this PR:
    * [Small improvements to repository to satisfy Kwalite](https://github.com/kawamurashingo/JQ-Lite/pull/503) - Waiting 🕰️

* [Doubly-Linked-PP](https://metacpan.org/dist/Doubly-Linked-PP) - Robert Acock (LNATION)
    * 2026.01.07
    * PR: [add meta-data to allow MetaCPAN to link to public repository](https://github.com/ThisUsedToBeAnEmail/Doubly-Linked/pull/1) - Merged ✅

* [Net-Clacks](https://metacpan.org/dist/Net-Clacks) - Rene Schickbauer (CAVAC)
    * 2026.01.07
    * I sent an email to [Rene Schickbauer](https://github.com/cavac) - Waiting 🕰️

* [MetaCPAN::Client](https://metacpan.org/pod/MetaCPAN::Client) - Mickey Nasriachi (MICKEY)
    * 2026.01.06
    * Issue: [Reference {"relation" => "eq","value" => 14646} did not pass type constraint "Int"](https://github.com/metacpan/MetaCPAN-Client/issues/130) - Fixed ✅

* [Exception-Reporter-Summarizer-PlackRequest](https://metacpan.org/dist/Exception-Reporter-Summarizer-PlackRequest) - Matthew Horsfall (alh) (WOLFSAGE)
    * 2026.01.06
    * Issue: [Why is the repo not included in META.json?](https://github.com/wolfsage/Exception-Reporter-Summarizer-PlackRequest/issues/2) - Waiting 🕰️

* [Geo-IP2Proxy](https://metacpan.org/dist/Geo-IP2Proxy) - IP2Location (LOCATION)
    * 2026.01.05
    * PR: [add meta-data to allow MetaCPAN to link to the repository](https://github.com/ip2location/ip2proxy-perl/pull/1) - Waiting 🕰️

* [Common-CodingTools](https://metacpan.org/dist/Common-CodingTools) - Richard Kelsch (RKELSCH)
    * 2025.12.26
    * PR: [Add links to VCS](https://github.com/richcsst/Common-CodingTools/pull/1) - Waiting 🕰️
    * PR: [Add .gitignore](https://github.com/richcsst/Common-CodingTools/pull/2) - Waiting 🕰️
    * PR: [Add GitHub Actions](https://github.com/richcsst/Common-CodingTools/pull/3) - Waiting 🕰️
    * PR: [Add test](https://github.com/richcsst/Common-CodingTools/pull/4) - Waiting 🕰️

* [JSON::Schema::Validate](https://metacpan.org/pod/JSON::Schema::Validate) - Jacques Deguest (JDEGUEST)
    * 2025.12.01
    * [Showcase: Localised JSON Schema validation in Perl](https://www.reddit.com/r/perl/comments/1p80dne/showcase_localised_json_schema_validation_in_perl/)
    * PR: [add .gitignore file](https://gitlab.com/jackdeguest/json-schema-validate/-/merge_requests/1) - Waiting 🕰️
    * PR: [Setup CI - GitLab pipeline](https://gitlab.com/jackdeguest/json-schema-validate/-/merge_requests/2) - Waiting 🕰️
    * [Open issue](https://gitlab.com/jackdeguest/json-schema-validate/-/issues/4)
    * Also check out the GitLab pipeline of the [Wanted module](https://gitlab.com/jackdeguest/Wanted/)

* [SVG](https://metacpan.org/dist/SVG) - Mohammad Sajid Anwar (MANWAR) + Gabor Szabo (SZABGAB)
    * 2025.11.11
    * As I am a maintainer of this project I could commit and push directly:
    * [add a test case to check loading attributes and trying to load bad attribute](https://github.com/manwar/SVG/commit/7d459c311342172d6b06d189454dfc5760cfaa7d) ✅
    * [add a test case for creating new instance from an existing one](https://github.com/manwar/SVG/commits/master/) ✅

* [Net-Async-Redis-XS](https://metacpan.org/dist/Net-Async-Redis-XS) - Tom Molesworth (TEAM)
    * 2022.12.02
    * Article: [Add GitHub Action CI to the Net-Async-Redis-XS Perl module](https://dev.to/szabgab/day-2-add-github-action-ci-to-the-net-async-redis-xs-perl-module-9oo)
    * PR: [Add GitHub Actions for CI](https://github.com/team-at-cpan/Net-Async-Redis-XS/pull/1) - Merged ✅

* [Win32-Wlan](https://metacpan.org/dist/Win32-Wlan) - Max Maischein (CORION)
    * 2022.12.05
    * Article: [CI for Win32-Wlan Perl module](https://dev.to/szabgab/ci-for-win32-wlan-perl-module-2jnp)
    * PR: [Add GitHub Actions to run the tests on every push](https://github.com/Corion/Win32-Wlan/pull/4) - Merged ✅

* [RDF::KV](https://metacpan.org/pod/RDF::KV) - Dorian Taylor (DORIAN)
    * 2022.12.07
    * Article: [Be pragmatic setting up CI for the RDF::KV](https://dev.to/szabgab/be-pragmatic-setting-up-ci-for-the-rdfkv-56kc)
    * PR: [Add GitHub Actions](https://github.com/doriantaylor/p5-rdf-kv/pull/3) - Waiting 🕰️

* [Perl::Efl](https://metacpan.org/dist/pEFL) - Maximilian Lika (PERLMAX)
    * 2022.12.08
    * Article: [Adding CI to Perl::Efl - sometimes you need to do some extra work](https://dev.to/szabgab/adding-ci-to-perlefl-sometimes-you-need-to-do-some-extra-work-i1d)
    * PR: [Add GitHub Actions](https://github.com/MaxPerl/Perl-Efl/pull/1) - Merged ✅

* [Mojo-UserAgent-Cached](https://metacpan.org/dist/Mojo-UserAgent-Cached) - Nicolas Mendoza (NICOMEN)
    * 2022.12.09
    * Article: [CI for Mojo-UserAgent-Cached and Plack-Middleware-Greylist](https://dev.to/szabgab/day-9-ci-for-mojo-useragent-cached-and-plack-middleware-greylist-4b3p)
    * PR: [Add GitHub Actions](https://github.com/nicomen/mojo-useragent-cached/pull/6) - Merged ✅

* [Plack-Middleware-Greylist](https://metacpan.org/dist/Plack-Middleware-Greylist) - Robert Rothenberg (RRWO)
    * 2022.12.09
    * Article: [CI for Mojo-UserAgent-Cached and Plack-Middleware-Greylist](https://dev.to/szabgab/day-9-ci-for-mojo-useragent-cached-and-plack-middleware-greylist-4b3p)
    * PR: [Add GitHub Actions](https://github.com/robrwo/Plack-Middleware-Greylist/pull/3) - Merged ✅

* [Log::Any](https://metacpan.org/dist/Log-Any) - Doug Bell (PREACTION)
    * 2022.12.14
    * Article: [CI for the Log::Any Perl module](https://dev.to/szabgab/ci-for-the-logany-perl-module-5bl2)
    * PR: [Add GitHub Actions](https://github.com/preaction/Log-Any/pull/94) - Merged ✅

* [Marpa::R2](https://metacpan.org/pod/Marpa::R2) - Jeffrey Kegler (JKEGL)
    * 2022.12.16
    * Article: [Moving from Travis-CI to GitHub Actions for Marpa::R2](https://dev.to/szabgab/day-16-moving-from-travis-ci-to-github-actions-for-marpar2-21cj)
    * Issue: [CI: Does Travis-CI still work for you?](https://github.com/jeffreykegler/Marpa--R2/issues/289)
    * Issue: [IO::Select and other modules in the IO package report version 1.49 whle IO itself is 1.50](https://github.com/Perl/perl5/issues/20609)
    * Issue: [cpan/engine/read_only/tests/* files missing](https://github.com/jeffreykegler/Marpa--R2/issues/291)
    * PR: [Add GitHub Actions](https://github.com/jeffreykegler/Marpa--R2/pull/292) - Rejected ❌ (it will be setup later)

* [Plack-Middleware-LogAny](https://metacpan.org/dist/Plack-Middleware-LogAny) - Sven Willenbuecher (SVW)
    * 2022.12.19
    * Article: [CI for Plack-Middleware-LogAny](https://dev.to/szabgab/day-19-ci-for-plack-middleware-logany-4f4i)
    * PR: [add github actions](https://github.com/XSven/Plack-Middleware-LogAny/pull/1) - Waiting 🕰️

* [MIME-Types](https://metacpan.org/dist/MIME-Types) - Mark Overmeer (MARKOV)
    * 2022.12.24
    * Article: [CI for perl5-MIME-Type](https://dev.to/szabgab/day-24-ci-for-perl5-mime-types-1nf)
    * PR: [Add GitHub Actions](https://github.com/markov2/perl5-MIME-Types/pull/14) - Merged ✅

* [Data::Alias](https://metacpan.org/dist/Data-Alias) - Matthijs van Duin (XMATH)
    * 2022.12.25
    * Article: [CI for Data::Alias in Perl - including threaded perl](https://dev.to/szabgab/day-25-ci-for-dataalias-in-perl-including-threaded-perl-5feh)
    * PR: [Add GitHub Actions](https://github.com/mvduin/perl-Data-Alias/pull/3) - Merged ✅


## Notes

* In the Dist::Zilla world [Dist::Zilla::Plugin::GithubMeta](https://metacpan.org/pod/Dist::Zilla::Plugin::GithubMeta) adds the META information based on a github remote called 'github' or 'origin'.


