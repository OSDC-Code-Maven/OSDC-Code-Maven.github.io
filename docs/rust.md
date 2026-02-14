# Rust

## Events

This material is being used during the events organized in the [Code-Mavens](https://www.meetup.com/code-mavens/) Meetup group.

## Docker

* [Source of Docker image we use](https://github.com/szabgab/rust-docker-on-ubuntu)


## Chat

* [OSDC Zulip](https://osdc.zulipchat.com/)
* [Telegram](https://t.me/RustMaven)


## How to select a Rust project to contribute to?

* Pick a Rust-based project you use.
* Pick a Rust crate that your code directly depends on. They are listed in the `Cargo.toml` file.
* Pick a Rust crate that your code indirectly depends on. They are listed in the `Cargo.lock` file.
* Search on GitHub: [A semi-popular, recently updated Rust project](https://github.com/search?q=stars%3A100..1000+pushed%3A%3E2025-10-01+language%3ARust+&type=repositories&ref=advsearch) `stars:100..1000 pushed:>2025-10-01 language:Rust`
* A recently updated crate or a crate in a category you are interested in. See [Crates.io](https://crates.io/).
* Pick a popular project and work on stale PRs. That is PRs where there is already good work, but the original author (of the PR) has vanished.
* Use the [Rust Digger](https://rust-digger.code-maven.com/) once it is running again.

## What and how to contribute to a Rust project?

* Link to VCS: Find the listing of the crate on [Crates.io](https://crates.io/) and check if it links to its VCS. If not, try to find the repository and send a PR to include the link. If you cannot find the repo then you cannot contribute to the project. You might want to send a message to the author expressing interest in contributing and asking if there is a public repository.
* Testing:
    * Run the tests of the crate locally or better yet in a Docker container. Report if there is any test failures or if there are difficulties in running the tests.
    * Generate [test coverage report using tarpaulin](https://rust.code-maven.com/testing/test-coverage-with-tarpaulin.html).
    * Find holes in the test coverage, write tests to check parts of the code that were not tested yet.
* CI
    * If there are tests, check if there is a CI?
    * Setting up CI: GitHub Actions or GitLab pipelines.
* Dependencies
    * Add [dependabot](https://docs.github.com/en/code-security/dependabot/) for GitHub Actions and for the dependencies.
* Code formatting
    * Using `cargo fmt --check` check if the code is well formatted. If not open an issue suggestion to do it.
* Linting
    * Use `cargo clippy` to run the linter. Configure Clippy.
* Fuzz testing
    * [test-fuzz](https://crates.io/crates/test-fuzz)
    * [fuzzing](https://rustprojectprimer.com/testing/fuzzing.html)
* Mutation testing with [cargo-mutants](https://mutants.rs/)
    * See article on [Mutation testing librsvg](https://viruta.org/mutation-testing-librsvg.html)
* Code complexity analyzis
    * [complexity](https://docs.rs/complexity/latest/complexity/)
* Refactoring
* Code reading

## Low hanging fruits from the Rust Digger

* [Has homepage but no repo](https://rust-digger.code-maven.com/has-homepage-but-no-repo handled) 2025-08-15   current count 3,619 - 3,608 - 3,728

```
chore: Update Cargo.toml use repository instead of homepage

chore: use `repository` field instead of `homepage` field
```

```
According to the [manifest](https://doc.rust-lang.org/cargo/reference/manifest.html)
it seems the `repository` field is preferable.
More explanation https://github.com/szabgab/rust-digger/issues/119
```

* [GitHub with www](https://rust-digger.code-maven.com/vcs/github-with-www)  Since 2021-01-01 Till  2025-07-03  current count: 253

```
chore: Minor change to remove www from github url in Cargo.toml
```

```
GitHub redirects to the address without www anyway, so let's put that in Cargo.toml.
See also https://github.com/szabgab/rust-digger/issues/96
```

* [Repo with http ](https://rust-digger.code-maven.com/vcs/repo-with-http) Since 2020-01-01 Till 2025-06-28   Current count: 355

```
chore: Minor change to use https in the github url in Cargo.toml
```

```
GitHub redirects to the address with https anyway, so let's put that in Cargo.toml.
See also https://github.com/szabgab/rust-digger/issues/97
```

* [Has Cargo.toml errors](https://rust-digger.code-maven.com/has-cargo-toml-errors)

```
chore: Fix typo in Cargo.toml
```

```
Given the most recent change here I know it is unlikely you will publish a new version of this crate on crates.io,
but in case you you might want to fix this typo in `Cargo.toml`.
See also: https://github.com/szabgab/rust-digger/issues/100
```

* [Lower-case cargo.toml](https://rust-digger.code-maven.com/lower-case-cargo-toml) Most recent is 2023-08-10, Maybe I should send PRs or open issues?

* [No homepage, no repo](https://rust-digger.code-maven.com/no-homepage-no-repo) handled: 2025-06-06   current count: 28,911

```
chore: Update Cargo.toml add repository field
```

```
To make it easier for potential contributors and automated tools to find the repository.
More explanation: https://github.com/szabgab/rust-digger/issues/89
```

## TODO

## Projects

* [zed](https://zed.dev/)
    * 2026.02.14
    * Issue: [panic while running inside Docker](https://github.com/zed-industries/zed/issues/49131) - Waiting 🕰️
    * Discussion: [Allow the user to provide an alternative path to devcontainer.json](https://github.com/zed-industries/zed/discussions/49182) - Waiting 🕰️

* [short_uuid](https://crates.io/crates/short_uuid)
    * 2026.02.02
    * Issue: [What is flickrBase58?](https://github.com/radim10/short-uuid/issues/10) - Waiting 🕰️
    * 2026.02.09
    * Issue: [GitHub Action does not run](https://github.com/radim10/short-uuid/issues/11)
    * PR: [GitHub workflow](https://github.com/radim10/short-uuid/pull/12) - Merged ✅
    * PR: [Improve test by comparing result to expected short](https://github.com/radim10/short-uuid/pull/13) - Merged ✅
    * We had trouble understanding if the test that fails should even work. Basically we did not know when is a string an "invalid short uuid"?
        * For sure it is when it has characters outside the vocabulary.
        * For sure if converting to uuid fails.
        * But if converting to uuid requires padding. Is that invalid? It is unclear so we did not "fix" the test.
        * We had some major trouble as VS code keept indicating compilation errors and we could not figure out what is the right way to write some code. It tooks some time till I tried to run `cargo build` on the terminal just to find out the code compiles. Restarting VS code then fixed that, but it was very unpleasant. Especially in-front of other people.
    * [Sample GitHub Workflow](https://doc.rust-lang.org/cargo/guide/continuous-integration.html) in the Cargo Book.
    * [cargo-dist](https://crates.io/crates/cargo-dist)
    * [GitHub Workflow](https://github.com/MeirKriheli/rusmux/blob/master/.github/workflows/release.yml) of the [rusmux](https://crates.io/crates/rusmux) project by Meir Kriheli
* [spyne](https://crates.io/crates/spyne) - Zaid Ahmed (ZA1815)
    * 2026.01.26
    * PR: [chore: Add repository URL to Cargo.toml](https://github.com/ZA1815/spyne/pull/1) - rejected ❌ - no comment
    * [Video recordings](https://rust.code-maven.com/adding-repository-to-cargo-toml-video)
    * Issue: [unresolved imports crate::serialization::serialize](https://github.com/ZA1815/spyne/issues/2) - Fixed ✅
    * PR: [Fix the capitalization of some names in the test](https://github.com/ZA1815/spyne/pull/3) - rejected ❌ - no comment
    * PR: [Add basic GitHub Actions to run the tests on every push and every pull-request](https://github.com/ZA1815/spyne/pull/4) - rejected ❌ - no comment

* [kftray-helper](https://crates.io/crates/kftray-helper) - Henrique Cavarsan (hcavarsan)
    * 2026.01.26
    * PR: [Add repository field to Cargo.toml](https://github.com/hcavarsan/kftray/pull/560) by Karol Skorek (skht) - Merged ✅
    * [Video recordings](https://rust.code-maven.com/adding-repository-to-cargo-toml-video)
    * Learn: [llvm-cov](https://crates.io/crates/cargo-llvm-cov) for test coverage

* [csv](https://crates.io/crates/csv)
    * 2026.01.18
    * Issue: [Remove Travis from the repository](https://github.com/BurntSushi/rust-csv/issues/418) - Waiting 🕰️
    * PR: [chore: Remove Travis-CI and Appveyor related badges](https://github.com/BurntSushi/rust-csv/pull/419) - Waiting 🕰️
    * PR: [chore: Add dependabot to monitor github actions](https://github.com/BurntSushi/rust-csv/pull/420) - rejected ❌ - author feels dependabot is too noisy.
    * Issue: [Remove or update ci/script.sh](https://github.com/BurntSushi/rust-csv/issues/421) - Waiting 🕰️
    * Find the most recent change of a file (even if the file is already deleted): `git rev-list -n 1 HEAD -- <file_path>`
    * Learn: [husky](https://typicode.github.io/husky/)
    * We tried to run Tarpaulin on this repo, but it failed. - TODO 🎁

* [xml](https://crates.io/crates/xml)
    * 2026.01.18
    * PR: [chore: Add dependabot configuration](https://github.com/kornelski/xml-rs/pull/63) - Merged ✅
    * PR: [chore: gitignore the files that might be generated by tarpaulin](https://github.com/kornelski/xml-rs/pull/65) - Merged ✅
    * PR: [chore: add cargo fmt to the CI to ensure it is always checked](https://github.com/kornelski/xml-rs/pull/66) - rejected ❌ - some strong (and negative) opinion on `rustfmt`.
    * Issue: [Fix cargo clippy issues and add cargo clippy to the ci](https://github.com/kornelski/xml-rs/issues/67) - Waiting 🕰️  - TODO 🎁
    * Issue: [Remove the master branch](github.com/kornelski/xml-rs/issues/64) - done  ✅

* [rama](https://crates.io/crates/rama)
    * 2026.01.18
    * This was mentioned by one of the participants in our live session.
    * I tried to run the tests both with `cargo test` and `just test`. Both failed and I did not have the energy to further investigate. - TODO 🎁

* states-rs
    * 2026.01.16
    * [chore: user repository field instead of homepage field](https://github.com/WolverinDEV/states-rs/pull/1) - Waiting 🕰️

* [dvb](https://crates.io/crates/dvb)
    * 2026.01.16
    * [chore: Add repository URL to Cargo.toml](https://github.com/hoodie/dvb-rs/pull/8) - Merged ✅

* [hannibal-derive](https://crates.io/crates/hannibal-derive)
    * 2026.01.16
    * [chore: Add repository field to Cargo.toml](https://github.com/hoodie/hannibal/pull/57) - Merged ✅

* [resource-bound](https://crates.io/crates/resource-bound)
    * 2026.01.16
    * [chore: Fix the repository URL in Cargo.toml](https://github.com/oOp995/resource-bound/pull/1) - Merged ✅

* [ferrotype](https://crates.io/crates/ferrotype)
    * 2026.01.13
    * PR: [Add GitHub action to run the test on every push](https://github.com/iamnbutler/ferrotype/pull/1) - Waiting 🕰️

* [stand](https://crates.io/crates/stand)
    * 2026.01.13
    * [Add GitHub Actions to run the tests on every push](https://github.com/ueneid/stand/pull/26) - Waiting 🕰️
    * Learn: [serena](https://github.com/oraios/serena)

* [k8s-openapi-ext-rs](https://crates.io/crates/K8s-openapi-ext)
    * 2026.01.13
    * PR: [add github actions with flags as needed](https://github.com/rkubectl/k8s-openapi-ext-rs/pull/2) - Merged ✅
    * Learn: [CodeRabbit](https://www.coderabbit.ai/)
    * Learn: [just](https://crates.io/crates/just)
    * Learn: [mise](https://mise.jdx.dev/)

* [PyDigger](https://pydigger.code-maven.com/)
    * 2026.01.09
    * During the Python session we encountered some issues with PyDigger and one of the participants sent this PR:
    * [feat: add support for License Expression field](https://github.com/szabgab/pydigger.rs/pull/3) - Merged ✅

* [mkenv](https://crates.io/crates/mkenv/)
    * Issue: [Test panics when USER env var is not set in a Docker container](https://github.com/ahmadbky/mkenv/issues/5) - Waiting 🕰️
    * PR: [make sure the tarpaulin test coverage report is not added to git](https://github.com/ahmadbky/mkenv/pull/6) - Merged ✅
    * PR: [add a test case that calls the default_fmt_val method](https://github.com/ahmadbky/mkenv/pull/7) - Waiting 🕰️
    * ---
    * PR: [run cargo fmt --check in the CI](https://github.com/ahmadbky/mkenv/pull/8) - Merged ✅
    * PR: [add dependabot to send PRs when new version of the actions or the crates are available](https://github.com/ahmadbky/mkenv/pull/9) - Merged ✅
    * PR: [run cargo clippy in the CI](https://github.com/ahmadbky/mkenv/pull/11) - Waiting 🕰️

* [axum](https://crates.io/crates/axum)
    * 2025.03.12
    * [Help with the basics of deployment](https://github.com/tokio-rs/axum/discussions/3561) - TODO 🎁 Read this!
    * [Add test to chat example](https://github.com/tokio-rs/axum/pull/3278) - TODO 🎁 - review
    * [Improving the examples - adding tests](https://github.com/tokio-rs/axum/issues/3263) - TODO 🎁
    * [[test] the static-file-server example](https://github.com/tokio-rs/axum/pull/3297) - TODO 🎁

* [anndata](https://github.com/scverse/anndata)
    * 2025.11.20
    * [Add type-checking](https://github.com/scverse/anndata/pull/2174) - TODO 🎁
    * [How to generate test coverage report?](https://github.com/scverse/anndata/issues/2233) - TODO 🎁

* [mdbook](https://crates.io/crates/mdbook)
    * [Remove index.html suffix](https://github.com/rust-lang/mdBook/issues/1251) - TODO 🎁
    * [Include `*.ipynb` files and not only `*.md` files](https://github.com/rust-lang/mdBook/issues/2480) - TODO 🎁

* Issue with lots of PRs:
    * [Send PRs to remove www from the github url of the repository in Cargo.toml](https://github.com/szabgab/rust-digger/issues/96)
    * [Send PRs to replace http by https in the github url of the repository in Cargo.toml](https://github.com/szabgab/rust-digger/issues/97)
    * [Send PRs or open issues for Crates with error in Crate.toml](https://github.com/szabgab/rust-digger/issues/100)
    * [Send PRs to Crates to use the repository field instead of the homepage field (July-August 2025)](https://github.com/szabgab/rust-digger/issues/104)


