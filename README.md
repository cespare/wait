# This package is deprecated

This package provides commonly-needed functionality and it saw use for several
years. Today, though, new code should not use this package. Instead, use
[golang.org/x/sync/errgroup](https://pkg.go.dev/golang.org/x/sync/errgroup).
Errgroup is a popular package and it has a nicer API for some use cases.
It uses contexts for cancelation, which are the standard mechanism today.
(The context package did not exist when github.com/cespare/wait was written.)

# wait

[![GoDoc](https://godoc.org/github.com/cespare/wait?status.svg)](https://godoc.org/github.com/cespare/wait)

wait is a Go package that provides `Group`, an extended version of
`sync.WaitGroup`.

wait is similar to two other packages of which I'm aware:

* [tomb](http://godoc.org/gopkg.in/tomb.v2) is a popular choice which is quite
  similar but has more features and a more complicated set of states
  (alive/dying/dead).
* Camlistore has [syncutil.Group](http://camlistore.org/pkg/syncutil/#Group)
  which records multiple errors but does not support cancellation.
