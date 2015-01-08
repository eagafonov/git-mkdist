# git-mkdist

Helper script to create a all-in-one-single-commit-git-repo to deploy without pushing whole history to server.

It does a few simple steps:

* clones current repo
* checkouts same commit as original repo 
* checkout submodules 
* wipes original git stuff
* init new repo and commit all files

## Install

put `git-mkdist` script from root to your PATH

## Run

To make a dist, run `git mkdist` in git repo root you want make a dist from. Dist appears in forlder `.dist`
     
## Configuration

A few git config variables are used

* mkdist.email, mkdist.name - author email/name to be used in resulting git repo. Default author string is 'gitmkdist <gitmkdist@localhost>'
* mkdist.keep-dists=(true|false) - Keep `.dists` content while creating new dists. Default is `false`

# TODO

* Config var to specify target repo (dev/test/production)
* Get target commit as command line option
* Autoupdate script from github
