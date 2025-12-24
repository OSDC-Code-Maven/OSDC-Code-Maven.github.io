# Rust

## Events

This material is being used during the events organized in the [Code-Mavens](https://www.meetup.com/code-mavens/) Meetup group.

## How to select a Rust project to contribute to?

* Pick a Rust-based project you use.
* Pick a Rust crate that your code directly depends on. They are listed in the `Cargo.toml` file.
* Pick a Rust crate that your code indirectly depends on. They are listed in the `Cargo.lock` file.
* Search on GitHub: [A semi-popular, recently updated Rust project](https://github.com/search?q=stars%3A100..1000+pushed%3A%3E2025-10-01+language%3ARust+&type=repositories&ref=advsearch) `stars:100..1000 pushed:>2025-10-01 language:Rust`
* A recently updated crate or a crate in a category you are interested in. See [Crates.io](https://crates.io/).
* Use the Rust Digger once it is running again.

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


## Projects

* Issue with lots of PRs:
    * [Send PRs to remove www from the github url of the repository in Cargo.toml](https://github.com/szabgab/rust-digger/issues/96)
    * [Send PRs to replace http by https in the github url of the repository in Cargo.toml](https://github.com/szabgab/rust-digger/issues/97)
    * [Send PRs or open issues for Crates with error in Crate.toml](https://github.com/szabgab/rust-digger/issues/100)
    * [Send PRs to Crates to use the repository field instead of the homepage field (July-August 2025)](https://github.com/szabgab/rust-digger/issues/104)


