+++
title = "Announcing mc-modpack-kit"
date = 2023-08-30

[taxonomies]
tags = ["modrinth", "modding", "minecraft", "ci"]
+++

Some time ago, I noticed that a lot of even bigger modpacks (mainly in the case for minecraft) management is quite messy, even some of my packs was pain the ass to maintain. So I started [mc-modpack-kit](https://github.com/jh-devv/mc-modpack-kit/). To make minecraft mod management a *breeze*!

By “*a breeze*”, I mean:

- Taking care about the releases and release notes.
- Making ready to use GitHub actions so you don't need to touch yaml.
- Allowing even novices to build their packs.
- Popularizing the monorepo structure in the modpack repos.

Along the way, I found out there were other ways to do the same, but manual!?!? I couldn't stand it.

`mc-modpack-kit` basically just makes mod managament more enjoyable.

## Quickstart

1. **Fork the [Repository](https://github.com/jh-devv/mc-modpack-kit/)**

   Start by forking this repository to your GitHub account.

2. **Set Up Secrets and Permissions**

   - Navigate to "Settings" -> "Secrets" and add the following secrets:
     - `MODRINTH_TOKEN`, `MODRINTH_ID` for Modrinth authentication.
     - `CURSEFORGE_TOKEN`, `CURSEFORGE_ID` for CurseForge authentication.
   - Enable "Allow GitHub Actions to create and approve pull requests" under "Settings" -> "Actions" -> "General" -> "Workflow permissions".

3. **Initialize Your Modpack**

   - Generate a `pack.toml` file using `packwiz` (installation instructions [here](https://packwiz.infra.link/installation/)) within a modpack folder.
   - Begin by running `packwiz init`, preferably within the `main` directory.
  
4. **Set a release channel**
   - By default this template uses the `beta (0.1.0)` channel, you can switch it to `release (1.0.0)` when you are ready!
   - This can be done via executing `.github/workflows/bump-version-release.yml`!

5. **You are good to go!**
   - You can now merge the release PR that release please has made, sit back and enjoy a cup of coffee! ☕ ^-^

## Next Steps
In the future, I plan to make mc-modpack-kit a family of sorts of modpack kits, or even a "framework" for them! This could be useful for as an example Terraria modpack

I hope you find this "project" of mine useful and basically thats that :3

> By the way, don't send me **any** of your political opinions. Keep them for yourself! I wan't to make the communnity friendly for e.g. LGBT.