# Third-party assets and attribution

## ResPlan

Source floor-plan annotations are derived from the ResPlan dataset by the ResPlan authors. The data is distributed under Creative Commons Attribution 4.0 International. Its original notice is retained in `licenses/ResPlan.txt`.

MorphVerse selects 1,000 source buildings, calibrates metric scale using the recorded listed area, constructs shared-wall geometry, and generates source-matched architectural variants. Source IDs, source release identity, annotation correspondences and scale evidence are retained per group. [Official repository](https://github.com/m-agour/ResPlan) · [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

## HSSD

Furniture meshes and base-color textures are derived from the Habitat Synthetic Scenes Dataset, maintained by the HSSD authors. The source repository is `hssd/hssd-hab`, pinned to revision `4369cb9876214c7fbebcf552eb532380e4d287e4`. HSSD uses Creative Commons Attribution-NonCommercial 4.0 International.

MorphVerse converts the selected meshes to OBJ, decodes base-color textures, fits dimensions to the shared furniture inventory, and applies verified front-direction corrections. Each object retains its HSSD asset ID and source SHA-256 identifier. [Dataset and license notice](https://huggingface.co/datasets/hssd/hssd-hab) · [HSSD project](https://3dlg-hcvc.github.io/hssd/) · [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

## ReplicaCAD

Task cups are derived from ReplicaCAD assets by Facebook, Inc. and its affiliates under CC BY-NC 4.0. The original notice is retained in `licenses/ReplicaCAD.txt`. The converted mesh retains its recorded source identity and dimensions. [Official dataset repository](https://github.com/facebookresearch/ReplicaCAD) · [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

## Presentation assets

Room finishes, skirting, lighting and cutaway geometry are generated from the saved MorphVerse building geometry. The featured renders reuse the material and presentation logic used for the MorphVerse paper figures. The animation shows source building 10412, whose source-scene identifiers are included in the dataset manifest.
