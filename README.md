# Go Training

[![Build Status](https://travis-ci.com/anz-bank/go-training.svg?branch=master)](https://travis-ci.com/anz-bank/go-training)
[![Coverage](https://codecov.io/gh/anz-bank/go-training/branch/master/graph/badge.svg)](https://codecov.io/gh/anz-bank/go-training)
[![GolangCI](https://golangci.com/badges/github.com/anz-bank/go-training.svg)](https://golangci.com/r/github.com/anz-bank/go-training)

This project is a playground for hands-on golang training.

## Prerequisites

-   Install `go 1.11` according to [official installation instruction](https://golang.org/doc/install)
-   Clone this project outside your `$GOPATH` to enable [Go Modules](https://github.com/golang/go/wiki/Modules)
-   Install `golangci-lint` according to [instructions](https://github.com/golangci/golangci-lint#local-installation)

## Build, execute, test, lint

Build and install this project with

    go install ./...

Execute its binary with

    0_hello_world

Test it with

    go test ./...

Lint it with

    golangci-lint run

Review coverage with

    go test -coverprofile=coverage.out ./... && go tool cover -html=coverage.out

## Pre-PR checklist

-   Ensure your source code changes
    -   Build
    -   Test
    -   Lint
    -   Have 100% test coverage
-   Ensure [good commit messages](https://chris.beams.io/posts/git-commit/)
    -   Separate subject from body with a blank line
    -   Limit the subject line to 60 characters
    -   Use the imperative mood in the subject line
    -   Do not end the subject line with a period
    -   Wrap the body at 80 characters
    -   Use the body to explain what and why vs. how
    -   Use `git rebase -i COMMIT_HASH` to rework your commits if necessary
-   Fill in PR description and reference an Issue for instance with `#6`
-   Review the "Files changed" section of your PR
-   "Think of the reviewer: your code needs to be reviewable and that should be a prime concern when writing your code, commits and PRs." (@camh-anz)
-   Only once you have ensured all previous points add reviewers to your PR
