# Precursor to Railroad Project

## 100% Libraries vs From Scratch

The two bad extremes are:

- **Library worship**: “A package exists, therefore I understand it.”
- No, you rented intelligence for five minutes.

- **From-scratch purism**: “Real computer scientists implement every algorithm themselves.”
- Also no. That is how you end up hand-rolling compression, authentication, and sadness.

The real skill is not “always build” or “always borrow.” The real skill is:

> **understand enough to judge the abstraction**

## Better Approach

## 1. Build a small version yourself

So you understand:

- the data structure
- the algorithm
- the tradeoffs
- where the pain comes from

## 2. Use the industrial tool after that

So you appreciate:

- why the tool exists
- what work it is saving you
- what assumptions it is making

## 3. Never use a library as a substitute for thinking

- A library is a tool, not a brain transplant.
- That is the blurry-area answer, but it is the honest one.

# A concrete classroom philosophy

For your spatial course, something like this works beautifully:

## Students should hand-build (based on 40MB railroad geojson)

- a simplification experiment
- zoom-based layer switching
- maybe a crude bounds check
- a simple graph from rail segments
- a point-in-polygon test
- a basic distance/bearing workflow

Because those are concept-rich.

## Students should not be expected to hand-build:

- a full tile engine
- a production-grade vector tile pipeline
- a robust CRS engine
- browser rendering internals
- industrial topology repair


# The distinction I want to get across

There are really three levels:

## Level 1 — Understand the idea

Can you explain it?
Can you sketch it?
Can you build a toy version?

## Level 2 — Implement a small version

Can you make it work on a modest dataset?
Can you see the tradeoffs?

## Level 3 — Recognize when professionals have already solved the ugly parts

> Can you evaluate a tool and use it responsibly?

- That progression is very CS.
- It respects both:

  - theory and implementation
  - practical engineering judgment

# A good approach I emphasize

> “If you can’t build a small version, you probably don’t understand it. 

> If you insist on building the full version every time, you probably don’t understand engineering.”

I want them to remember the trades offs.

# The test I like

When deciding whether to build or borrow, ask:

## Should we build it ourselves?

Yes, if:

- it teaches the core concept
- the small version is manageable
- correctness is easy to verify
- implementation pain is educational

## Should we use a library?

Yes, if:

- the problem is already well-solved
- correctness is tricky
- performance matters
- edge cases are brutal
- the implementation burden hides the actual lesson

That last one matters a lot in teaching.

Sometimes writing it yourself is not “more rigorous.”  
Sometimes it just burns all the oxygen in the room.

# Railroad example

The railroad geojson is  exactly the kind of thing where a layered approach is ideal. The 40mb file needs to be processed and turned into different granularity's based on zoom levels.

## Students write:

- manual simplification
- multiple detail layers
- zoom switching logic

They learn the concept.

## Then you show:

- vector tiling tools
- why they exist
- what they automate
- why nobody sane wants to hand-build all of it for real maps

That is a fantastic CS lesson, because it teaches both:

- computational thinking
- engineering judgment

# A phrase I think your students would benefit from

> **“We write enough ourselves to understand the machine, then we use the machine to do bigger work.”**

That’s a healthy mindset.

# Another framing that fits my field (CS) well

I am not teaching them to become passive consumers of libraries.

I am teaching them to become:

- informed users of abstraction
- capable debuggers
- occasional implementers
- good judges of when the abstraction leaks

That is a much better goal than “reinvent the earth.”

# In practice for this mini-project

I’d explicitly tell students:

## What we will build ourselves

- geometry simplification experiment
- multi-resolution outputs
- zoom-driven layer selection

## What we will not build ourselves

- full tile pyramid generation
- binary tile encoding
- vector tile protocol support
- industrial map-serving infrastructure

And then add:

> “You should understand what those tools do, even if you do not implement every byte of them.”

That is mature CS, not laziness.

# My blunt opinion

The phrase “real programmers write everything from scratch” is one of those macho nonsense ideas that sounds cool until deadlines, correctness, and maintenance show up with a baseball bat.

Real programmers:

- understand the fundamentals
- inspect the abstraction
- prototype intelligently
- reuse proven tools when appropriate

That’s the grown-up version.

# Best one-sentence rule

Here’s the version I’d put on a slide:

> **Build the smallest version that teaches the idea. Borrow the version that survives the real world.**

# End Precursor


My real question is can you take the lessons from my "precursor" and apply them to a project that I would like my students to attempt. I have a 40mb world railroad geojson file, and I would like them to attempt to process said 40mb file into a simplified set of rail data files (coarse/medium/fine/extra fine) which will be displayed based on zoom levels. I need help breaking this down into components, help with choosing our method of geometry simplification for each level of detail, and also how we will use our viewport to eliminate portions of the specific files that cannot be seen. I realize there are already libraries that create sets of vector tiles, but I want a simple program first, before we introduce the tried and true library version of how to solve the problem of too much data to load all the time at every zoom level. Can you provided an outline at first with some suggestions on how to solve this problem?


