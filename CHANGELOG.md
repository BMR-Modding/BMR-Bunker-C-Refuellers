# Changelog

## 0.1.3 - Oil columns and additional compatibility

- Replaced the tank loaders with Crusher's animated SP Rose oil column, including the visible oil stream. **Crusher's Trucks And Assets (`CLW_Assets`) is now required.** The column is supplied by that external pack; no copy is bundled with BMR.
- Added optional **Kirkland Coal Mine** support at Kirkland Services, using the coal delivery track with a separate Bunker C track link. Includes the column, two baseplates and the adjusted delivery-track endpoint.
- Added optional **Kater's Sylva Interchange Turntable** support: two columns share Bunker C storage and use the diesel delivery track.
- Updated the base locations and Foxy's Alarka / Stryker's Bryson adaptations to the new column and latest authored placements. **ALW Scenery Assets is no longer required by BMR**; other mods may still require it.
- Removed BMR's **Appalachian Railway Ela** addition, including its scenery, delivery span, industry component, service binding and milestone targets. Ela is left to King's own standpipe integration to avoid duplicate facilities.
- Preserved the existing milestone links, shared industry storage and Dillsboro/Andrews loading-track extensions.

## 0.1.2 - Alarka and Bryson compatibility

- Added automatic compatibility for Foxy's Alarka Yard Expanded, adapting the Bunker C delivery span to the expanded yard and its engine fuel service.
- Added automatic compatibility for Stryker's Bryson, placing the Bunker C loader at Bryson Roundhouse and sharing the coal and diesel delivery span.
- Connected the Bryson loader to the appropriate industry storage for either layout and removed the BMR baseplates when Stryker's Bryson is active.
- Kept the original Bryson setup when Stryker's Bryson is absent or disabled. Both compatibility additions are optional; no new mandatory dependencies were added.

Known issue: invisible coal towers observed with Stryker's Bryson are being investigated in [FUSE issue #288](https://github.com/F-U-S-E-E/FuseDevelopmentGroup/issues/288). This update does not include a fix for that issue.

## 0.1.1 - Loading-track extensions

- Extended the engine-service loading tracks at Dillsboro and Andrews to provide more room for coal, Bunker C and diesel deliveries.

## 0.1.0 - Initial release

- Added Bunker C refuelling at East Whittier, Dillsboro, Bryson, Alarka, Nantahala and Andrews.
- Added a conditional Ela facility for Appalachian Railway, unlocked with Route to Cherokee.
- Added two baseplates per loader, delivery spans and industry components with shared Bunker C storage.
- Connected all seven facilities through Toolshed, with TM tank-car deliveries and 10,000-gallon configured storage per location.
- Linked the added loaders and baseplates to the relevant milestones; East Whittier is available with the starting engine service.
- Moved the East Whittier Bunker C setup into this standalone mod. Older East Whittier Yard versions that still contain that loader need updating to avoid duplicates.

The base facilities' startup visibility and milestone unlocks have been tested in-game.
