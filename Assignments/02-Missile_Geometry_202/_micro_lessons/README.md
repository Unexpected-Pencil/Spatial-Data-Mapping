| #   | File                                         | Description |
| --- | -------------------------------------------- | ----------- |
| 1   | [00_Paths](00_Paths)                         | -           |
| 2   | [01_JSON_GeoJSON](01_JSON_GeoJSON)           | -           |
| 3   | [02_Viewing_GeoJSON](02_Viewing_GeoJSON)     | -           |
| 4   | [03_Styling_Filtering](03_Styling_Filtering) | -           |
| 5   | [04_Bounding_Box](04_Bounding_Box)           | -           |
| 6   | [05_Interactive_Maps](05_Interactive_Maps)   | -           |
| 7   | [06_Point_In_Polygon](06_Point_In_Polygon)   | -           |
| 8   | [07_Distance](07_Distance)                   | -           |
| 9   | [08_Bearing](08_Bearing)                     | -           |
| 10  | [09_Lines](09_Lines)                         | -           |
| 11  | [10_Intersections](10_Intersections)         | -           |
| 12  | [11_Buffers](11_Buffers)                     | -           |
| 13  | [12_WDO_Library](12_WDO_Library)             | -           |
| 14  | [13_Refactoring](13_Refactoring)             | -           |
| 15  | [README.md](README.md)                       | -           |

# Missile Geometry 101 — Micro Lesson Roadmap

These micro lessons are designed to build the skills needed for the **Missile Geometry 101/202** project one concept at a time. Each lesson introduces a small, focused idea. The final project is where those ideas are combined.

The general progression is:

```text
Paths → JSON/GeoJSON → Viewing Maps → Styling → Extent → Clicks
→ Point in Polygon → Distance → Bearing → Lines → Intersections
→ Buffers → Reusable Helpers / WDO
```

---

## 00 — Paths, Working Directories, and Data Files

### Goal

Learn how to locate files reliably before doing any spatial work.

### Students will practice

- checking the current working directory
- building paths with `pathlib`
- verifying whether files exist
- failing cleanly when files are missing

### Why this matters

Before students can load GeoJSON, JSON, or images, they need to understand where their code is running and where the data lives.

---

## 01 — JSON, GeoJSON, and Feature Collections

### Goal

Understand the structure of the data before trying to display it.

### Students will practice

- reading JSON files
- identifying `FeatureCollection`, `Feature`, `properties`, and `geometry`
- distinguishing regular JSON from GeoJSON
- understanding that GeoJSON coordinates are stored as `[lon, lat]`

### Why this matters

Students should know what they are holding in memory before trying to map or analyze it.

---

## 02 — Viewing GeoJSON with Folium

### Goal

Load GeoJSON and display it on an interactive map.

### Students will practice

- loading a GeoJSON file
- adding it as a map layer in Folium
- centering and zooming a map
- seeing polygon features rendered visually

### Why this matters

This is the first “reward” notebook: students see their data on a map.

---

## 03 — Properties, Styling, and Filtering

### Goal

Use feature data to control how things look and what gets displayed.

### Students will practice

- reading `feature["properties"]`
- styling features dynamically
- coloring based on attribute values
- filtering features before display

### Example tasks

- countries A–M one color, N–Z another
- show only countries above a population threshold
- show only countries in one hemisphere

### Why this matters

Students learn that **data drives map output**.

---

## 04 — Bounding Boxes and Spatial Extent

### Goal

Understand the geographic extent of a dataset.

### Students will practice

- computing min/max longitude and latitude
- interpreting dataset bounds
- drawing a rectangle for a bounding box
- reinforcing coordinate order

### Why this matters

This is the first step from “displaying shapes” to “reasoning about space.”

---

## 05 — Interactive Maps with ipyleaflet

### Goal

Capture user clicks and save point data from a map.

### Students will practice

- switching from Folium to ipyleaflet
- using map click callbacks
- dropping markers interactively
- saving clicked coordinates to a file
- clearing points with widgets

### Why this matters

Students move from viewing maps to **interacting** with maps.

---

## 06 — Point in Polygon and Clicked Region Detection

