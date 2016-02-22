# til

## bash

### loop
    > for i in $(find . -type f); do grep <searchterm> $i -H; done;

## git

### squashing commits
Squash the last two commits:
    > git rebase -i HEAD~2
