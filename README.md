# Packwiz Modpack with Github Actions
This repo is a template for creating a [packwiz](https://packwiz.infra.link/) modpack with an auto-updating [prism launcher](https://prismlauncher.org/) modpack using Github Actions to push updates to Github Pages and Releases.
It can also publish updates to Curseforge and/or Modrinth, provided a token and project ID.
## Usage
0. Clone/Fork/Download this template onto your pc
1. Enter the packwiz folder and edit the `pack.toml` or run `packwiz init -r`
2. Enter the `prism` folder and edit the `instance.cfg`, specifically the `name` and `PreLaunchCommand` variables
3. Create a new instance in Prism Launcher with your desired Minecraft and modloader versions, and copy the `mmc-pack.json` file from that instance into the `prism` folder
4. Replace or remove `modpack.png` and update or remove the `iconKey` in `instance.cfg` accordingly
5. Replace this `README.md` and the `LICENSE.md` files as appropriate for your modpack
6. Use `packwiz` to add mods to your pack in the `packwiz` folder
7. Test modrith export: `packwiz modrinth export`. If it fails with notification about manual downloads, you'll need to add those mods from Modrinth instead of Curseforge. If they are not availible on Modrith, do not add the jar files to the mods folder or add them via direct download url instead, as this would violate the licence terms of those mods.
8. Commit and push to GitHub.
9. (optional) In your repo settings on GitHub, under the Pages environment, add the `MODRINTH_TOKEN` and `MODRINTH_ID` and/or `CURSEFORGE_TOKEN` and `CURSEFORGE_ID` to enable automated releases on the respective site.

Releases and release notes are automatically generated from your `pack.toml` and commit messages. To create a new release, simply increment the `version` value in `pack.toml`, commit, and push.
Note that the prism pack requires a system installation of java version 21 or higher for the packwiz updater.
