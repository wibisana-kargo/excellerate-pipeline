# Kargo Excellerate CI/CD Assignment


Your assignment for this section is to create 2 Github Actions pipelines. Consider the long term maintainability for the pipelines. In this case, some forms of abstraction may be preferred, such as using a Makefile or Composite Actions.

The requirement details for each pipe will be detailed below.

## Before Starting

Before working on this assignment, we suggest fulfilling these pre-requisites to help you on your tasks

- Create a fork of this repository
- Choose 1 language for your assignment (go/python/nodejs), your pipelines should fulfill both requirements for the selected language
- Install git
- (optional) Work on a unix machine, build environment and examples are made for a unix machine
- (optional) Docker hub account (personal)
- (optional) Install docker
- (optional) Install related language to try relevant commands locally
  - golang
  - python
  - nodejs

## Tasks

Your tasks are to create 2 pipelines that fulfill the following requirements. Stubs are provided.

* Build
  * Pipeline should trigger on all pushes to master branch.
  * Build and tag a docker image of the app. Give the docker image a tag corresponding to the git commit hash.
  * Push the image to a repository. Either:
    * Personal docker hub account (public repository), or
    * (Bonus) kargotech-prod GCR.
* Test
  * Pipeline should trigger on all PR.
  * Run unit test for selected app
    * Golang: go test
    * Python: pytest
    * Nodejs: npm test (mocha)
  * (Bonus) Get code coverage and store the result on Actions summary 
