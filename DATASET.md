# Data format

The dataset contains 1,000 groups and 4,000 furnished layouts, covering five to eight rooms per building. Each source ID has Manhattan, curved, oblique and mixed variants. Room IDs, furniture IDs and furniture dimensions correspond within a group. Positions and yaw are adapted to each layout.

```text
dataset/
  manifest.json
  catalog.csv
  SHA256SUMS.txt
  assets/
    manifest.json
    <sha256>.obj
    <sha256>.png
  groups/
    <source_id>/
      source.json
      manhattan/
      curved/
      oblique/
      mixed/
        floorplan.json
        objects.json
        scene.xml
        floorplan.webp
```

`source.json` retains the canonical source annotation, metric calibration and source identity. Historical artifact locations use `provenance://` identifiers.

`floorplan.json` contains metric rooms, shared boundaries, doors, wall solids, envelope and physical parameters. Boundary points record the accepted simulation geometry and its approximation bounds.

`objects.json` records furniture and task-object identities, room IDs, categories, dimensions, footprints, positions, Z-axis yaw, asset identities and source hashes. OBJ meshes are already fitted to the recorded dimensions. Their placement uses the recorded position and yaw.

`scene.xml` is the native MuJoCo model. It references the shared meshes and textures with relative paths. Coordinates use an XY ground plane with Z up. Every XML is checked against its validated source hash.

`floorplan.webp` is a compact preview of the saved room and furniture geometry. Full geometry is stored in JSON.

`manifest.json` lists every group and variant, source-scene identifiers, XML hashes and recorded morphology metrics. `catalog.csv` provides the corresponding flat index. `SHA256SUMS.txt` covers the complete extracted dataset.

The source scenes passed MuJoCo loading, asset and furniture-pose checks, room-level RGB-D rendering and simulation stepping. Publication verifies every XML against that validated source, verifies all shared assets, and checks model loading on representative buildings.
