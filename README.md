# covermerge

The `covermerge` tool takes the results from multiple Golang test coverage profiles and merges them into a single coverage profile.

usage
-----

    covermerge [coverprofiles...]

covermerge takes the source coverprofiles as the arguments (output from `go test -coverprofile coverage.out`, or similar testing framework) and outputs a merged version of the files to standard out. You can only merge profiles that were generated from the
same source code. If there are source lines that overlap or do not merge, the process will exit with an error code.
