# julia-nixos

NixOS derivation for Julia 1.6.

## Usage

Place the file next to `/etc/nixos/configuration.nix` and import it with
```
imports = [
  ./julia.nix
]
```
after a 
```
nixos-rebuild switch
```
you will have Julia 1.6 available when running `j16`.

## Extra

Let me know if you want to call R packages with this derivation, I have some code for that lying around.
