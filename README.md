# basics

Whenever I start a new project, I find that there is a bit of drudgery
involved in just setting up the basics, things like:

* Creating initial autoconf, automake files
* Parsing command-line options
* Setting up a logging mechanism
* Specifying dependencies for common libraries, e.g. boost

This repository includes starting points for new projects.

# Quickstart

Starting with a fetch `git init` repository, to start with say the C++ basics:

    git remote add basics git@github.com:thinkski/basics.git
    git fetch basics
    git read-tree --prefix=/ -u basics/master:cpp/

Then

    ./autogen.sh
    ./configure
    make
    
This will produce an executable `src/foobar` which you can run:

    ./src/foobar --help


## Tips

* Make sure you have Boost installed. On Mac OS X, if using Homebrew:

    brew install boost
    
* Make sure you have the supplimental Autoconf macros installed. On Mac OS X, if using Homebrew:

    brew install autoconf-archive
