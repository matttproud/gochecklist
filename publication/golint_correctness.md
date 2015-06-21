# Overview
Your project's source code should be free of warnings from
[golint](https://github.com/golang/lint).

`golint` is a fantastic way to automate convention adherence checking for Go
projects.  It is updated frequently and usually accurate.


# Why
`golint` reports irregularities in your project.  Many of the checks it
performs deal with how well-formed the project is in relation to upstream
conventions and standards, especially with idioms.

The majority of mature Go projects follow these conventions, so not following
them thereby makes a project unjustifiably unidiomatic.


# How
Install `golint` and use it:

    $ go get -u github.com/golang/lint/golint
    $ golint your/package


You may want to consider creating a
[presubmission](https://www.chromium.org/developers/how-tos/depottools/presubmit-scripts) or [git
commit](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) test that
to ensure automated compliance.


# Exceptions
It may be unwise to apply this rule to generated code (e.g.,
[go generate](http://blog.golang.org/generate) or from IDL, like
[Protocol Buffers](https://developers.google.com/protocol-buffers/)).
