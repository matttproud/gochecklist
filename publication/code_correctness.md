# Overview
Your project's source code should be formatted correctly and validated for
correctness. The Go project and open-source community provides a comprehensive
set of tools for improving the quality of your code.

# Why
`gofmt` removes the need for you to worry about manually formatting your
code.  The accepted convention is to use `gofmt` in all cases.

`go tool vet` reports potential irregularities in your project that won't be
caught at compile-time but rather may be seen at runtime (e.g., shadowing, or
[variadic function argument
mismatches](https://golang.org/ref/spec#Function_types), etc.).

`golint` reports irregularities in your project.  Many of the checks it
performs deal with how well-formed the project is in relation to upstream
conventions and standards, especially with idioms. The majority of mature Go ]
projects follow these conventions, so not following them thereby makes a
project unjustifiably unidiomatic.

# How
An easy way to apply these correctness tools to your codebase is to use
the [gometalinter](https://github.com/alecthomas/gometalinter). It
automates the downloading, installation and processing of your code with
tools such as `gofmt`, `golint`, and `go vet` (among others).

    $ go get github.com/alecthomas/gometalinter
    $ gometalinter --install --update
    $ gometalinter ./...

You may want to consider creating a
[presubmission](https://www.chromium.org/developers/how-tos/depottools/presubmit-scripts) or [git
commit](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) test that
to ensure automated compliance.

# Exceptions
It may be unwise to apply this rule to generated code (e.g.,
[go generate](http://blog.golang.org/generate) or from IDL, like
[Protocol Buffers](https://developers.google.com/protocol-buffers/)).
