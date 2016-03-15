# til

## bash

### loop

    > for i in $(find . -type f); do grep <searchterm> $i -H; done;

or a little more whitespace robust

    > find . -type f| while read f; do echo $f; done
    
### line endings

    > dos2unix.exe -i /foo/bar/some.properties
    dos2unix: /foo/bar/some.properties MODE 0100644  (regular file)
       0     193       0  no_bom    text    /foo/bar/some.properties
       

This option prints number of line breaks (DOS Unix Mac), the byte order mark, and if the file is text or binary.
    
## git

### squashing commits
Squash the last two commits:

    > git rebase -i HEAD~2
