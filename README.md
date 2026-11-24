# Geologic Maps

Styled, Instagram-ready (4:5) geologic and seismic maps for Ingalls
Weather. Each project lives in its own directory with its own README.

Migrated from `markingalls/ingalls-weather-scripts`, with the history of
these files preserved.

## Projects

- [`county-geology-map/`](county-geology-map/) — reusable geologic map for
  any Washington or Oregon county: rock units, faults, folds, highways,
  water, and cities, with local legend wording drawn from the source data.
  `run_all.py` renders the whole series (39 WA + 36 OR counties), and
  `--palette cvd` renders a colorblind-friendly variant.
- [`wallowa-geology-map/`](wallowa-geology-map/) — geologic map of Wallowa
  County, OR with mapped faults and the most recent M3+ earthquake.
- [`wallowa-earthquakes-map/`](wallowa-earthquakes-map/) — every M3.0+
  earthquake on record in and around Wallowa County, from USGS ComCat.
  `wallowa-geology-map/` reuses its earthquake fetcher and basemap extras.

## Shared resources

- [`maps/`](maps/) — the shared, state-agnostic geology color table
  (`geology_classes.json`), crosswalks from each source dataset to it
  (`geology_sgmc.py`, `geology_wadnr.py`, `geology_ogdc.py`), legend
  wording (`geology_labels.py`), and basemap data (land, state and county
  boundaries, roads, Wallowa-area layers).
- [`assets/`](assets/) — the Ingalls Weather logo.

Run each project's scripts from inside its directory; paths to `../maps/`
and `../assets/` are relative to it. `setup.sh` in each project installs
GDAL, the Python requirements, and the Poppins fonts.
