# BMR Bunker C Refuellers

Bunker C refuelling facilities for Railroader, built around the base-game engine-service locations. An optional conditional addition supplies Ela Engine Service when Appalachian Railway is enabled.

Version: **0.1.0**. This repository contains the authored FUSE and Toolshed configuration; no build step is required.

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

The facilities share Bunker C storage with their engine-service industry, accept Bunker C deliveries from TM tank cars, and have a configured storage capacity of 10,000 gallons each. Toolshed connects the placed loader to compatible locomotive fuel load points.

## Requirements

Install and enable these separately:

- FUSE.
- Toolshed.
- ALW Scenery Assets for FUSE (`ALW.SceneryAssets.FUSE`), providing the tank-loader model.
- C_L_B's ASSETS01 (`C_L_B.ASSETS01`), providing the baseplates.

Appalachian Railway (`Appalachian-Railway.KingG`) is optional. FUSE skips the Ela fragment when it is absent or disabled; the six base-map facilities remain available according to their milestones. Refuelling requires suitable Bunker C equipment.

## Installation

1. Install the required mods.
2. Copy the **BMR.Bunker.c.refillers** folder from this repository into `Railroader/Mods`.
3. Confirm `Info.json` is directly inside `Railroader/Mods/BMR.Bunker.c.refillers`.
4. Enable the mod in the mod manager and restart Railroader.

When downloading GitHub's source ZIP, copy the inner mod folder rather than the outer repository folder. The top-level README and source manifest are repository documentation.

## Compatibility

The six main placements target the base-game layout. Other mods can introduce scenery overlaps, move or replace track, or rename engine-service industries. These combinations may require a compatibility patch.

For East Whittier Yard, use the updated yard configuration with its old bundled Bunker C loader removed. An older copy can produce a duplicate loader. This mod applies at FUSE priority 110, after the current East Whittier Yard priority of 100.

The Ela service uses an exact scenery-object target so its optional binding cannot fall back to another tank-loader model when Appalachian Railway is absent.

For a conflict report, include the location, affected mod names and versions, and a screenshot. Include `FUSE.log` and `Player.log` if a package, industry or loader fails to function.

## Files

- `Info.json`: dependencies, apply priority and the two FUSE data files.
- `map.fuse.json`: the six main facilities, delivery spans, industry additions and milestone links.
- `appalachian-ela.fuse.json`: optional Ela placement and operations, conditional on Appalachian Railway.
- `ToolshedServiceFacilities.json`: the seven service bindings.

The placed object IDs, service IDs, industry IDs and span IDs are referenced across these files. Keep their links consistent when editing. Changes made to the installed mod are not automatically synchronized with this repository.

FUSE's installed runtime accepts the additive object form used for milestone targets. Some editor schema versions only describe arrays and underline these entries; changing them to arrays would replace the milestone's existing target list.

## Validation at initial upload

- The author confirmed the base facilities' new-company visibility and milestone unlocking in-game.
- The available runtime log shows the conditional Ela fragment applied and Toolshed connected its receiving unloader.
- The latest Ela baseplate milestone additions and source-file metadata were checked in configuration; an in-game retest of those final changes is still pending.
- JSON structure, facility links, scenery targets and additive milestone parsing were checked before upload.
- Imported runtime files are recorded with SHA-256 hashes in `source-manifest.json`.

Tile Editor backups, saves, logs, game assemblies and third-party assets are excluded. The runtime version remains 0.1.0; this upload does not create a tagged release.

## Credits

Mod author: BMR | Bjørn. 
Tank-loader assets are supplied by ALW Scenery Assets; 
baseplate assets by C_L_B's ASSETS01. 
Runtime support is supplied by FUSE and Toolshed, with the optional Ela location using Appalachian Railway's engine service.
