---
layout: page
title: About this project
permalink: /about/
---

You can find a longer description of my work as posts [here]({{ site.baseurl }}{% link index.md %})

You can find more information about this project goal on the [issue page of my fork][my-fork-issues]

What got included
-----------------

Here is a list of pull request that got merged in netjsonconfig during my gsoc with a short description

* Extend Renderer documentation [#67][67] 
* Advices on contributing to the project [#69][69]
* Added command to validate input [#71][71]
* Explain errors in NetJSON input using the json schema [#84][84]
* AirOS backend and tests [#91][91]

What was excluded
-----------------

Here is a list of pull request that we didn't merge in netjsonconfig during my gsoc with a short description

* More documentation on how to start working on a custom backend [backend-for-dummies][backend-for-dummies]
* Use the json-schema to set default values was issue [#81][81] and I had a [solution][computer-do-the-thing] that wasn't feasible to merge as it would break all the tests by adding all the values, even the optionals

Bugs still out there
--------------------

Here is a list of WONTFIX or difficult bugs that I discovered and would have gotten the project sidetracked

* Merging custom json-schema does not override default definitions [#83][83]

What is working
---------------

We can configure the device in bridge mode, the basis for router mode are there but I have been unable to connect after. This is not an issue with the code but with my understanding of the update procedure. I am sure we are missing something in the procedure as the device is not bricked after the update.

What is missing
---------------

Many converters are still using safe defaults, you can find the updated list [here][airos-netjsonconfig]


[airos-netjsonconfig]: http://netjsonconfig.openwisp.org/en/airos/backends/airos.html#converters-with-defaults
[backend-for-dummies]: https://github.com/EdoPut/netjsonconfig/tree/backend-for-dummies
[computer-do-the-thing]: https://github.com/EdoPut/netjsonconfig/tree/computer-do-the-thing
[my-fork-issues]: https://github.com/EdoPut/netjsonconfig/issues?utf8=%E2%9C%93&q=is%3Aissue%20
[67]: https://github.com/openwisp/netjsonconfig/pull/67
[69]: https://github.com/openwisp/netjsonconfig/pull/69
[71]: https://github.com/openwisp/netjsonconfig/pull/71
[81]: https://github.com/openwisp/netjsonconfig/issues/81
[83]: https://github.com/openwisp/netjsonconfig/issues/93
[84]: https://github.com/openwisp/netjsonconfig/pull/84
[91]: https://github.com/openwisp/netjsonconfig/pull/91
