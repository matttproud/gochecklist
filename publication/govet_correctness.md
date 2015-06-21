# Overview
Your project's source code should be free of notices from the 
[go vet](http://godoc.org/golang.org/x/tools/cmd/vet).

`go tool vet` is a great way to use static analysis find potential bugs in Go
code.


# Why
`go tool vet` reports potential irregularities in your project that won't be
caught at compile-time but rather may be seen at runtime (e.g., shadowing, or
[variadic function argument
mismatches](https://golang.org/ref/spec#Function_types), etc.).


# How
    $ go tool vet


You may want to consider creating a
[presubmission](https://www.chromium.org/developers/how-tos/depottools/presubmit-scripts) or [git
commit](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) test
to ensure no new errors are introduced.

