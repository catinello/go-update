go-update
===

Bash script to install or update Go using the latest offical golang.org packages for your unprivileged user, without the need for a package manager.

## Installation:

    $ curl -O https://raw.githubusercontent.com/catinello/go-update/master/go-update
    $ chmod +x go-update
    $ ./go-update

## Requirements:

Have to be available in $PATH:

    bash, awk, tar, tr, uname, grep, curl, sha256sum, rm, basename

## Usage:

    Usage: go-update [OPTIONS]
    
    OPTIONS:
      -h Show this help.
      -s Suppress all output.

## Examples:

First run to install Go to your users home:

    $ go-update
    → You are using a linux-amd64 system.
    → Fetching information from golang.org.
    → Installing go1.10.1.
    → Download of https://dl.google.com/go/go1.10.1.linux-amd64.tar.gz was successful
    → Verfication of archive succeeded.
    → Go paths: GOROOT: /home/catinello/.go | GOPATH: /home/catinello/go
    → Extraction completed.
    → Please make sure to source /home/catinello/.bashrc

To update just retrigger, like in this example from 1.10 to 1.10.1:

    $ go-update
    → You are using a linux-amd64 system.
    → Fetching information from golang.org.
    → Upgrading from go1.10 to go1.10.1.
    → Download of https://dl.google.com/go/go1.10.1.linux-amd64.tar.gz was successful
    → Verfication of archive succeeded.
    → Go paths: GOROOT: /home/catinello/.go | GOPATH: /home/catinello/go
    → Extraction completed.
    → Please make sure to source /home/catinello/.bashrc

In case you're running already the latest version:

    $ go-update
    → You are using a linux-amd64 system.
    → Fetching information from golang.org.
    → Latest go1.10.1 version is already installed.

You may want to add that to your crontab or some other automated call and may consider the output suppress option and watch the return code for errors.

## Notes:

It probably works with FreeBSD or MacOS too. I use it only on linux and amd64/arm architectures though. Testers and contributions are welcome.

Be careful to not mix it up with a golang linux distribution package. You really can't mess it up, since it's all related to your GOROOT/GOPATH environment variables and different file locations.

## License:

[&copy; Antonino Catinello][HOME] - [BSD-License][BSD]

[BSD]:https://github.com/catinello/go-update/blob/master/LICENSE
[HOME]:https://antonino.catinello.eu

