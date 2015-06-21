# Overview
Each directory should contain one package, and the package's name should match
that directory's name.


# Why
The entire standard library conforms to this, and almost all well-formed
third-party Go projects adhere to this.  This it to say, it is an unspoken
convention.

Further, deviations impose an onerous cognitive burden for users.  Suppose
you have the following filesystem listing:


  /Development/project/src/frobnicator/frob.go

    // Package frob frobnicates thingamabobbers.
    package frob

    func Frobnicate(i ...interface{}) {}


What happens when you want to use this ficticious package?  Here's your package
here.


  /Development/project/src/thingamajigger/jigger.go


    // Package thingamajigger makes thingers.
	package thingamajigger

    import "frobnicator"

    func Jigger(i ...interface{}) {
	  frob.Frobnicate(i...)
	}


What's the first thing you notice?  You specified the import by way of its path:
`import "frobnicator"`, but how do you
[reference](https://golang.org/ref/spec#QualifiedIdent) it?  Note how we must
call it by the full-qualified identifier of `frob.Frobnicate`.  That's annoying,
because it does not match the base directory name: `frobnicator`.

Why is this annoying?  For one, it breaks with convention.  For two, it requires
you to manually inspect the `package <pkg>` statement of a file in the target
directory and track additional information.

Your customers are time-poor, so think about any additional mismatch as an
unjustifiable cost you impose on them.


# Exceptions
There are a couple of exceptions to this:

  1. `package main`: entrypoints have their own rules.

  2. [test examples](https://blog.golang.org/examples): these are their own
     special snowflakes.
