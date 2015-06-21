# Overview
Your project's source code should be formatted with
[gofmt](http://blog.golang.org/go-fmt-your-code).


# Why
Go strictly removes the need for you to worry about manually formatting your
code.  The accepted convention is to use `gofmt` in all cases.

Projects that do not comply with `gofmt` often are treated as pariahs by the
community, irrespective of the technical correctness of their implementation.


# How
Regular use of `gofmt` on your code ensures compliance.  Further, as the
language evolves, you may want to acquaint yourself with the automated code
simplifier: `gofmt -s`.

    $ gofmt -w -s your_file.go

You may want to consider creating a
[presubmission](https://www.chromium.org/developers/how-tos/depottools/presubmit-scripts) or [git
commit](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) test that
to ensure automated compliance.

Many text editors have gofmt integration.  If you use Emacs, see
[go-mode](https://github.com/dominikh/go-mode.el), for instance.


# Exceptions
It may be unwise to apply this rule to generated code (e.g.,
[go generate](http://blog.golang.org/generate) or from IDL, like
[Protocol Buffers](https://developers.google.com/protocol-buffers/)).
