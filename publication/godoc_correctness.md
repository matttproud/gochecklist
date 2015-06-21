# Overview
Your project's source code should be readable with 
[godoc](http://blog.golang.org/godoc-documenting-go-code).


# Why
Many a Go user studies a package for the first time by reading its documentation
through the [godoc](http://godoc.org/golang.org/x/tools/cmd/godoc) tool.  This
is where cursory make-or-break opinions are formed.  Thusly it is important to
leave a good impression!

Good and correct inline documentation is convention with both standard libraries
and the most respected third-party Go projects out there.


# How
You should first get an idea of how the documentation looks locally.  This can
be done with the `godoc` tool.  The inspection should be done both from the
perspective of your command line client &hellip;

    $ godoc your/package | less

&hellip; and your web browser

    $ godoc -http=':6060'

Your review should include the following topics:

  1. spelling,

  2. grammar,

  3. militant conciseness,

  4. convention, and

  5. presentation.

