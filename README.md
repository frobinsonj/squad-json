[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

|Index|Type|
|-----------|--------|
|actions|`{ [action: string]: Action }`|
|deployables|`{ [deployable: string]: Deployable }`|
|characteristics|`{ [characteristic: string]: string }`|
|factions|`{ [faction: string]: Faction }`|
|items|`{ [item: string]: Item }`|
|layers|`{ [layer: string]: Layer }`|
|levels|`{ [level: string]: Level }`|
|metadata|`Metadata`|
|roles|`{ [role: string]: Role }`|
|units|`{ [unit: string]: Unit }`|
|vehicles|`{ [vehicle: string]: Vehicle }`|

|Versions|Type|
|-----------|--------|
|DESERT|`"/Game/Blueprints/*" \| undefined`|
|FOREST|`"/Game/Blueprints/*" \| undefined`|
|SNOW|`"/Game/Blueprints/*" \| undefined`|

|Metadata|Type|
|-----------|--------|
|squad_version|`string`|
|timestamp|`number`|

|Action|Type|
|-----------|--------|
|name|`string`|
|details|`string`|
|type|`"TACTICAL" \| "STRATEGIC"`|
|icon|`"icons/tactical/*.png" \| "icons/strategic/*.png"`|
|duration|`{ enroute: number, active: number }`|
|delay|`{ initial: number, respawn: number }`|

|Deployable|Type|
|-----------|--------|
|name|`string`|
|versions|`Versions`|
|class_names|`string[]`|
|type|`string`|
|icon|`"icons/radial/*.png"`|

|Faction|Type|
|-----------|--------|
|name|`string`|
|short_name|`string`|
|flag|`"icons/flags/*.png"`|
|badge|`"icons/badges/*.png"`|
|buddy_rally|`boolean`|
|alliance|`string`|
|theaters|`string[]`|
|units|`string[]`|
|roles|`{ [type: string]: { name: string, details: string, options: string[] } }`|

|Item|Type|
|-----------|--------|
|name|`string`|
|class_name|`string`|
|category|`string`|
|image|`"items/*.png"`|
|icon|`"icons/item/*.png"`|
|info|`{ [field: string]: string }`|


|LayerUnits|Type|
|-----------|--------|
|`[faction: string]`|`string[]`|

|LayerTeam|Type|
|-----------|--------|
|tickets|`number`|
|defaultUnit|`string`|
|units|`LayerUnits \| null`|

|LayerObjectiveLocation|Type|
|-----------|--------|
|name|`string`|
|order|`number`|
|location|`{ x: number, y: number, z: number }`|
|minimap|`{ x: number, y: number }`|

|Layer|Type|
|-----------|--------|
|name|`string`|
|gamemode|`string`|
|level|`string`|
|size|`string`|
|minimap|`"minimaps/*.png"`|
|minimap_corners|`{ min: { x: number, y: number }, max: { x: number, y: number } }`|
|commander|`boolean`|
|fob_radius|`{ name: string, exclusion: number, construction: number }`|
|lighting|`string`|
|units|`LayerUnits \| null`|
|teams|`[LayerTeam, LayerTeam]`|
|objective|`{ count: number, locations: LayerObjectiveLocation[] }`|

|Level|Type|
|-----------|--------|
|name|`string`|
|country|`string`|
|minimap|`"minimaps/*.png"`|
|image|`"levels/*.png"`|
|thumbnail|`"levels/thumbnails/*.png"`|

|Role|Type|
|-----------|--------|
|versions|`Versions`|
|class_names|`string[]`|
|type|`string`|
|icon|`"icons/role/*.png"`|
|tags|`string[]`|
|items|`string[]`|

|Unit|Type|
|-----------|--------|
|name|`string`|
|faction|`string`|
|details|`string`|
|badge|`"badges/*.png"`|
|type|`string`|
|buddy_rally|`boolean`|
|vehicle_commander_action|`boolean`|
|characteristics|`string[]`|
|actions|`string[]`|
|vehicles|`{ [vehicle: string]: { count: number, delay: { initial: number, respawn: number } } }`|
|deployables|`{ [deployable: string]: { limit: number \| null, cost: number } }`|

|Vehicle|Type|
|-----------|--------|
|name|`string`|
|versions|`Versions`|
|class_names|`string[]`|
|type|`string`|
|tags|`string[]`|
|tickets|`number`|
|icon|`"icons/map/*.png"`|
