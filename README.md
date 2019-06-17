# Haystacl [![GoDoc](https://godoc.org/github.com/carlmjohnson/haystack?status.svg)](https://godoc.org/github.com/carlmjohnson/haystack) [![Go Report Card](https://goreportcard.com/badge/github.com/carlmjohnson/haystack)](https://goreportcard.com/report/github.com/carlmjohnson/haystack)

Pinboard search CLI

## Installation

First install [Go](http://golang.org).

If you just want to install the binary to your current directory and don't care about the source code, run

```bash
GOBIN="$(pwd)" GOPATH="$(mktemp -d)" go get github.com/carlmjohnson/haystack
```

## Screenshots
```
$ haystack -h
haystack - a Pinboard search client

usage:

        haystack [options] <tags>...

-auth-token taken from environmental variable $PINBOARD_TOKEN if set.

Options:

  -auth-token string
        auth token, see https://pinboard.in/settings/password (default "$PINBOARD_TOKEN")
  -password string
        password
  -t    shortcut for -tag-search
  -tag-search
        search for similar tags, rather than saved pages
  -timeout duration
        timeout for query (default 5s)
  -user string
        username

$ haystack -t sql
"SQL": 32
"SQLite": 7
"Yesql": 7
"MySQL": 2

$ haystack MySQL
Title: hyperpolyglot.org
Date: Mar. 7, 2017 8:22am
Tags: MySQL Postgres database SQLite SQL
URL: http://hyperpolyglot.org/db

Title: pgloader
Date: May. 2, 2016 4:04pm
Tags: database Postgres MySQL command_line_tools
URL: http://pgloader.io/
```
