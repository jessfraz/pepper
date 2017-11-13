# pepper

[![Travis CI](https://travis-ci.org/jessfraz/pepper.svg?branch=master)](https://travis-ci.org/jessfraz/pepper)

Named after Pepper Potts. Set all your GitHub repos master branches to be
protected.

You can set which orgs to include and use `--dry-run` to see the
changes before they are actually made. Your user is automatically added to the
repositories it will consider.

Also see [jessfraz/audit](https://github.com/jessfraz/audit) for checking what
collaborators, hooks, deploy keys, and protected branched you have added on
all your GitHub repositories.

## Installation

#### Binaries

- **darwin** [386](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-darwin-386) / [amd64](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-darwin-amd64)
- **freebsd** [386](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-freebsd-386) / [amd64](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-freebsd-amd64)
- **linux** [386](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-linux-386) / [amd64](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-linux-amd64) / [arm](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-linux-arm) / [arm64](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-linux-arm64)
- **solaris** [amd64](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-solaris-amd64)
- **windows** [386](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-windows-386) / [amd64](https://github.com/jessfraz/pepper/releases/download/v0.1.1/pepper-windows-amd64)

#### Via Go

```bash
$ go get github.com/jessfraz/pepper
```

## Usage

```console
$ pepper -h
pepper - v0.1.1
  -d    run in debug mode
  -dry-run
        do not change branch settings just print the changes that would occur
  -nouser
        do not include your user
  -orgs value
        organizations to include
  -token string
        GitHub API token
  -url string
        GitHub Enterprise URL
  -v    print version and exit (shorthand)
  -version
        print version and exit
```

```console
$ pepper --dry-run --token 12345 --orgs jessconf --orgs maintainerati
[OK] jessconf/jessconf:master is already protected
[OK] jessfraz/.vim:master is already protected
[OK] jessfraz/anonymail:master is already protected
[OK] jessfraz/apk-file:master is already protected
[UPDATE] jessfraz/certok:master will be changed to protected
...
[OK] jessfraz/weather:master is already protected
[OK] jessfraz/ykpiv:master is already protected
[OK] maintainerati/wontfix-cabal-site:master is already protected
```
