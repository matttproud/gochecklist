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

  ☐ Compiles: Does the project [build](https://golang.org/cmd/go/)?

  ☐ Tests Pass: Do the projects tests, if any, pass?

  ☐ gofmt Correctness: Is the code
    [formatted](https://blog.golang.org/go-fmt-your-code) correctly?

  ☐ golint Correctness: Is the [linter](https://github.com/golang/lint)
    satisfied?

  ☐ go tool vet Correctness: Is the Go
    [vet](http://godoc.org/golang.org/x/tools/cmd/vet) satisfied?

  ☐ _Go Code Review Comments_ Correctness: Does the project fulfill the
    [upstream code review
    criteria](https://github.com/golang/go/wiki/CodeReviewComments)?

  ☐ Build Instructions: Does the project's documentation instruct how to build
    the project?

  ☐ Test Instructions: Does the project's documentation instruct how to perform
    tests?

  ☐ README Presence: Does the project's include a documentation entrypoint?

  ☐ Directory Names and Packages Match: Does each `package <pkg>` statement
    match the file's containing directory for exported packages?

  ☐ Godoc Correctness: Does the project's
    [godoc](http://blog.golang.org/godoc-documenting-go-code) work correctly?

  ☐ Exporting Only What is Needed: Are any private or internal types
    accidentally exported?  Are all the types one needs to use the project
    correctly exported?

  ☐ Solving a Real Problem: Does the project fulfill a real necessity or
    provide useful learning value?

  ☐ Idiomaticness: Have the authors even bothered to consult
    [Effective Go](https://golang.org/doc/effective_go.html) or the
    [standard library](https://golang.org/pkg/) for prior art?


### Good Citizen
Projects that provide the following, in addition to the above, set themselves
above the pack.

  ☐ Contribution Process: Does the project document a contribution process or
    workflow (e.g., `CONTRIBUTING.md` or use of
    [Gerrit](https://www.gerritcodereview.com/))?  Does the project take
    affirmative steps to avoid the issues documented in the [Unbecoming of a
    Hacker](http://sealedabstract.com/rants/conduct-unbecoming-of-a-hacker/)?

  ☐ Code Review Readiness: Does the project note any special nuances or hints
    for code review?  Are the maintainers sufficiently patient to work with
    newcomers _to the code review process_ or willing to document what is
    expected?

  ☐ Issue Reporting Process: Is a process documented for how and where to
    report problems?

  ☐ Contact Information: Does the project list contacts or mailing lists for
    maintainers and users?

  ☐ API Stability and Maturity Grants: Does the project document its
    stability guarantees, if any?

  ☐ Dependency Vendoring: Does the project vendor its dependencies in some
    fashion?  Bonus points for low-tech. solutions to this.

  ☐ Continuous Build: Does the project use a continuous build (CB)?  Is it
    easy for change proposals to be submitted to the CB?  Does the team
    actively follow the CB?

  ☐ Presence of Useful Tests: Does the project have tests, specifically ones
    that are easy to reason with and maintain?

  ☐ Minimal Third-Party Dependencies: Does the project [avoid unnecessarily
    using external packages when the first-party
    suffice](https://www.youtube.com/watch?v=yi5A3cK1LNA)?

  ☐ Offers API Examples: If the project exposes a public API, have the
    important parts of been [documented as
    _playable_ examples](https://blog.golang.org/examples)?

  ☐ Demonstrates Correct Layout: Does the project lay out its files and
    packages in a [sane and conventional
    way](http://golang.org/doc/code.html#Organization)?  Is it neither
    too sparse nor too dense?  Are the executable binaries contained within
    a `cmd` directory?


### Extra Credit
These points go above and beyond being a good citizen.  Established and mature
projects are likely to fulfill these, though they are certainly not required
for a project to be successful.

  ☐ References Similar Solutions: Does the project's document actively
    reference existing solutions or implementation and offer to compare itself
    with them?

  ☐ Enrolled in Appropriate Directories: Is the project listed in appropriate
    [registries](https://github.com/golang/go/wiki/Projects)?

  ☐ References Formal Research: If the project builds upon formal research,
    does the project's documentation prominently link to the supporting
    documentation describing the research (e.g., peer reviewed article)?

  ☐ Roadmap: Does the project offer a formal roadmap?

  ☐ Benchmarks: In addition to tests, does the project have benchmarks?

  ☐ Blackbox Tests: In addition to [standard tests](http://goo.gl/xQmI6F),
    does the project have [blackbox tests](http://goo.gl/fJ5n7d)?


# Contributing
Contributions are encouraged.  Instructions are documented in
[CONTRIBUTING.md](CONTRIBUTING.md).


# License
This project is [Apache License 2.0](LICENSE).