# "Flake Package"

This is a installable "flake"
which rather than providing a usual `packages.<system>.<package>` output is in its entirety addable to `environment.systemPackages`

Installation is rather simple

Add this repo as a flake input
```nix
inputs.flake-package.url = "github:gerg-l/flake-package";

```
Pass your inputs to your [modules](https://blog.nobbz.dev/2022-12-12-getting-inputs-to-modules-in-a-flake/)

Then add `inputs.flake-package` to `environment.systemPackages` or `users.users.<name>.packages`

Rebuild, and you should be able to run `flake-package` from your shell

# how

the flexible type check of `lib.types.package` [here](https://github.com/NixOS/nixpkgs/blob/54cfbd1a979cfe3cf7cf5ab6fbacaf4e4b2a3275/lib/types.nix#L497)

# why

because it's funny

### TODO

use a multiarch statically compiled binary instead of a bash script
