# OSDC - PRC - Pull Request Challenge

Our goal is to encourage people with no or little experience in contributing to open source projects to get involved. We realize that making a big contribution would require a lot of work. Luckily we found thousands of projects with small and well defined opportunities to contribute.

Some of the tasks only require the change of a single character, for example replacing an insecure link to http://github.com/ by a secure link to https://github.com/. Other tasks are slightly more complex, but even those don't require deep involvement in the projects.

We believe that these small contributions add up and make the whole open source ecosystem a healthier place.

## The Challenge

* Create 20 Pull-Requests that are **accepted** and **merged** by the end of the challenge.
Neither you nor us can make sure that a given Pull-Request is going to be accepted. We definitely cannot be sure if it will be accepted on time.
Therefore you might need to create more than 20 Pull-Requests.

* In the PR there must be a reasonable explanation of why you think the given change is useful. Next to each task we'll include some suggested explanations. Feel free to rephrase it.

* Once the PR was merged a new comment must be added to the PR explaining about the challenge and the site where you found the specific project.
e.g. for Rust-based projects something like this:

```
The idea for this PR was found on the [Rust Digger](https://rust-digger.code-maven.com/) site and it was sent as part of the [OSDC](https://osdc.code-maven.com/prc) challenge for improving the Open Source ecosystem.
```

## Dates

This round of the challenge starts on Aug 8 and ends at UTC midnight UTC on Aug 31 2023.

## Who can participate?

* Any person above the age of 18 years at the time of registration who has a GitHub account with an avatar. (Preferable your picture, but a nice drawing will do as well.)
* In this iteration of the challenge we'll allow a very limited number of participants. We'll pick the participants from among the first people who register.
member of the Maakaf community
* This iteration of the challenges is limited to the members of the Maakaf community.

## Display of the results

Using your GitHub account we'll generate a page where we display your name and avatar taken from your GitHub account along with all the Pull-Requests
you sent during the period of the challenge.

![](https://avatars.githubusercontent.com/u/48833?v=4)


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
* The first few participants (exact number will be determined later) who complete the tasks will receive a T-shirt specifically made for this challenge. (We stil need to work out the logistics of this, but you'll need to supply your postal address in order to receive this present.)


## Tasks eligible for our challenge

A few comments:

* You will find the tasks in one of the Digger projects developed by Gabor Szabo.
* The Digger sites show the projects starting from the most recently released going back in time. It is better to try to fix projects that were uploaded recently as it is more likely that these projects are actively maintained and thus your pull-request will be accepted in a short period of time.
* The Diggers are updated only by projects that were **released**. This means that even if your contribution was accepted it will take time till it is reflected on the Digger. Don't worry, for the purpose of the challenge we look at the Pull-Request.
* Because the Diggers have a delay, this means that there will be items listed on the Diggers as having some issues even after those have been fixed. So before you send a fix, make sure the problem still exists in the repository.
* Before you send a pull-request make sure there are no existing pull-requests for the same issue. Check both the open pull-requests and the already closed ones. After all sending a duplicate pull-request won't help you in the challenge and will be annoying to the receiver. Even more so with a PR that was already rejected by the author/maintainer of the project.


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

