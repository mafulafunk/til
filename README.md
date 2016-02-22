# til

## bash

### loop

    > for i in $(find . -type f); do grep <searchterm> $i -H; done;

or a little more whitespace robust

    > find . -type f| while read f; do echo $f; done
    
## git

### squashing commits
Squash the last two commits:

    > git rebase -i HEAD~2
