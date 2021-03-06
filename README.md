# julia-nixos

**This derivation is deprecated now that Julia 1.6 is in Nixpkgs (https://github.com/NixOS/nixpkgs/pull/123188).**

NixOS derivation for Julia 1.6.

In practise, this derivation works well for me.
It's how I use Julia daily and do most of my development.
However, I found two issues with this derivation:

- REPL crashes in some cases when terminating a running process (https://github.com/timholy/Revise.jl/issues/602)
- Cairo.jl doesn't work (https://github.com/JuliaGraphics/Cairo.jl/issues/336)

According to Pontus Stenetorp, this is due to the fact that the binary isn't patched.

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
you will have Julia 1.6 available globally.

## Extra

Let me know if you want to call R packages with this derivation, I have some code for that lying around.
