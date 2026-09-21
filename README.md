# BMR Bunker C Refuellers

Bunker C refuelling facilities for Railroader, with loaders at six base-game engine-service locations and an optional seventh at Ela for Appalachian Railway.

**Version 0.1.1** · [Nexus Mods](https://www.nexusmods.com/railroader/mods/1756) · [GitHub releases](https://github.com/BMR-Modding/BMR-Bunker-C-Refuellers/releases) · [Report a problem](https://github.com/BMR-Modding/BMR-Bunker-C-Refuellers/issues)

## Requirements

Install and enable these separately before installing this mod:

- **FUSE**.
- **Toolshed**.
- **ALW Scenery Assets for FUSE** (`ALW.SceneryAssets.FUSE`), providing the tank-loader model.
- **C_L_B's ASSETS01** (`C_L_B.ASSETS01`), providing the baseplates.

**Appalachian Railway** (`Appalachian-Railway.KingG`) is optional. It enables the Ela addition; the six base-map locations work without it. You also need a locomotive or tender that uses Bunker C.

The download contains this mod's configuration and documentation. Required mods and their assets are not bundled.

## Installation with Unity Mod Manager (UMM)

**UMM is the primary installation method.**

1. Install the required mods above and close Railroader.
2. Download **BMR-Bunker-C-Refuellers-v0.1.1.zip** from the release's **Assets** section.
3. Open **Unity Mod Manager (UMM)** for Railroader and install the downloaded ZIP. Leave the ZIP intact for UMM to install.
4. Confirm the mod and its requirements are enabled, then start Railroader.

For an update, install the new release ZIP through UMM. Preserve any personal placement edits separately before updating, and keep only one installed copy of the mod.

### Manual installation (alternative)

With Railroader closed, extract the **BMR.Bunker.c.refillers** folder into `Railroader/Mods`. Check that the path is `Railroader/Mods/BMR.Bunker.c.refillers/Info.json`, with no extra folder level, then enable the mod and start the game.

Use the packaged release ZIP for UMM installation. GitHub's automatic **Source code** archives contain the repository and its development files.

## Locations and milestones

Each facility includes a tank loader, two baseplates and a tank-car delivery span. The added loader and baseplates follow the milestone listed below.

| Location | Availability |
| --- | --- |
| East Whittier | Available with the starting engine service. |
| Dillsboro | Dillsboro Engine Service. |
| Bryson | Ela Bridge to Bryson. |
| Alarka | Alarka Branch. |
| Nantahala | Fontana Bridge to Nantahala. |
| Andrews | Nantahala to Andrews / Build Red Marble Grade to Andrews. |
| Ela, with Appalachian Railway | Route to Cherokee. |

The facilities share Bunker C storage with their engine-service industry, accept Bunker C deliveries from TM tank cars, and have a configured storage capacity of **10,000 gallons each**. Toolshed connects the placed loader to compatible locomotive fuel load points.

Use the **Bunker-C Loader** entry under the engine service's **Tracks** list to locate the delivery span. Spot a TM tank car carrying Bunker C on that span to replenish the facility.

## Compatibility and known limitations

The six main placements target the base-game layout. Other mods can introduce scenery overlaps, move or replace track, or rename engine-service industries. These combinations may require a compatibility patch.

**BMR East Whittier Yard:** use an updated yard version with its old bundled Bunker C loader removed. An older version can create a duplicate loader. This mod applies at FUSE priority 110, after the current East Whittier Yard priority of 100.

**Appalachian Railway:** the Ela addition loads automatically when the mod is enabled and follows its Route to Cherokee milestone. FUSE skips this addition when Appalachian Railway is absent or disabled.

**Compatibility with every map mod has not been tested.**

## Reporting problems

Please [open an issue](https://github.com/BMR-Modding/BMR-Bunker-C-Refuellers/issues) with:

- The affected location and a screenshot of the placement or error.
- Your Railroader version, this mod's version, and relevant mod names and versions.
- Whether the area or engine-service milestone is unlocked.
- `FUSE.log` and `Player.log` for loading, industry or refuelling problems.

The game logs are normally in `%USERPROFILE%/AppData/LocalLow/Giraffe Lab LLC/Railroader`.

## Source files and editing

No compilation is required. The mod uses four configuration files:

- `Info.json`: dependencies, apply priority and the two FUSE data files.
- `map.fuse.json`: the six main facilities, delivery spans, industry additions and milestone links.
- `appalachian-ela.fuse.json`: optional Ela placement and operations, conditional on Appalachian Railway.
- `ToolshedServiceFacilities.json`: the seven service bindings.

Object, service, industry and span IDs link these files together. Keep those references consistent when editing. Changes made to an installed copy do not automatically update this repository.

Milestone targets use FUSE's additive object form to preserve existing targets. Some editor schema versions only describe arrays and underline these entries; changing them to arrays would replace the milestone's existing target list. The optional Ela service uses an exact scenery-object target so it cannot fall back to another loader when Appalachian Railway is absent.

The repository's `source-manifest.json` records the runtime files' SHA-256 hashes. Releases include a ZIP checksum for checking the download. See `CHANGELOG.md` for version history.

## Credits

Mod author: BMR | Bjørn. 
- Tank-loader assets are supplied by ALW Scenery Assets; 
- baseplate assets by C_L_B's ASSETS01. 
- Runtime support is supplied by FUSE and Toolshed 
- The optional Ela location using Appalachian Railway's engine service.
