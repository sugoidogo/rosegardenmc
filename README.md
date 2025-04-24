# Packwiz Modpack with Github Actions
This repo is a template for creating a [packwiz](https://packwiz.infra.link/) modpack with an auto-updating [prism launcher](https://prismlauncher.org/) modpack using Github Actions to push updates to Github Pages and Releases.
It can also publish updates to Curseforge and/or Modrinth, provided a token and project ID.
## Usage
0. Clone/Fork/Download this template onto your pc
1. Enter the packwiz folder and edit the `pack.toml` or run `packwiz init -r`
2. Enter the prism folder and edit the `instance.cfg`, specifically the `name` and `PreLaunchCommand` variables
3. Replace or remove `modpack.png` and update or remove the `iconKey` in `instance.cfg` accordingly
4. Replace this `README.md` and the `LICENSE.md` files as appropriate for your modpack
5. Use `packwiz` to add mods to your pack in the `packwiz` folder
6. Commit and push to GitHub.
7. (optional) In your repo settings on GitHub, under the Pages environment, add the `MODRINTH_TOKEN` and `MODRINTH_ID` and/or `CURSEFORGE_TOKEN` and `CURSEFORGE_ID` to enable automated releases on the respective site.

Releases and release notes are automatically generated from your `pack.toml` and commit messages. To create a new release, simply increment the `version` value in `pack.toml`, commit, and push.
