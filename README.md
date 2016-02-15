# til

## bash

### loop
    > for i in $(find . -type f); do grep <searchterm> $i -H; done;
