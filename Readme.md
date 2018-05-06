bwt-unified-build
=================

Docker container combining a number of different tools and based on
[gitlab sonar scanner][]. Feel free to make use of this resource but understand
that it is used internally as part of a build chain and not in the scope of any
supported product by those involved in it's production. It is recommended that
you manage your own forked copy as this one may change to suit our build chain
without notice, and thus should be considered unstable.

Purpose
-------

Docker overlays are not currently supported by many build chain tools and source
management suites. This container serves to reduce resources required during
builds internally and mitigate redundant loads on public resources used(mainly
OS repos and infrastructure) for software packages with exponential testing
growth rates. One example being a library with support for dozens of embedded
chipsets, platforms and protocol wrappers where each possible build
configuration combination needs unit testing.

Used Works
----------

* [gitlab sonar scanner][]: [Local readme][gitlab sonar scanner readme]

Packages
--------

* Language support
  * gcc
  * g++
  * python
* Build tools
  * build-essential
  * cmake
* Code analysis
  * cppcheck
  * lcov
  * gcovr
  * valgrind
  * vera++
* Misc
  * git
* Dependencies
  * libexpat1-dev
  * openjdk-8-jre-headless

LICENSE
=======

All the code contained in this repository is licensed under a GNU-GPLv3 license.

Copyright Matt Barnett 2018.

See [LICENSE][] for more details

[gitlab sonar scanner]: https://github.com/ciricihq/gitlab-sonar-scanner
[gitlab sonar scanner readme]: ./Readme.gitlab-sonar-scanner.md

[docker hub]: https://hub.docker.com/r/nullm/bwt-unified-build
[LICENSE]: ./LICENSE
