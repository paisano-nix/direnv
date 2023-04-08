## Paisano Direnv Support

### Usage

```console
direnv fetchurl https://raw.githubusercontent.com/paisano-nix/direnv/main/lib
```

##### `.envrc` without watcher

```bash
#! /bin/sh

source $(fetchurl https://raw.githubusercontent.com/paisano-nix/direnv/main/lib <hash>)

use env //repo/shells/default
```

##### `.envrc` with simple watcher

```bash
#! /bin/sh

source $(fetchurl https://raw.githubusercontent.com/paisano-nix/direnv/main/lib <hash>)

use envreload //repo/shells/default
```

##### `.envrc` with multiple watcher

```bash
#! /bin/sh

source $(fetchurl https://raw.githubusercontent.com/paisano-nix/direnv/main/lib <hash>)

use envreload //repo/shells/default \
  //repo/config/default \
  //repo/packages
```
