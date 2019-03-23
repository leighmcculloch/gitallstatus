# gitallstatus

Check the state of all your git worktrees in subdirectories.

## Install

### Binary (Linux; macOS; Windows)

Download the binary from the [releases][] page.

[releases]: https://github.com/leighmcculloch/gitallstatus/releases

### From Source

```
go get 4d63.com/gitallstatus
```

## Usage

Print a list of repositories in the current directory that have branches not
pushed upstream, or dirty working directories:

```
gitallstatus [-e] [-a]
```

Add `-e` to exit with an error code if there are changes not pushed.

Add `-a` to print all branches.

Example:

```
$ gitallstatus
fork-stretchr-testify/
  master               ↑  origin/master
  base                    <none>
gs/
  master               ↑↓ origin/master
helloworld/
  push-with-request       <none>
  add-vcr-2           M   origin/add-vcr-2
  add-vcr              ↑↓ origin/add-vcr
```
