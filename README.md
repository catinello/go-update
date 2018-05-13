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
    → Retrieve system information: linux-amd64 ✓
    → Fetching information from golang.org. ✓
    → Decide on procedure: Installing go1.10.1. ✓
    → Download of https://dl.google.com/go/go1.10.1.linux-amd64.tar.gz ✓
    → Verify given checksums. ✓
    → Set Go paths: GOROOT: /home/catinello/.go | GOPATH: /home/catinello/go ✓
    → Extracting the Go package. ✓
    → Adding environment variables to your bash resource configuration. ✓
    ! Please make sure to source /home/catinello/.bashrc

To update just retrigger, like in this example from 1.10.1 to 1.10.2:

    $ go-update
    → Retrieve system information: linux-amd64 ✓
    → Fetching information from golang.org. ✓
    → Decide on procedure: Upgrading from go1.10.1 to go1.10.2. ✓
    → Download of https://dl.google.com/go/go1.10.2.linux-amd64.tar.gz ✓
    → Verify given checksums. ✓
    → Set Go paths: GOROOT: /home/catinello/.go | GOPATH: /home/catinello/go ✓
    → Extracting the Go package. ✓
    → Adding environment variables to your bash resource configuration. ✓
    ! Please make sure to source /home/catinello/.bashrc
    
In case you're running already the latest version:

    $ go-update
    → Retrieve system information: linux-amd64 ✓
    → Fetching information from golang.org. ✓
    → Decide on procedure: Latest go1.10.2 version is already installed. ✓

You may want to add that command to your crontab or some other automated call. Consider the output suppress option (-s) and watch the return code for errors (!0).

## Notes:

It probably works with BSD's and MacOS too. I use it only with linux and on amd64/aarch64 plattforms though. 

## License:

[&copy; Antonino Catinello][HOME] - [BSD-License][BSD]

[BSD]:https://github.com/catinello/go-update/blob/master/LICENSE
[HOME]:https://antonino.catinello.eu
