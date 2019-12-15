# til

## bash / zsh

### loop

    > for i in $(find . -type f); do grep <searchterm> $i -H; done;

or a little more whitespace robust

    > find . -type f| while read f; do echo $f; done
    
i.e. do a git pull in the subdiretories of the current folder
    
    > find . -type d -depth 1 | while read d; do git -C $d pull; done
    
### recursive grep

    > grep -r "commons-lang" .
    
### line endings

    > dos2unix.exe -i /foo/bar/some.properties
    dos2unix: /foo/bar/some.properties MODE 0100644  (regular file)
       0     193       0  no_bom    text    /foo/bar/some.properties
       

This option prints number of line breaks (DOS Unix Mac), the byte order mark, and if the file is text or binary.

### brace expansion

    > echo a{p,c,d,b}e
    
is expanded to:
    
    ape ace ade abe
    
In itself kinda useless, but think about:

    > echo foo/bar/more/less/{first.foo,second.foo}
    foo/bar/more/less/first.foo foo/bar/more/less/second.foo
    
Exchange the `echo` with a `mv` and it executes a `move` of a file in a `distant` directory without explicitly writing out the full path.

    > mv foo/bar/more/less/{first.foo,second.foo}

## piping

### into vim

    >  ls -la | vim -
    
## git

### squashing commits
Squash the last two commits:

    > git rebase -i HEAD~2

## vi / vim

### execute shell commands
show diff to last save

    > :w !diff % -
    
    
## curl
Stuff to be found without a full featured browser

    > curl ipinfo.io/8.8.8.8 
