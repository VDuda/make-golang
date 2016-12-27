# make.go

A Go script that replaces your Makefile

## Features

- Automated versioning of produced binaries.
- Parallel cross compilation for all target platforms.

## Usage

This script is meant to live in your project's root and used with `go run
make.go`.

- `go run make.go` builds a versioned binary for the current platform.
- `go run make.go -os windows -arch amd64` builds a versioned binary for a
  specific platform.
- `go run make.go --release` builds versioned binaries for all target
  platforms.
- `go run make.go --clean` removes produced binaries.

## Reasons to use a make.go instead of a more succinct Makefile

- Your project has a non trivial building procedure that could benefit from
  being expressed in robust Go code.
- You want the increased portability of Go.
- You like writing Go!