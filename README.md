# Isometric Renders — Minecraft 26.3 port

> **Unofficial port** of [gliscowo/isometric-renders](https://github.com/gliscowo/isometric-renders) (1.21.4, MIT) to Minecraft **26.3** (Fabric).
> Not affiliated with the original author; report port bugs [here](../../issues), not upstream. See [DEVELOPMENT.md](DEVELOPMENT.md) for the port's state and dev workflow.
>
> **Download:** grab `IsometricRenders-<version>.jar` from [Releases](../../releases) and drop it in your `mods` folder.
> Needs Minecraft 26.3, Java 25 and Fabric API — owo-lib is bundled inside the jar, so don't install it separately.
> To update, replace the old jar with the new one. Older versions stay available on the Releases page.
>
> Port-only additions: export anti-aliasing (supersampling Off/2x/4x), correct colors for translucent blocks in exports,
> view-based translucent sorting in area renders, debug overlays in area renders (F3 hitboxes, chunk borders and other
> debug renderers, plus Scarpet `draw_shape` shapes when Carpet is installed), and a client gametest (`./gradlew runClientGameTest`).


[![release](https://img.shields.io/github/v/release/YatagarasuMC/isometric-renders-for-fabric26.3?logo=github&style=for-the-badge)](../../releases)
[![docs](https://img.shields.io/badge/-documentation-gray?style=for-the-badge&logo=gitbook&labelColor=blue)](https://docs.wispforest.io/isometric-renders/home)
[![upstream](https://img.shields.io/badge/-upstream-gray?style=for-the-badge&logo=github&labelColor=black)](https://github.com/gliscowo/isometric-renders)

## Overview

Isometric Renders allows you to take isometric screenshots, or rather, create renders of game objects like parts of world, blocks, items and entities.
These are automatically keyed to have a transparent background and you can adjust scale, positioning and many more options right in-game in a fancy gui.
This was designed with modded wikis or similar documentation in mind, should be easy to use and mostly pretty performant.

**In-Depth documentation is available on the [wiki](https://docs.wispforest.io/isometric-renders/home)** (written for
upstream; the in-game UI is the same)

#


### Currently Supported Rendering Targets

- Items
- Blocks
- Entities
- Areas of the world
- Batch export of multiple blocks or items
- Item Atlases (Overviews)
