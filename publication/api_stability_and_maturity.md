# API Stability and Maturity

One of the great features of the Go programming langugae is the commitment to compatibility as decribed on the document [Go 1 and the Future of Go Programs](https://golang.org/doc/go1compat). Most importantly, the policy states that programs written for Go 1.0 should continue to work without modification in Go 1.1, 1.2, etc. Although it isn't necessary to for every Go library to commit to this level of forward compatibility, it is important to keep this expectation in mind when releasing your own project.

## Project Maturity and Stability

Without defining a strict terminology, it is still useful to inform your users of the overall maturity of your library. We suggest including a "Stability and Compatibility" section in your top-level README.md file that summarizes the current status. For example:

1. The Foo library is currently undergoing heavy development with frequent, breaking API changes.
2. The Foo library is getting close to a stable release, and we are trying to minimize breaking API changes. However, we cannot make any guarantees at this time.
3. The Foo library is considered stable. We will make every effort to ensure API compatibility in future releases.

## Semantic Versioning

There internets are full of heated debates on the topic of version naming. We suggest that Go library authors adopt a versioning scheme that is compatible with the [SemVer 2.0 Standard](http://semver.org):

```text
MAJOR.MINOR.PATCH
```

* `MAJOR`: Incremented when you make incompatible API changes. Use `1` for the first API-stable release.
* `MINOR`: Incremented when you make backwards-compatible functionality additions or modifications. This also includes fixes that have a non-trivial impact on performance - CPU, memory  or storage.
* `PATCH`: Incremented when you apply bug fixes or documentation changes. Should not have significant impact on functionality or performance.

Another convention to consider adopting is that post-1.0-release breaking API changes should always require a change in the import path. This could be accomplished using either of the following approaches:

### Including a version indicator in the import path. 

The downside to this approach is that you have to plan for the migration by including the `v1`' package in your path from the very beginning. Keep in mind that this is not recommended by API design experts such as [Martin Fowler](http://martinfowler.com/articles/enterpriseREST.html).

```go
import (
  "github.com/:username/:projectname/v1/:apiname"
  "github.com/:username/:projectname/v2/:apiname"
)
```

### Creating a new top-level repository.

Instead of introducing a version element to your import path, fork your repository to create a version 2.

```go
import (
  "github.com/:username/:projectname/:apiname"
  "github.com/:username:projectname2/:apiname"
)
```

## Version Labeling and Import Paths

We suggest that you use the version labeling and naming mechanism provided by our version control system. Git users should use [git tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging), Mercurial users should also use [hg tagging](https://mercurial.selenic.com/wiki/Tag), and Subversion users should use [svn tagging](http://svnbook.red-bean.com/en/1.7/svn-book.html#svn.branchmerge.tags).

In general, you should avoid including the `v` text in the version tags. So intead of `v1.0.3`, you should tag your release with `1.0.3`.
