

# 🔥 MICRO LESSON 5 — Styling Without Logic

### Goal:
Manipulate feature properties dynamically.

### Task:
- Load the world GeoJSON.
- Color **only countries whose name starts with A–M** one color.
- Color N–Z another color.
- No manual hardcoding of country names.

### Concepts Reinforced:
- Attribute inspection
- Lambda styling functions in Folium
- Feature properties access
- Avoiding brute force

### Why this works:
They must:
- Look at feature["properties"]
- Extract a field
- Apply conditional logic

But they are NOT:
- Computing distances
- Doing intersections
- Solving missile logic

---

# 🔥 MICRO LESSON 6 — Filtering Without Geometry

### Goal:
Teach spatial data filtering without spatial math.

### Task:
- Display only countries with population > X (you choose threshold).
- Everything else should not render.

OR

- Display only countries in the Western Hemisphere (based on centroid longitude).

### Concepts Reinforced:
- GeoPandas filtering
- Centroid property
- Boolean masks
- Attribute vs geometry filtering

They begin to see:
> Data drives map output.

---

# 🔥 MICRO LESSON 7 — Bounding Box Reasoning

### Goal:
Teach spatial extent awareness.

### Task:
- Compute bounding box of world dataset.
- Print:
  - min_lat
  - max_lat
  - min_lon
  - max_lon
- Add a rectangle layer showing the bounding box.

### Why this matters:
Before distance.
Before trajectory.
Before missile math.

Students must understand:
> Every dataset has spatial extent.

And this lesson reinforces:
- Geometry bounds
- Coordinate ordering
- Folium Rectangle

---

# 🔥 MICRO LESSON 8 — Distance Without Context

### Goal:
Teach Haversine independently of threats.

### Task:
- Compute distance between:
  - Your base
  - 5 manually chosen capitals
- Output sorted list from closest to farthest.
- Display results in popup markers.

No trajectories.
No missiles.
No damage zones.

Just pure:
- Distance math
- Sorting
- Units sanity

This aligns directly with Milestone 2 in your spec  [oai_citation:1‡README.pdf](sediment://file_000000003004722fb1f460f4a5de6b06) without unlocking everything.

---

# 🔥 MICRO LESSON 9 — Bearing Without Destination

### Goal:
Understand compass math.

### Task:
- Given:
  - Base location
  - Bearing = 45°
  - Distance = 500km
- Compute and plot destination point.

Do NOT:
- Create intermediate points.
- Create lines.
- Animate.

Just:
Start → single computed end point.

This isolates:
- Trig
- Degree vs radian conversion
- Earth curvature assumptions

---

# 🔥 MICRO LESSON 10 — Lines Without Meaning

### Goal:
Construct geometry explicitly.

### Task:
- Create a LineString between:
  - Base
  - Computed destination
- Add to map.

That’s it.

No threat types.
No buffering.
No intersection.

Now they know:
- Point
- Line
- Styling

---

# 🔥 MICRO LESSON 11 — Intersections Without Drama

### Goal:
Teach intersects() in isolation.

### Task:
- Draw a random diagonal line across the world.
- Determine which countries it intersects.
- Print their names.
- Highlight them in a new layer.

No missile.
No threat logic.
Just:
> Line vs Polygon

This directly scaffolds Milestone 4  [oai_citation:2‡README.pdf](sediment://file_000000003004722fb1f460f4a5de6b06) without giving them the final structure.

---

# 🔥 MICRO LESSON 12 — Buffers Without Explosions

### Goal:
Teach buffer concept clearly.

### Task:
- Create 3 points.
- Buffer them with:
  - 100km
  - 300km
  - 600km
- Overlay semi-transparent.
- Observe differences.

Ask:
- What changes when CRS is geographic?
- Why do buffers look weird near poles?

This plants seeds for:
Milestone 5 damage zones  [oai_citation:3‡README.pdf](sediment://file_000000003004722fb1f460f4a5de6b06).

---

# 🧠 Now — About “Not Spoon Feeding”

The trick is:

You never combine:
- Distance
- Bearing
- Line
- Intersection
- Buffer

In one micro lesson.

You isolate them.

The project is the first time they assemble them.

---

# 🧩 Alternate Creative Micro Lessons

If you want more playful:

### 🟡 “Threat of Letters”
Color countries based on:
- Number of letters in their name.
- Even vs odd.

Teaches:
Attribute transformation.

---

### 🟡 “Hemisphere Filter”
Shade countries differently based on:
- Whether centroid latitude > 0.

Teaches:
Geometry-derived attributes.

---

### 🟡 “Closest Neighbor”
Find the two closest country centroids globally.

Teaches:
Pairwise distance.

---

### 🟡 “Trajectory Prediction Lab”
Given 3 bearings from base:
- 0°
- 120°
- 240°
Plot endpoints.
Discuss:
Why are they not evenly spaced visually?

Teaches:
Projection distortion awareness.

---

# ⚖️ The Pedagogical Balance

Right now your instinct is correct:

Project 01 can be generous.
Project 02 you tighten the screws.

Because once they understand:
- Geometry objects
- CRS
- Distance
- Intersection
- Buffer

You stop showing them how to chain it.

---

# 🎓 If You Want To Be Evil (Constructively)

Instead of:
“Load world boundaries”

Say:
> Load a country boundary dataset and confirm it contains polygon geometries.

Make them discover:
- geometry type
- .geom_type
- .unique()

Subtle. Powerful.

---

# 🧠 Meta Advice

Your pacing problem is not about content.

It’s about:
> When does isolation become assembly?

Micro lessons should feel like:
“Here’s a new Lego brick.”

The project is:
“Build the castle.”

---

If you want next:

- I can design a **2-week micro lesson progression map**
- Or build a **micro lesson template format** you reuse every time
- Or help you decide which lessons become graded vs practice

You’re building a really solid spatial reasoning curriculum here.

And the WDO thanks you. 🌍🚀