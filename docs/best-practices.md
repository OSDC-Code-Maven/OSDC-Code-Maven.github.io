# Best practices in software development

In reality I don't like the expression of "best practices" as in my opinion what is best for a given project will depend a lot on its circumstances that vary from project to project.
However, we can talk about several practices each project would benefit from.

Software collapse (which is also called software rot) is a phenomenon many of us have encountered. In a nutshell it is software starting to break due to external circumstances.

An extreme case would be a software running on a computer without any changes. By itself the software won't start to misbehave, but the hardware will at one point fail. Then you'll have to replace that. Most likely you will NOT be able to buy the exact same hardware. On newer hardware you'll have to install a newer version of the operating system. With that new versions of compilers and libraries will come that don't support the original versions of the libraries you used. This can easily cause your software to misbehave or to entirely stop working.

Even less extreme and more frequent changes can impact your ability to run your code without any changes. e.g. if one of the compilers or libraries you used has to be upgraded due to a security vulnerability.


We can differentiate between projects based on the frequency of their use. One one hand there are software projects (e.g. your browser) that millions of people use daily,
on the other extreme there are software projects one writes to run an experiment that is used for a very short period of time. However you, or other researchers might want to repeat the same experiment a few years later and might want to use this software again.

Software that is in daily use easily justifies constant maintenance. Any change in the environment will quickly trigger a bug report that can be used to address the issue. On the other hand in software that is rarely used you will only notice the breakage caused by the environment when the software is used again. By that time the gap might have become too big to bridge and the knowledge to maintain the software might have been lost.


In the academic world this will be couple with the (lack of) capability to repeat an experiment in similar circumstances.
