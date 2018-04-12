go-update
===

Bash script to install or update Go using the offical golang.org packages for your unprivileged user.

## Installation:

    $ curl -O https://raw.github.com/catinello/go-update/master/go-update
    $ chmod +x go-update
    $ ./go-update

## Requirements:

    Have to be available in $PATH: bash, awk, tar, tr, uname, grep, curl, sha256sum, rm, basename

## Usage:

    Usage: go-update [OPTIONS]
    OPTIONS:
      -h Show this help.
      -s Suppress all output.

## Examples:

First run install go to your users home:

    $ go-update
    → You are using a linux-amd64 system.
    → Fetching information from golang.org.
    → Installing go1.10.1.
    → Download of https://dl.google.com/go/go1.10.1.linux-amd64.tar.gz was successful
    → Verfication of archive succeeded.
    → Go paths: GOROOT: /home/catinello/.go | GOPATH: /home/catinello/go
    → Extraction completed.
    → Please make sure to source /home/catinello/.bashrc

To update just retrigger:

    $ go-update
    → You are using a linux-amd64 system.
    → Fetching information from golang.org.
    → Latest go1.10.1 version is already installed.

You may want to add that to your cron or some other automated call and cosider the output suppress option.

## Notes:

It probably works with freebsd or macos too. I use it only on linux and amd64/arm architectures though.

## License:

[&copy; Antonino Catinello][HOME] - [BSD-License][BSD]

[BSD]:https://github.com/catinello/go-update/blob/master/LICENSE
[HOME]:https://antonino.catinello.eu

