# BMR Bunker C Refuellers

Bunker C refuelling facilities for Railroader, with loaders at six base-game engine-service locations, plus optional additions at Kirkland Services for Kirkland Coal Mine and at Sylva Interchange Fuel Service for Kater's turntable mod.

**Version 0.1.3** · [Nexus Mods](https://www.nexusmods.com/railroader/mods/1756) · [GitHub releases](https://github.com/BMR-Modding/BMR-Bunker-C-Refuellers/releases) · [Report a problem](https://github.com/BMR-Modding/BMR-Bunker-C-Refuellers/issues)

## Requirements

Install and enable these separately before installing this mod:

- **FUSE**.
- **Toolshed**.
- **[Crusher's Trucks And Assets](https://www.nexusmods.com/railroader/mods/1766)** (`CLW_Assets`), providing the SP Rose oil column.
- **C_L_B's ASSETS01** (`C_L_B.ASSETS01`), providing the baseplates.

You also need a locomotive or tender that uses Bunker C.

**Foxy's Alarka Yard Expanded**, **Stryker's Bryson**, **Kirkland Coal Mine** and **Kater's Sylva Interchange Turntable** are optional. Their compatibility adjustments activate automatically when the corresponding mod is enabled.

Install the legacy **C_L_B's ASSETS01** dependency manually: place its inner mod folder directly inside `Railroader/Mods`. Avoid an extra `Mods/Mods` folder level.

This mod contains configuration and documentation. Required dependency mods and their assets are installed separately, including Crusher's oil column.

## Installation with Unity Mod Manager (UMM)

**UMM is the primary installation method.**

1. Install the required mods above and close Railroader.
2. Download **BMR-Bunker-C-Refuellers-v0.1.3.zip** from the release's **Assets** section.
3. Open **Unity Mod Manager (UMM)** for Railroader and install the downloaded ZIP. Leave the ZIP intact for UMM to install.
4. Confirm the mod and its requirements are enabled, then start Railroader.

For an update, install the new release ZIP through UMM. Preserve any personal placement edits separately before updating, and keep only one installed copy of the mod.

### Manual installation (alternative)

With Railroader closed, extract the **BMR.Bunker.c.refillers** folder into `Railroader/Mods`. Check that the path is `Railroader/Mods/BMR.Bunker.c.refillers/Info.json`, with no extra folder level, then enable the mod and start the game.

Use the packaged release ZIP for UMM installation. GitHub's automatic **Source code** archives contain the repository and its development files.

## Locations and milestones

Each facility includes a Bunker C loader and a tank-car delivery span. The base placements include two baseplates; the Stryker's Bryson adaptation uses the yard's existing surface. The added loader and any baseplates follow the milestone listed below.

| Location | Availability |
| --- | --- |
| East Whittier | Available with the starting engine service. |
| Dillsboro | Dillsboro Engine Service. |
| Bryson | Ela Bridge to Bryson. |
| Alarka | Alarka Branch. |
| Nantahala | Fontana Bridge to Nantahala. |
| Andrews | Nantahala to Andrews / Build Red Marble Grade to Andrews. |
| Kirkland Services, with Kirkland Coal Mine | Available with the enabled route mod. |
| Sylva Interchange Fuel Service, with Kater's Sylva Interchange Turntable | Available with the enabled turntable mod. |

The facilities share Bunker C storage with their engine-service industry, accept Bunker C deliveries from TM tank cars, and have a configured storage capacity of **10,000 gallons each**. Toolshed connects the placed loader to compatible locomotive fuel load points.

Use the **Bunker-C Loader** entry under the engine service's **Tracks** list to locate the delivery span. Spot a TM tank car carrying Bunker C on that span to replenish the facility.

## Compatibility and known limitations

The six main placements target the base-game layout. Other mods can introduce scenery overlaps, move or replace track, or rename engine-service industries. These combinations may require a compatibility patch.

**BMR East Whittier Yard:** use an updated yard version with its old bundled Bunker C loader removed. An older version can create a duplicate loader. This mod applies at FUSE priority 110, after the current East Whittier Yard priority of 100.

**Appalachian Railway / Ela:** BMR no longer adds an Ela loader, baseplates, delivery span, industry component or milestone links. Ela is left to Appalachian Railway's own standpipe integration to avoid duplicate facilities.

**Foxy's Alarka Yard Expanded:** automatically adapts the Bunker C delivery span to the expanded yard and adds Bunker C to Alarka Engine Fuel Service. The placement uses Crusher's SP Rose oil column and keeps the existing Alarka industry and delivery-span binding.

**Stryker's Bryson:** automatically places the Bunker C loader at Bryson Roundhouse and uses the same delivery span as coal and diesel. It connects to the roundhouse's shared Bunker C storage and removes the two BMR baseplates at this location. The original Bryson setup is used when Stryker's Bryson is absent or disabled.

**Coal-tower visibility in Stryker's Bryson:** invisible coal towers have been reported in the FUSE setup used during compatibility work. The report remains open as [FUSE issue #288](https://github.com/F-U-S-E-E/FuseDevelopmentGroup/issues/288). This release does not include a FUSE fix.

**Compatibility with every map mod has not been tested.**

## Reporting problems

Please [open an issue](https://github.com/BMR-Modding/BMR-Bunker-C-Refuellers/issues) with:

- The affected location and a screenshot of the placement or error.
- Your Railroader version, this mod's version, and relevant mod names and versions.
- Whether the area or engine-service milestone is unlocked.
- `FUSE.log` and `Player.log` for loading, industry or refuelling problems.

The game logs are normally in `%USERPROFILE%/AppData/LocalLow/Giraffe Lab LLC/Railroader`.

## SP Rose oil-column asset

Install **[Crusher's Trucks And Assets](https://www.nexusmods.com/railroader/mods/1766)** separately and enable `CLW_Assets`. The installed layout should be `Railroader/Mods/CLW_Assets/info.json`, with its oil-column pack in `CLW_Assets/SCAssetPacks/SpRoseOilColumn`. FUSE discovers the pack from that folder.

- Tile Editor name: **Oil Column**.
- Scenery identifier: `scenery://SPRoseOilColumn`.
- Asset/model identifier: `SPRoseOilColumn` (unchanged).

BMR uses Crusher's external column for all loader placements, including the Foxy's Alarka and Stryker's Bryson adaptations and the optional Kirkland and Sylva additions. Existing placement, industry and service IDs are retained. ALW Scenery Assets is no longer required by BMR Bunker C Refuellers; other installed mods may still require it.

The external pack supplies the column's arm animation, fuel outlet and visible oil stream. Click the spout end to raise or lower the arm, and position a compatible locomotive or tender's fuel opening beneath it to refuel.

## Kirkland Coal Mine addition

When **Kirkland Coal Mine** is enabled, a Bunker C oil column and two baseplates are added at **Kirkland Services**. Deliver Bunker C to the same track used for coal; the Bunker C delivery span has its own Locations UI entry. The existing repair and coal services are preserved. The adjusted delivery-track endpoint is included.

## Kater's Sylva Interchange Turntable addition

When **Kater's Sylva Interchange Turntable** is enabled, two oil columns serve **Sylva Interchange Fuel Service**. Both draw from the same 10,000-gallon Bunker C storage. Use the **diesel delivery track** to replenish that storage; Bunker C has its own delivery-span entry. The existing coal and diesel services are preserved.

The final Sylva placements and operation were tested in-game by the mod author on 24 September 2026.

## Source files and editing

No compilation is required. The mod uses eight configuration files:

- `Info.json`: dependencies, apply priority and the six FUSE data files.
- `map.fuse.json`: the shared scenery and milestone links, plus the five non-Bryson base facilities.
- `bryson-vanilla.fuse.json`: the original Bryson span and industry addition, active when Stryker's Bryson is absent.
- `foxy-alarka.fuse.json`: optional Alarka adjustments for Foxy's Alarka Yard Expanded.
- `stryker-bryson.fuse.json`: optional Bryson Roundhouse placement, delivery span and industry addition for Stryker's Bryson.
- `kirkland-coal-mine.fuse.json`: optional Kirkland Services industry and column, with a separately named Bunker C span covering the coal delivery track.
- `katers-sylva-turntable.fuse.json`: optional Sylva fuel-service addition and dedicated Bunker C span over Kater's diesel delivery track.
- `ToolshedServiceFacilities.json`: the nine service bindings, including both Bryson industry IDs, the exact Kirkland target and both Sylva stands.


The repository's `source-manifest.json` records the runtime files' SHA-256 hashes. Releases include a ZIP checksum for checking the download. See `CHANGELOG.md` for version history.

## Credits

Mod author: BMR | Bjørn.
- SP Rose oil-column asset by Crusher / Mecrusher, supplied separately in [Crusher's Trucks And Assets](https://www.nexusmods.com/railroader/mods/1766).
- Earlier versions used the ALW Scenery Assets tank-loader model.
- baseplate assets by C_L_B's ASSETS01.
- Runtime support is supplied by FUSE and Toolshed
