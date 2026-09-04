# Lunexa — Forge Design Direction

## Three stylistic approaches

### Theme Name: Blacksmith Cinema
Very Brief Intro: A dark, tactile, editorial fitness experience inspired by industrial product films and forged metal. The interface is sparse, spatial, and built around one hero object.
Probability: 0.07

### Theme Name: Monolith Protocol
Very Brief Intro: A severe architectural direction using brutalist composition, monumental type, and controlled motion to make training feel like entering a private institution.
Probability: 0.03

### Theme Name: Ember Precision
Very Brief Intro: A warmer luxury-performance direction with bronze light, restrained grain, and a more human rhythm that balances intensity with ritual.
Probability: 0.09

## Selected approach: Blacksmith Cinema

### Design Movement
Contemporary cinematic product design fused with industrial minimalism and the restraint of luxury automotive art direction.

### Core Principles
1. One hero object, one clear action: the barbell is the main character and the UI recedes around it.
2. Darkness creates focus: near-black surfaces and large negative space make bronze light feel earned.
3. Motion is physical: rotations, camera drift, and plate loading should feel weighted rather than decorative.
4. Interface as atmosphere: labels, status marks, and controls are integrated into the scene instead of boxed into dashboard components.

### Color Philosophy
Black and charcoal establish a quiet, premium chamber. A single ownable bronze accent signals heat, effort, and crafted metal; it is reserved for interaction states, progress, and light-catching edges. Off-white typography remains slightly softened to avoid sterile white-on-black contrast.

### Layout Paradigm
A full-viewport stage with asymmetric overlays: a slim utility rail, a low-left narrative lockup, and a right-side interaction stack. No conventional navbar or repeated content grid. Progress is expressed as a vertical scene index and small spatial markers.

### Signature Elements
- Thin bronze hairlines and a vertical scene index that behaves like a film timeline.
- Technical micro-labels with wide tracking, such as SYSTEM / 001 and LOAD VECTOR.
- Subtle grain, vignette, floor reflections, and radial light sweeps that make the browser feel like a physical chamber.

### Interaction Philosophy
Every control should reveal more of the object. Dragging rotates the barbell with direct manipulation; tapping plates loads weight; mode selection changes the chamber's atmosphere. Feedback is concise and sensory, never modal or cluttered.

### Animation
Use slow idle rotation and camera drift as a breathing state. Entering the experience uses a controlled light sweep and opacity reveal. Weight loading uses short spring-like translations and plate spacing changes. The transformation stage uses a dark hold, then a restrained vertical lift. Respect reduced motion by replacing camera moves with opacity and small positional changes.

### Typography System
Use Space Grotesk for headlines and IBM Plex Mono for technical microcopy. Headlines are compact, bold, and slightly tight; supporting copy is small, airy, and tracked. Large type is reserved for scene statements and the final CTA.

### Brand Essence
FORGE is a cinematic strength ritual for people who train with intent, not noise. Personality: exacting, grounded, relentless.

### Brand Voice
Headlines are declarative and spare. CTAs are verbs with direction, never hype. Microcopy sounds like a piece of equipment label.

Example lines:
- Discipline has a shape.
- Load the bar. Find the edge.

### Wordmark & Logo
A custom geometric FORGE wordmark paired with a compact four-notch anvil mark: a squared bronze glyph with a central vertical cut that echoes a barbell collar.

### Signature Brand Color
Forged Bronze — #B8662E, used as a precise glint rather than a wash.

## Content model

All editable content is centralized in `client/src/lib/content.ts`, including brand name, scene copy, training modes, weight increments, and final CTA text.

## Build notes

The implementation uses a procedural Three.js-style canvas treatment built with CSS and DOM geometry to keep the static experience lightweight and resilient, while preserving the requested 3D-product-render feeling. Desktop supports pointer dragging and plate clicks; mobile supports touch dragging and tap loading. Sound is opt-in and represented by a mute toggle with no autoplay.

## Style Decisions

The scroll revision keeps Blacksmith Cinema strict across the full journey. Every chapter now exposes a visible scene cue through a persistent bronze hairline, dynamic sequence metadata, a physical state readout, or a declarative Space Grotesk statement. The barbell remains continuously present and gains stronger edge-light, metal texture, and floor reflection treatment as the scroll deepens. Forged Bronze #B8662E remains restricted to glints, active marks, numerals, hairlines, and CTA emphasis. FORGE owns the visual hierarchy; Lunexa stays a quiet studio signature.
