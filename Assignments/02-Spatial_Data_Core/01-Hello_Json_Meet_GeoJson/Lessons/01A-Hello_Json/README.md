```yaml
title: 01A — Hello JSON → Getting to GeoJSON
artifact: README
course: OOP / Spatial Data crossover
purpose: Concept refresher + gentle on-ramp to GeoJSON
audience: Students who "know JSON" but don’t always *think* in JSON
tone: Friendly, slightly sarcastic, low-stakes but important
```

# 📘 Notebook Overview — *Hello JSON (Refresher) → Getting to GeoJSON*

This notebook is a **quick refresher and conceptual bridge**, not a deep dive.

Its job is to:
- reconnect JSON to something students already understand (Python dictionaries),
- expose common mental-model mistakes around JSON traversal,
- and quietly prepare students for **GeoJSON**, where structure suddenly matters a lot.

If JSON felt “easy” before, this notebook exists to show *why that confidence sometimes collapses* once nesting appears.

---

## What This Notebook Covers

### 1. JSON ≈ Python `dict` (With a Catch)
- Reinforces the idea that JSON maps cleanly to Python dictionaries and lists
- Emphasizes **structure over syntax**
- Highlights why “I know JSON” often means “I know flat JSON”

### 2. A Small, Generic JSON Example
- Walks through a realistic nested JSON object
- Demonstrates:
  - key lookup
  - list traversal
  - nested access patterns
- Focuses on *thinking in paths*, not just printing values

### 3. Your Turn (Hands-On)
- Students are asked to:
  - inspect structure
  - access nested values
  - reason about *where* data lives, not just *what* it is
- This section is intentionally lightweight but revealing

---

## Why This Matters (Even If It Feels Review-ish)

GeoJSON, APIs, configuration files, and modern data formats all assume:
- comfort with nested structures
- disciplined traversal
- zero fear of dictionaries-of-lists-of-dictionaries

This notebook is the **last low-pressure checkpoint** before JSON stops being forgiving.

---

## How This Fits in the Course

- Acts as a **bridge notebook** between:
  - basic Python data structures  
  - and structured spatial data formats (GeoJSON)
- Designed to be:
  - quick to complete
  - easy to revisit
  - useful as a reference later in the semester
