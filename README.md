# solutions-cramera-scenes

Scene bundles for the [cramera](https://github.com/AICOR-Solutions/cramera) viewer: digital
twins imported from Isaac Sim and CRAM robot runs recorded in them. Every directory is one
self-contained bundle (URDFs, meshes, trajectory); `index.json` lists them for the viewer's
scene picker.

## Scenes

| Bundle | Environment | Robot | Shows | Written by |
| --- | --- | --- | --- | --- |
| `aicor_lab` | AICOR Lab Automation Twin | - | Lab hall and Cell 01 | monorepo cramera USD import |
| `aicor_lab_r01` | AICOR Lab Automation Twin | FR3 | R01 demo cycle L09 - HN - H4 - L09 | monorepo cramera USD import |
| `warehouse` | Small Warehouse Twin | - | Warehouse hall | monorepo cramera USD import |
| `warehouse_tiago_two_totes` | Small Warehouse Twin | TIAGo++ | A08 + A09 to the packing station in-feed | monorepo cramera recording |
| `warehouse_tiago_stretch_totes` | Small Warehouse Twin | TIAGo++, Stretch | TIAGo: A08 + A09 to the in-feed; Stretch: R01 to A10 | monorepo cramera recording |
| `warehouse_tiago_plan_steps` | Small Warehouse Twin | TIAGo++ | Park, torso up, drive, torso down, drive back, park | cramera 1.0 recording |

## Opening them

```bash
cramera --scenes /path/to/solutions-cramera-scenes
```

or set `CRAMERA_SCENES` to this directory.

`warehouse`, `warehouse_tiago_two_totes` and `warehouse_tiago_stretch_totes` were written by
the cramera package of the CRAM monorepo, before version 1.0. The monorepo viewer opens them;
cramera 1.0 reads them only with its compatibility for those bundles (`cramera-check-bundle`
on cramera 1.0 `main` still reports their `scene.json` as unreadable).
