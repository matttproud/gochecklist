# Overview
Your project should include all of the necessary information about how to build
it.


# Why
Customers abandon projects that are not easy to build.


# How
Your project should be buildable by means of the conventional `go get` and
`go build` dance if it does not use [Cgo](http://blog.golang.org/c-go-cgo),
[SWIG](http://www.swig.org/), or other non-Go code interface.  Anything more
than this represents an unnecessary hurdle.

Most readers can stop here.

If non-Go code and its dependencies are thrown in the mix, things become more
complicated.  A project should thusly strive to ...

  1. have its [continuous build](continuous_build.md) mirror the documentation's
     prescribed processes as closely as possible, if not functioning as a test
     for it;

  2. document its non-Go code dependencies thoroughly (e.g., what versions are
     used, how they are configured, etc.);

  3. be flexible with respect to where the non-Go dependencies are installed in
     case one wants to avoid system packages in favor of local vendored ones;

  4. rely on simple build automation to create a local sandboxed build
     environment (e.g., Makefile-orchestrated shadowed include and library
     directories and search paths to bypass system locations).

In the best of cases, well-designed, unobtuse build automation obviates the need
for extensive build process documentation.

The moral of the story is that non-Go code integrations impose a tremendous
burden on authors, maintainers, and users.  Tread carefully.

These prescriptions may sound heavyweight, but they are necessary.  Continuous
build environments often callously change their underlying platform from
underneath users.  As the author of a project, you want to insulate yourself
from this unnecessary churn as much as possible.
