#!/bin/bash

if [ -L "$0" ]; then
    root=$(cd "$(dirname "$(readlink "$0")")" && pwd)
else
    root=$(cd "$(dirname "$0")" && pwd)
fi

TAG="$1"
test -z "$1" && {
    echo "usage: $0 <FULL_TAG>"
    exit 1
}

set -x

# Does it have my executables handy in $PATH?
docker run --rm "$TAG" which \
	  octodns-compare \
	  octodns-dump \
	  octodns-report \
	  octodns-sync \
	  octodns-validate

# Execute one.
docker run --rm "$TAG" \
	  octodns-sync --help
