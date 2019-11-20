# Assignment #3 - Managed Contribution
ACIT3890 - BCIT - Fall 2019

## Goals for This Assignment

The purpose of this assignment is for you to work with the tool chain
of an open source project.

This is a group assignment, with teams of two or three.

## Assignment Topics

The following assignment topics,
related to the CodeIgniter 4 project, are available:

### Docker Containers

- goal: preconfigured containers for contributors or developers
- each configured with all tools (unit testing, doc gen, DB, etc)
- follow lead of https://codeigniter4.github.io/CodeIgniter4/installation/running.html#hosting-with-vagrant
- contributors need to use this to run unit testing, code coverage, & gen docs, before submitting PR
- developers need to use this to run app unit testing & test their app in canned environment
- target repos: codeigniter4 (for contributors), appstarter? (for developers), framework?
- config & writeup, for developer testing & test deployment
- strictly speaking, not part of the toolchain, but instead complimenting it

### Sphinx integration

- goal: addition job step(s) to build into travis-ci
- for PRs, look for sphinx errors & block merge if any
- for merges to "develop", rebuild the in-progress user guide & API docs
- for merges to "master", rebuild the deployed user guide & API docs?
- target repo: codeigniter4
- see user_guide_src/README.rst

### Docs Versioning

- goal: simplify doc management, improve usability
- target repo: codeigniter4
- accommodate multiple doc versions, like https://phpunit.readthedocs.io/en/8.3/
- multiple documents (user guide, API, contributing?)
- multiple versions (2, 3.0.x, 3.1.10, 3.1.11, 4.0.0, 4.0.1, ...)
- hosted on github.io? readthedocs? subdomain?
- modified sphinx "make"
- updated sphinx & python versions

### Release build orchestration

- goal: improve stability of release process
- improve & expand the release build script(s)
- cross-repo integration for distros
- follow lead of adminh/workflow & release* scripts
- triggered by "release-xxx" PR??
- release tagging?

### Github Actions

- goal: replace travis-ci with github actions?
- possibly add functionality independent of CI/CD?
- see https://github.com/features/actions
- new kid in town, general release Nov 13 
- see https://github.blog/2019-11-14-powering-community-led-innovation-with-github-actions/
- target repo: website2 (replace travis-ci)
- target repo: module-tests (make it easier for developers)
- how far can we take this?

## Assignment Recipe

### First week

- copy target repo to one of your own, where you have admin rights
- add tools needed so the current CI/CD works
- milestone review, team & JLP

### Second week

- add tools needed to implement your contribution
- draft config for your project
- draft scripts for your project
- draft docs for your project
- milestone review, team & JLP

### Third week

- demonstrate new functionality
- completed config, scripts & docs for your project
- milestone review, team & JLP

## Assignment submission

Your contribution should have already been submitted as one or
more PRs to the target repo.

Submit a writeup of your project, with appropriate links.

Due date: Sunday, Dec 8, 17:30
