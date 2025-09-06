# zen-browser-flake

Nix flake to build and install Zen Browser.

## Installation

Add to your `flake.nix` inputs:

```nix
zen-browser = {
    url = "github:14Artemiy88/zen-browser-flake";
    inputs.nixpkgs.follows = "nixpkgs";
};
```

Then add to your `environment.systemPackages` for NixOS:

```nix
environment.systemPackages = [
    inputs.zen-browser.packages.${system}.default
];
```


Run:

```bash
sudo nixos-rebuild switch
```

Or for home-manager:

```nix
home.packages = [ 
    inputs.zen-browser.packages.${system}.default
];
```

```bash
home-manager switch
```



## Usage

Run `zen` in your terminal or find Zen Browser in your app launcher.

## License

MIT License

## Contributing

Feel free to open issues or pull requests!

---