### Goal

Determine which polygon contains a clicked point.

### Students will practice

- converting click coordinates into geometry-friendly format
- looping through polygon features
- testing whether a point lies inside a region
- classifying a click by region name

### Example tasks

- determine which quadrant/region was clicked
- later extend to which US state was clicked

### Why this matters

This is the bridge between **click capture** and **spatial reasoning**.

---

## 07 — Haversine Distance

### Goal

Compute geographic distances between real locations.

### Students will practice

- using latitude/longitude in formulas
- computing distances between points
- sorting locations by distance
- displaying results on a map

### Why this matters

Distance is one of the core mathematical tools needed for the final project.

---

## 08 — Bearings and Destination Points

### Goal

Compute a destination point from a start point, bearing, and distance.

### Students will practice

- working with bearings
- converting between degrees and radians
- computing a destination coordinate
- plotting the result

### Why this matters

Students isolate the directional math before using it in more complex trajectory work.

---

## 09 — LineStrings and Trajectories

### Goal

Build line geometry explicitly from points.

### Students will practice

- creating `LineString` geometries
- drawing start-to-end paths
- visualizing simple trajectories

### Why this matters

Students turn point computations into visible geometry.

---

## 10 — Line and Polygon Intersections

### Goal

Determine whether paths intersect polygon regions.

### Students will practice

- testing line vs polygon relationships
- identifying intersected countries or regions
- highlighting intersected features

### Why this matters

This supports later reasoning about routes, paths, and impacted regions.

---

## 11 — Buffers and Zones

### Goal

Create zones of influence around points or lines.

### Students will practice

- buffering points by different distances
- visualizing impact zones
- comparing small and large buffers
- discussing geographic CRS limitations

### Why this matters

Buffers introduce area-based reasoning and set up future damage-zone logic.

---

## 12 — Installing and Using the WDO Library

### Goal

Install and use the reusable helper code stored in `src/wdo`.

### Students will practice

- understanding the `src` project layout
- reading the purpose of `pyproject.toml`
- running `pip install -e .`
- importing helper functions from `wdo`

### Why this matters

At this point students have seen enough repeated geometry code that packaging helper functions now feels useful instead of mysterious.

---

## 13 — Refactoring Spatial Code into Reusable Helpers

### Goal

Organize repeated notebook code into reusable functions and small helper classes.

### Students will practice

- identifying repeated code
- refactoring into helper functions
- deciding when a small class is useful
- separating map state from geometry logic

### Why this matters

Students move from “working notebook code” to **reusable project code**.

---

# Suggested Notebook Naming

A clean naming scheme might look like this:

```text
00-Paths_and_Working_Directories.ipynb
01-JSON_and_GeoJSON_Basics.ipynb
02-Viewing_GeoJSON_with_Folium.ipynb
03-Properties_Styling_and_Filtering.ipynb
04-Bounding_Boxes_and_Extent.ipynb
05-Interactive_Maps_with_ipyleaflet.ipynb
06-Point_in_Polygon.ipynb
07-Haversine_Distance.ipynb
08-Bearings_and_Destination_Points.ipynb
09-LineStrings_and_Trajectories.ipynb
10-Line_Polygon_Intersections.ipynb
11-Buffers_and_Zones.ipynb
12-Installing_the_WDO_Library.ipynb
13-Refactoring_Into_Reusable_Helpers.ipynb
```

---

# Notes for Students

- Each notebook teaches **one new capability**
- Not every notebook is a full assignment
- The final project is where these ideas are assembled together
- You are not expected to memorize everything — you are expected to build and reuse your own notes and examples

---

# Notes for Instructor

### Merge candidates

- working directory + data elsewhere
- styling + filtering + property inspection
- WDO helper library + installing local library

### Split candidates

- current “lines and distances” content into:
  - distance notebook
  - line notebook

### Delay until later

- local package installation
- refactoring into a mini library
- class-based notebook cleanup patterns

Those topics are valuable, but they make more sense **after** students see why repetition becomes a problem.

---

If you want, next I can turn this into a **more polished markdown file with brief prerequisites and “used later in project milestone X” tags**.
