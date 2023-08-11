# OSDC - PRC - Pull Request Challenge

Our goal is to encourage people with no or little experience in contributing to open source projects to get involved. We realize that making a big contribution would require a lot of work. Luckily we found thousands of projects with small and well defined opportunities to make a difference.

Some of the tasks only require the change of a single character, for example replacing an insecure link to http://github.com/ by a secure link to https://github.com/. Other tasks are slightly more complex, but still without the need for programming. Then there are other tasks that require programming in Python, Rust, or in JavaScrip. However, even those tasks don't require a deep involvement in the projects.

Open Source runs the world.

We believe that these (relatively) small contributions add up and make the whole open source ecosystem a healthier place.


## The Challenge

* Create 20 Pull-Requests that are **accepted** and **merged** by the end of the challenge.
Neither you nor us can make sure that a given Pull-Request is going to be accepted. We definitely cannot be sure if it will be accepted on time.
Therefore you might need to create more than 20 Pull-Requests.

* In the PR there must be a reasonable explanation of why you think the given change is useful. Next to each task we'll include some suggested explanations. Feel free to rephrase it.

* Once the PR was merged a new comment must be added to the PR explaining about the challenge and the site where you found the specific project.
e.g. for Rust-based projects something like this:

> The idea for this PR was found on the [Rust Digger](https://rust-digger.code-maven.com/) site and it was sent as part of the [OSDC](https://osdc.code-maven.com/prc) challenge for improving the Open Source ecosystem.

* We will manually verify each PR after it was accepted by the owner of the project.

## Dates

This round of the challenge starts on Aug 8 and ends at UTC midnight UTC on Aug 31 2023.

## Who can participate?

* Any person above the age of 18 years at the time of registration who has a GitHub account with an avatar. (Preferable your picture, but a nice drawing will do as well.)
* In this iteration of the challenge we'll allow a very limited number of participants. We'll pick the participants from among the first people who register.
* This iteration of the challenges is limited to the members of the Maakaf community.

## Display of the results

Using your GitHub account we'll generate a page where we display your name and avatar taken from your GitHub account along with all the Pull-Requests
you sent during the period of the challenge.

### Sample display:

<img src="https://avatars.githubusercontent.com/u/48833?v=4" width="60px" title="Gabor Szabo" alt="Gabor Szabo">
Gabor Szabo
* [Update Cargo.toml add repository](https://github.com/simon-bourne/include-doc/pull/1)
* [Update Cargo.toml add repository](https://github.com/alexevanczuk/packs/pull/100)
* [http => https](https://github.com/lightningdevkit/rust-lightning/pull/2444)
* [Update Cargo.toml http => https](https://github.com/tizoc/ocaml-interop/pull/51)
* [Update Cargo.toml remove www](https://github.com/janstarke/mactime2/pull/3)
* [Update Cargo.toml add repository](https://github.com/ndaniels/csc411_image/pull/1)
* [Update Cargo.toml add repository](https://github.com/snowdriftsystem/pkrs/pull/1)
* [Update Cargo.toml add repository](https://github.com/Demonthos/dioxus-storage/pull/5)


## Registration:

* Send and e-mail to [Gabor Szabo](mailto:gabor@szabgab.com) with your GitHub username.
* Wait for the acceptance e-mail from Gabor.
* You can actually go ahead and start sending the Pull-Requests, after all these are valuable contributions even if you don't get accepted to the PRC.

## Questions and Communication

We will use the [PRC stream on OSDC Zulipchat](https://osdc.zulipchat.com/#narrow/stream/399632-prc) for communication.

If you have any question about the challenge or about a specific PR your are about to send or a PR that you already sent.
If you'd like to discuss something with other participants of the challenge.
That's the place!

## Prizes

* The biggest prize you get is the good feeling that you have contributed to Open Source projects and thus made the world a slightly better place.
* Your picture (or avatar) together with your accomplishment will be displayed on our web site.
* The first few participants (exact number will be determined later) who complete the tasks will receive a T-shirt specifically made for this challenge. (We still need to work out the logistics of this, but you'll need to supply your postal address in order to receive this present.)


## Tasks eligible for our challenge

A few comments:

* You will find the tasks in one of the Digger projects developed by Gabor Szabo.
* The Digger sites show the projects starting from the most recently released going back in time. It is better to try to fix projects that were uploaded recently as it is more likely that these projects are actively maintained and thus your pull-request will be accepted in a short period of time.
* The Diggers are updated only by projects that were **released**. This means that even if your contribution was accepted it will take time till it is reflected on the Digger. Don't worry, for the purpose of the challenge we look at the Pull-Request.
* Because the Diggers have a delay, this means that there will be items listed on the Diggers as having some issues even after those have been fixed. So before you send a fix, make sure the problem still exists in the repository.
* Before you send a pull-request make sure there are no existing pull-requests for the same issue. Check both the open pull-requests and the already closed ones. After all sending a duplicate pull-request won't help you in the challenge and will be annoying to the receiver. Even more so with a PR that was already rejected by the author/maintainer of the project.

* The tasks are listed more-or-less in order of complexity / difficulty.

* Some don't require any programming at all, some require knowledge of Python, Rust, or JavaScript.


### Replace http by https in the repository link of a Rust Crate

On [this page](https://rust-digger.code-maven.com/vcs/repo-with-http) we list the Rust Crates (projects) that include a field in their meta-data called `repository` that includes an insecure URL starting with `http://`. GitHub will redirect to the https version of the same page, but why should we have an insecure link if it is redirected anyway. This is really just a one-letter change.

* Follow the link to go to the repository.
* Before you send a PR make sure that the link with the `http://` prefix indeed redirects to the `https://` site.
* The repository will have a file called `Cargo.toml` that will have an entry called `repository`.
* That needs to be changed to use `https`

* Sample explanation: `Though GitHub will automatically redirect the visitors to the site with https, it is probably better to link to that site.`

* [Sample PR](https://github.com/Morganamilo/paru/pull/1018)

### Replace www.github.com by github.com in the repository link of a Rust Crate

The Rust Crates listed on [this page](https://rust-digger.code-maven.com/vcs/github-with-www) include a link to GitHub using a URL starting with www.
This was probably typed in manually as GitHub redirects those URLs to the site without www.

* Follow the link to go to the repository.
* The repository will have a file called `Cargo.toml` that will have an entry called `repository`.
* Change the URL to use `https://github.com`

* Sample explanation: `Though GitHub will automatically redirect the visitors to the site without the www prefix, it is probably better to link to that site without it.`

* [Sample PR](https://github.com/Iron-E/money/pull/1)

### Add the repository field to a Rust Crate.

The crates listed on [this page](https://rust-digger.code-maven.com/no-homepage-no-repo) do not include a link to their public Version Control System (VCS). In order to make it easier to contribute to a project we need to make it easier to find its VCS  (Git repository). Sometimes people forget to add this field, sometimes they don't even know they can add this field. Some people don't even have public VCS, however we can't fix that.

This is a slightly harder task as you need to track down the repository yourself and then add the URL to the Cargo.toml file.

* Click on the name of the owner, you will see all the crates they have released.
* If you are lucky some of those have a link to their repos.
* Alternatively, each user-page has a link to "GitHub" that leads to the GitHub account of that person or team.
* In the GitHub account search for the repository that holds the source code of the crate. You can usually recognize it by its name. Assuming it exists.
* If you found the repository, it should have a file called `Cargo.toml`. In the file there should be a section called `[package]`.
* The section is missing the keyword `repository` with the URL of the repository in double-quotes as its value. That's what you need to add.


* Sample explanation: `Update Cargo.toml add repository url to make crates.io, rust-digger, and other sites link to it.`

* [Sample PR](https://github.com/sebosp/nom-mpq/pull/2)


### Add data to the List of Organizations with Open Source Projects

* We maintain a [list of organization with open source projects](https://osdc.code-maven.com/open-source-by-organizations/). The list includes corporations, higher-education institutions, governments, and non-profit organizations that have at least on "GitHub organization" where they publish open source projects.
* The data is in YAML files in the [this GitHub repository](https://github.com/OSDC-Code-Maven/open-source-by-organizations/).

* Add another YAML file to the `data/github` folder referencing to the "GitHub organization" of real-world organization.
* It might be necessary to add a YAML file to he `data/organizations` folder as well, but that should be only necessary if a new YAML file was added to the `data/github` folder.


### Add instructions for contributors to a Python project

Some open source projects have very detailed instructions in how to set up the local development environment, how to run the tests of the projects and how to contribute to the project. The [Python Flask](https://github.com/pallets/flask) project has a file called `CONTRIBUTING.rst` which is a really good example for this. In the [PyDigger](https://github.com/szabgab/pydigger.com) project we also try to provide detailed information in the `README.md` file.

However, many Python projects don't have such explanation. Especially the smaller and newer ones. So the task is to find such projects, set up the local development environment, run the tests, and then send a PR describing how to do this in either the README file of the project or a separate file called CONTRIBUTING.

* To find a candidates look at [recently updated Python projects](https://github.com/topics/python?l=python&o=desc&s=updated) find one with a few stars (the 5-20 star range might be the best).
* Check if there are already instructions in either the README file or in some other file.
* If there are no instructions yet, clone the project and try to run the tests locally. If you encounter problems, open an issue on the project and either try to continue despite the problem or switch to another project while waiting for the author to respond to the issue.


### Add GitHub Actions (CI) to a Python project

On the PyDigger site there is a page listing [projects on GitHub without CI](https://pydigger.com/search/has-github-no-ci).
A Continuous Integration System (CI) will help the project developers to make sure the tests of a projects are executed on every push to the project and on every pull-request. The most common such system for projects hosted on GitHub is using GitHub Actions.

The task is to create the '.github/workflows' folder in the repository and add a GitHub Action configuration YAML file.

* It might be a good idea to  first clone the project to your computer and make sure you know how to run the tests locally, however this is not a requirement.
* There are a number of ways to start doing so.
    * Fork the project on GitHub and then click on the `Actions` menu item. You'll see a number of suggested workflow files. You can start with one of those.
    * We have a number of [GitHub Action skeletons](https://code-maven.com/github-actions), one of the is for Python. You can use the YAML file from there.
    * You can find a long list of [Python project with GitHub Actions](https://pydigger.com/search/has-github-actions). You can get inspiration from those.
    * If this is the first time you create GitHub Actions, you might want to start by playing around it in one of your own repositories. Maybe one that was created specifically for this purpose.

* Sample explanation: `Add GitHub Actions to make the tests run on every push and every pull-request.`

* [Sample PR](https://github.com/firlast/wsblib/pull/3)
* [Sample PR](https://github.com/Ara101/pcr_optimizer/pull/4)


### Fix an issue in the Rust Digger or in the PyDigger

* The [Rust Digger](https://rust-digger.code-maven.com/) is written in rust and its source code is [here](https://github.com/szabgab/rust-digger).
* The [Pydigger](https://pydigger.com/) is written in Python and its source code is [here](https://github.com/szabgab/pydigger.com).

Both have a number of issues already listed in their respective GitHub repositories. Fixing any of those bugs or implementing a feature request will certainly help this project. Before you get started, please comment on the issue so we can verify that the issue is still relevant and so that we can discuss the implementation.

* There is not sample explanation for this, nor is it necessary to add the post-acceptance explanation to this project.

### Fix an issue in the "Organizations with Open Source Projects"

The [list of organizations](https://osdc.code-maven.com/open-source-by-organizations/) have a number of [open issues](https://github.com/OSDC-Code-Maven/open-source-by-organizations/issues). Implementing one of them will help this project.

* Before you get started on an issue, please first comment on it so we can check it is still relevant and we can discuss the implementation.

* There is not sample explanation for this, nor is it necessary to add the post-acceptance explanation to this project.


