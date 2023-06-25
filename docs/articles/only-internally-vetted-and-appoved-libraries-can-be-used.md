---
title: Only internally vetted and approved Open Source libraries can be used.
published: true
published_at: 2023-06-26 08:26 +0000
---

This article is based on a conversation I had with a manager at one of the large hi-tech companies.
My conversation partner preferred that I leave out the name of the company.

I asked how can the developers use 3rd party open source libraries?

Developers can't install libraries directly from the 3rd party registry, nor from GitHub. Nor from anywhere else on the internet.
They can only use libraries and only the versions of those libraries that were vetted and approved by a team of the company specialized to screen open source libraries.
They have an in-house repository of the libraries, developers can only install from there.

If you wish to use a library that is not approved yet, you will need to submit a request to that team.
They will evaluate the library and all of its dependencies in terms of license and code security.

They will also ask you why do you need that particular library. What alternatives did you see and why would you like to use specifically this library.

They will will also take in account the level of maintenance this project gets.
After all, including a library that is not maintained will soon become a liability as the team finds out that some features are missing
or when they find bug or security vulnerabilities.

This of course makes it much harder to use Open Source libraries. It also means that this security team has to have members who can read
and properly evaluate code written in all the programming languages used in the organization.

This creates a pressure to reduce the number of programming languages in the organization. In itself this is not a problem,
but it might reduce the possibility to explore other languages that might fit better specific tasks.

Only relatively large companies can afford to have such a team that is not working on the products of the company.
