# Texas waste pit map

Interactive map of the 6,943 oil and gas waste pits registered with the Railroad Commission of Texas between July 1, 2025 and August 31, 2026, the first year of the agency's Chapter 4 pit registry.

**Live map:** https://saulbanov.github.io/waste-pit-map-site/

By Saul Elbein and Greg Randall, Future Heist.

## What the map shows

Every pit with usable coordinates (6,934 of 6,943), colored by pit type, with filters for schedule, status and a set of flags computed from the registry and public overlays: FEMA flood zones, Texas Water Development Board well records, and a county choropleth of population and agricultural value. Status, dimensions and groundwater depth are what the operator entered on Form EP-1. The Commission does not review those entries.

## Source

RRC open-records export dated 2026-09-01, released to Saul Elbein. File `20260901_ORR_AuthPitAB_20250701to20260831.xlsx`, sha256 `c05a347f9fdc429aae45212774ef8faa7c2094f51d874fd228d090b26a8c6806`. The footer of the map carries the same provenance string.

## Dataset and method

The full dataset, the scripts that built every layer, and method notes are in `saulbanov/waste-pit-dataset` (shared on request for fact-checking). This repository holds only the rendered map and the three files it reads:

```
index.html                 the map (Leaflet, loaded from cdnjs)
data/pits.geojson          one point per pit with all computed flags
data/tx_counties.geojson   Census county polygons, simplified
data/county.summary.csv    per-county counts and overlays
```

## Editing

This is a publishing copy. The source of record is the private repo `saulbanov/waste-pit-map` (`map/index.html` and `data/views/`). Edit there and re-copy; the only change in this copy is the data path (`data/` instead of `../data/views/`) and the credit line.
