# Overview
Your project should include all of the necessary information about how to test
it.


# Why
Customers will abandon projects that are not easy to test.


# How
Your project should be testable by means of the conventional `go get` and
`go test` dance if it does not use [Cgo](http://blog.golang.org/c-go-cgo),
[SWIG](http://www.swig.org/), or other non-Go code interface.  Anything more
than this represents an unnecessary hurdle.

If the project relies on external process or systems integrations, what those
are, how they are set up, etc. should be documented clearly.  Think carefully
about parallelizing the same test across various instances on the same node and
cluster: the test should be designed in a way to promote isolation from test
runs and the production environment.

A project should thusly strive to ...

  1. have its [continuous build](continuous_build.md) mirror the documentation's
     prescribed processes as closely as possible, if not functioning as a test
     for it;

  2. rely on simple test automation to create a local sandboxed test
     environment (e.g., Makefile-orchestrated shadowed include and library
     directories and search paths to bypass system locations).

In the best of cases, well-designed, unobtuse test automation obviates the need
for extensive test process documentation.


# See Also
[Build Instructions](build_instructions.md)