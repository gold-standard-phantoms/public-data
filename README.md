# Public Data Repository

This repository stores **publicly releasable** product data for Gold Standard Phantoms.

## Scope and release rules

Only files that are explicitly cleared for public release should be added here.

- No clinical images should be included.
- Customer scanned atlas images must have a corresponding **site release agreement** before inclusion.

## Folder design

Top-level folder for datasets is `phantoms/`.
Inside `phantoms/`, each product has its own folder with an `atlas` folder.
Each `atlas` folder contains pairs of files:

- `*.nii.gz` (image volume)
- `*.json` (metadata for the matching image)

### Planned structure

```text
public-data/
  phantoms/
    MS120D/
      atlas/
        ...
    MS120E/
      atlas/
        ...
    MS190F/
      atlas/
        ...
    SPIRIT/
      atlas/
        spirit_issue1.0_vx1_sub1.nii.gz
        spirit_issue1.0_vx1_sub1.json
        spirit_issue1.0_vx0.5_sub1.nii.gz
        spirit_issue1.0_vx0.5_sub1.json
        spirit_issue1.0_vx0.25_sub1.nii.gz
        spirit_issue1.0_vx0.25_sub1.json
        ...
```

## Product folders

Under `phantoms/`:

- `MS120D`
- `MS120E`
- `MS190F`
- `SPIRIT`

## Notes

### ATLAS directory

- Folder names above are standardised for repository consistency.
- SPIRIT atlas naming format: `spirit_issue1.0_vx<VX>_sub<SUB>`.
- `VX` is the size of each voxel in the atlas and is currently one of `1`, `0.5`, or `0.25`.
- `SUB` is the subvoxel calculation value and is can take on values `1` or `2` for this initial set.
- The current structure is for `atlas` data only.
- Additional directories (for example, reference segmentations and scanner data) are expected to be added later.
