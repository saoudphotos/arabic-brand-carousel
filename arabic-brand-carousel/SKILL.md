---
name: "arabic-brand-carousel"
description: "Builds a branded Arabic Instagram carousel from any topic: the user gives the topic, and the skill analyzes it and designs the slides, asking only for brand details it cannot infer. Use for any carousel request."
---

# Arabic Brand Carousel

The user gives a topic. You do the analysis and the design. Ask only for what you cannot infer, in one short message. Write in the user's dialect.

## Step 1: Brand details (ask only if missing)

If the user already shared brand details in this conversation or in an earlier carousel, use them. Otherwise ask once, in one message:
- Brand mark: a logo file, a wordmark, or a handle.
- Colors: a base color and an accent color.

If the user does not answer or does not know, use a default and say so in one line: a near-black base, off-white text, and one bright accent. Do not ask about font, layout, or structure. Decide those yourself.

If the user shares an existing carousel or post, read its colors, fonts, and layout from the images and use them.

## Step 2: Analyze the topic

Decide these yourself before designing:
- The core idea in one sentence.
- The audience and what they want from it.
- The angle: surprise, a practical how-to, a list, a comparison, or a story.
- The number of slides: 7 by default, up to 10 for lists.
- Facts and numbers: verify them before writing. If the content relies on news, research, or an official document, add a source line on the relevant slide.

## Step 3: Plan the slides

- Slide 1 (cover): a hook that stops the scroll. Pick the cover type that fits the topic:
  - Question with a highlighted keyword, for curiosity.
  - Number with a bold promise, for lists.
  - Visual hero, for tech and product topics or any topic that benefits from imagery (see Step 4).
  - Single bold word with a highlight, for opinions and warnings.
- Slides 2 to N-1: one idea per slide. Vary the layouts so the carousel does not feel repetitive. Layouts: cards with icons, numbered list, before and after, chip grid, step-by-step, or a large statement.
- Last slide: one engagement prompt. Pick the one that fits: a comment keyword, "save it for later" with "send it to someone", or a question for the audience. Show the brand mark.
- Each slide has under 40 words.

## Step 4: Design rules (apply to every slide)

Layout is fixed at 1080 x 1350.

Brand bar, repeated on every slide:
- Top left: slide counter (e.g. "3 / 7"), small and muted.
- Top right: a category pill with a short topic label.
- Bottom left: the brand mark or handle, small.
- Bottom right: a swipe cue in the accent color, on every slide except the last.

Typography:
- Default font: Cairo, weight 900 for headlines and 700 for labels and body. Cairo is a bold Arabic font with clear letterforms at display sizes.
- Use the font when rendering the slides to images, so the font is baked into the PNG files. The viewer does not need the font installed. Do not rely on online font imports, since they fail when offline.
- If the user's brand uses another font, use that one instead, loaded the same way.
- Headlines: 110 to 130 px on covers, 90 to 120 px on content slides. Body text: 40 to 50 px. Gray label above the headline: 36 to 44 px.
- Right-to-left layout.
- Keep at least 80 px margin from every edge.

Emphasis:
- One highlighted word per headline, in the accent color, with a hand-drawn underline. One highlight per slide.
- A slide can use its own accent when it covers a different item, such as a color, a tool, or a step. Use that color for its underline, label, and dot. Otherwise keep one accent for the whole series.

Visuals:
- One visual element on the cover and on key slides. Pick one that fits the topic:
  - Device mockup or product image, for tech.
  - Row of colored dots, for lists of items that each have a color.
  - Abstract shapes, when no photo is available: concentric circles, an arch frame, stacked cards, diagonal stripes, a sunrise half-circle, pill buttons, a dotted grid, or hexagons. Keep them large, and keep them away from the headline so text stays readable.
  - Photos, only when the user uploads them or approves generating them.
- A soft glow in the accent color behind the visual adds depth.
- Decoration must support the idea. Remove anything that does not.

## Step 5: Check before delivery

- The cover explains the topic in under two seconds.
- Fonts and colors match across the series.
- The brand bar is aligned on every slide.
- No shape or visual overlaps the headline. Check this in the rendered image, not only in the code.
- Text is readable against the background.
- Dialect text has no spelling errors.
- Score the carousel out of 100. Give one reason for each lost point and one concrete fix.

## Delivery

Build one HTML file with every slide at 1080 x 1350. Keep it as the editable source.

Render each slide to PNG with a headless browser, using the Cairo font loaded from a local file. The PNG files are the final deliverable, since they include the font and can be posted as they are. Send the PNG files to the user for review. Export the final set only after the user approves the design.

Then explain in one or two sentences why you chose this cover and layout, and offer one next change.
