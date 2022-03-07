# Plutarch-starter

## How do I get this project sturucture.
1. Creating nix scripts / cabal project using [init-haskell](https://github.com/masaeedu/init-haskell).
2. Install niv, and add git dependencies using niv:
```sh
niv add <org_name>/<repo_name>
```
If you want certain version of the package, use `--rev`
```sh
niv add <org_name>/<repo_name> --rev xxxx
```
3. Add the revision number and the sha256 hash to the cabal.project
```
source-repository-package
  type: git
  location: https://github.com/plutonomicon/plutarch
  tag: f8b7eb06184112ae2bebdec5a8156010141a05d5
  --sha256: 1vkhcj7rhxdzzxl5mgc1nhj8knvdg33kygw1187m25ckqsb5mnfb
```
> The hash has to be commented, and the tag is actually the commit hash in git.

## Build and run
```
hpack && cabal run
```