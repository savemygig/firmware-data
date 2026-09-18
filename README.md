# Save My Gig open data

Two datasets for DJs, venues, schools and tool builders, derived from the makers' own documentation. Published by [Save My Gig](https://www.savemygig.com), the DJ booth troubleshooting reference.

## Datasets

### 1. Firmware faults by version, AlphaTheta and Pioneer DJ
Every fault AlphaTheta document in a firmware change history, per model, with the version that fixed it and the version at or above which the model carries none of them. Faults only; feature additions are left out. 55 models.

- `data/firmware-issues.json`
- `data/firmware-issues.csv`
- Live page, with the same rows and a badge per unit: https://www.savemygig.com/knowledge/pioneer-dj/firmware

### 2. USB drive compatibility for standalone DJ players
Which file systems each standalone player reads (FAT32, exFAT, HFS+, NTFS), which rekordbox library format it expects (Device Library or OneLibrary) or whether it runs Engine DJ, and the maker document each row rests on. 29 models. A cell with no maker statement says "not stated" rather than guessing.

- `data/usb-compatibility.json`
- `data/usb-compatibility.csv`
- Live page: https://www.savemygig.com/knowledge/usb-compatibility

## How the data is made
No cell is written by hand. Both files are generated from the same source that renders the pages on savemygig.com, so the page and the file cannot disagree. Every row names the maker document it rests on. The `reviewed` field in each JSON is the date the sources were last re-read.

Field definitions are inside each JSON under `fields`.

## Updates
The files here mirror https://www.savemygig.com/data/ and are refreshed when the site's data changes, at least twice a month. If you need the newest copy without waiting, fetch the site URLs directly.

## Licence
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Reuse, quote and redistribute freely, with credit to Save My Gig and a link to the page the data comes from. Full text in `LICENSE`.

## Corrections
If a maker document contradicts a row, open an issue with the document URL. Rows are changed only against a maker source.
