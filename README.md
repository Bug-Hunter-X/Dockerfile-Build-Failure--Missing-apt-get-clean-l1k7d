# Dockerfile Bug: Missing apt-get clean

This repository demonstrates a common error in Dockerfiles: forgetting to run `apt-get clean` after installing packages.

The original `Dockerfile` fails to build because of this omission. The solution shows how to fix it.

## Bug

The `Dockerfile` in this repository attempts to install Python and its dependencies. However, it omits the crucial `apt-get clean` command, resulting in a build failure due to space limitations.

## Solution

The `Dockerfile.fixed` file demonstrates the corrected version, which includes `apt-get clean` to remove unnecessary downloaded packages and caches, allowing for a successful build.