# zen-browser-flake

Nix flake to build and install Zen Browser.

## Installation

Add to your `flake.nix` inputs:


inputs = {
zen-browser.url = "github:your-username/zen-browser-flake";
# optional: follow nixpkgs if needed
zen-browser.inputs.nixpkgs.follows = "nixpkgs";
};


Then add to your `environment.systemPackages` for NixOS:


environment.systemPackages = [
inputs.zen-browser.packages.${system}.default
];


Run:


sudo nixos-rebuild switch


Or for home-manager:


home.packages = [ inputs.zen-browser.packages.${system}.default ];
home-manager switch


## Usage

Run `zen` in your terminal or find Zen Browser in your app launcher.

## License

MIT License © Your Name

## Contributing

Feel free to open issues or pull requests!

---