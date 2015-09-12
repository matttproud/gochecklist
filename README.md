# Purpose
The purpose of this project is to marshal various conventions and practices
around publishing [Go](https://www.golang.org) projects in one place.

It is written in a way where you can check-off each bullet point as you go
along.

  ☑ Do I have a [plush Go Gopher](https://goo.gl/w8qQLV)?


# List of Recommendations and Guidelines
Below are the recommendations as partitioned by topical area with brief
explanations.  Detailed explanations for each of these will be documented
externally.


## Publication and Reiteration
This subsection is dedicated to the acts of initially publishing a project or
having an established project undergo a major reiteration.  The practical difference between these points is the former means one-time blanket application of
these principles; whereas the latter means ensuring that subsequent changes to
the project uphold and fulfill these principles.


### Minimum Criteria
The failure to fulfill any of these usually causes one to discard a project and
look for alternatives.

  ☐ Licensed: Does the project have a license?

  See: [publication/licensing.md](publication/licensing.md)

  ☐ Compiles: Does the project [build](https://golang.org/cmd/go/)?

  See: [publication/compilation.md](publication/compilation.md)

  ☐ Tests Pass: Do the projects tests, if any, pass?

  See: [publication/tests_pass.md](publication/tests_pass.md)

  ☐ Code Correctness: Does the code pass format, lint and error checking tools?

  See: [publication/code_correctness.md](publication/code_correctness.md)

  ☐ _Go Code Review Comments_ Correctness: Does the project fulfill the
    [upstream code review
    criteria](https://github.com/golang/go/wiki/CodeReviewComments)?

  See: [publication/code_review_comments.md](publication/code_review_comments.md)

  ☐ Build Instructions: Does the project's documentation instruct how to build
    the project?

  See: [publication/build_instructions.md](publication/build_instructions.md)

  ☐ Test Instructions: Does the project's documentation instruct how to perform
    tests?

  See: [publication/test_instructions.md](publication/test_instructions.md)

  ☐ README Presence: Does the project's include a documentation entrypoint?

  See: [publication/documentation_entrypoint.md](publication/documentation_entrypoint.md)

  ☐ Directory Names and Packages Match: Does each `package <pkg>` statement's
    package name match the containing directory name?

  See: [publication/dir_pkg_match.md](publication/dir_pkg_match.md)

  ☐ Godoc Correctness: Does the project's
    [godoc](http://blog.golang.org/godoc-documenting-go-code) work correctly?

  See: [publication/godoc_correctness.md](publication/godoc_correctness.md)

  ☐ Exporting Only What is Needed: Are any private or internal types
    accidentally exported?  Are all the types one needs to use the project
    correctly exported?

  See: _TODO_

  ☐ Solving a Real Problem: Does the project fulfill a real necessity or
    provide useful learning value?

  See: _TODO_

  ☐ Idiomaticness: Have the authors even bothered to consult
    [Effective Go](https://golang.org/doc/effective_go.html) or the
    [standard library](https://golang.org/pkg/) for prior art?

  See: _TODO_


### Good Citizen
Projects that provide the following, in addition to the above, set themselves
above the pack.

  ☐ Contribution Process: Does the project document a contribution process or
    workflow (e.g., `CONTRIBUTING.md` or use of
    [Gerrit](https://www.gerritcodereview.com/))?  Does the project take
    affirmative steps to avoid the issues documented in the [Unbecoming of a
    Hacker](http://sealedabstract.com/rants/conduct-unbecoming-of-a-hacker/)?

  See: _TODO_

  ☐ Code Review Readiness: Does the project note any special nuances or hints
    for code review?  Are the maintainers sufficiently patient to work with
    newcomers _to the code review process_ or willing to document what is
    expected?

  See: _TODO_

  ☐ Issue Reporting Process: Is a process documented for how and where to
    report problems?

  See: _TODO_

  ☐ Contact Information: Does the project list contacts or mailing lists for
    maintainers and users?

  See: _TODO_

  ☐ API Stability and Maturity Grants: Does the project document its
    stability guarantees, if any?

  See: [publication/api_stability_and_maturity.md](publication/api_stability_and_maturity.md)


  ☐ Dependency Vendoring: Does the project vendor its dependencies in some
    fashion?  Bonus points for low-tech. solutions to this.

  See: _TODO_

  ☐ Continuous Build: Does the project use a continuous build (CB)?  Is it
    easy for change proposals to be submitted to the CB?  Does the team
    actively follow the CB?

  See: _TODO_

  ☐ Presence of Useful Tests: Does the project have tests, specifically ones
    that are easy to reason with and maintain?

  See: _TODO_

  ☐ Minimal Third-Party Dependencies: Does the project [avoid unnecessarily
    using external packages when the first-party
    suffice](https://www.youtube.com/watch?v=yi5A3cK1LNA)?

  See: _TODO_

  ☐ Offers API Examples: If the project exposes a public API, have the
    important parts of been [documented as
    _playable_ examples](https://blog.golang.org/examples)?

  See: _TODO_

  ☐ Demonstrates Correct Layout: Does the project lay out its files and
    packages in a [sane and conventional
    way](http://golang.org/doc/code.html#Organization)?  Is it neither
    too sparse nor too dense?  Are the executable binaries contained within
    a `cmd` directory?

  See: _TODO_


### Extra Credit
These points go above and beyond being a good citizen.  Established and mature
projects are likely to fulfill these, though they are certainly not required
for a project to be successful.

  ☐ References Similar Solutions: Does the project's document actively
    reference existing solutions or implementation and offer to compare itself
    with them?

  See: _TODO_

  ☐ Enrolled in Appropriate Directories: Is the project listed in appropriate
    [registries](https://github.com/golang/go/wiki/Projects)?

  See: _TODO_

  ☐ References Formal Research: If the project builds upon formal research,
    does the project's documentation prominently link to the supporting
    documentation describing the research (e.g., peer reviewed article)?

  See: _TODO_

  ☐ Roadmap: Does the project offer a formal roadmap?

  See: _TODO_

  ☐ Benchmarks: In addition to tests, does the project have benchmarks?

  See: _TODO_

  ☐ Blackbox Tests: In addition to [standard tests](http://goo.gl/xQmI6F),
    does the project have [blackbox tests](http://goo.gl/fJ5n7d)?

  See: _TODO_


# Contributing
Contributions are encouraged.  Instructions are documented in
[CONTRIBUTING.md](CONTRIBUTING.md).


# License
This project is [Apache License 2.0](LICENSE).
