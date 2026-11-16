# Visual standard: specific, expressive, useful

Aim for a designed explanation whose subject is recognizable from its composition. Precision and personality can coexist. Expressiveness comes from a meaningful visual, decisive scale, and rhythm, not from accumulating effects.

## Choose a direction, not a skin

Start with the source relationship and the reader's task. A color palette is not an art direction. Choose how the content occupies space, what dominates, and how evidence attaches to it.

These are examples, not templates or a required menu. Combine, adapt, or choose another direction when the source calls for it:

| Direction | Useful for | Composition and character |
| --- | --- | --- |
| Editorial spread | Arguments, research synthesis, decisions | A thesis at contrasting scale, a large annotated visual, short evidence columns or margin notes; expressive type and deliberate whitespace |
| Technical field guide | Systems, dependencies, operating processes | A precise schematic or cross-section, clear paths and boundaries, labels attached to parts, restrained instrument-like metadata |
| Evidence dossier | Audits, uncertain findings, source analysis | Claim paired with evidence and qualification; references, ruled rows, visible distinction between observed and unknown |
| Comparative plate | Alternatives and trade-offs | Aligned criteria, a shared baseline, mirrored structures or a spectrum; differences visible in position as well as color |
| Route or atlas | Histories, journeys, connected actors | A path, branching route, or spatial map with landmarks and local annotations; scale and direction carry meaning |
| Typographic poster | One short idea or a small set of principles | A compact, confident composition; an oversized key phrase and a carefully placed explanation instead of artificial sections |

For repeated artifacts, choose again from the new content. Do not reuse the previous palette, hero, and section order by habit. When the user supplies a design reference or requests consistency, work within it.

## Compose around the explanation

Make the opening a complete thought: a meaningful headline, enough context to interpret it, and a visible entry into the main visual. Avoid a tall empty hero that pushes the explanation below the first screen.

- Establish one dominant element, a supporting layer, and quiet annotations. Equal-sized blocks give everything equal weight.
- Use the grid to express relationships: a wide diagram with a narrow commentary rail, aligned opposing columns, a full-width process with notes under its stages. Centered framing is an option, not a default.
- Alternate spatial roles when the material warrants it: open diagram, dense evidence rows, quiet conclusion. A compact artifact may need only one composition.
- Put a qualification where it changes interpretation. A chart caveat buried in the footer is too far away.
- Make graphic marks do work. A boundary can show scope, an arrow can show sequence, a gap can distinguish groups. If a line implies no real relationship, remove it.

### From generic to specific

**Process:** “title → three rounded feature cards → conclusion” becomes a connected process with inputs, transitions, output, and qualifications attached to the relevant stage. Add a failure branch only if the source supports it.

**Comparison:** scattered pros-and-cons cards become aligned rows by criterion, so the reader can compare the same property without hunting.

**Research:** a wall of summary panels becomes an evidence chain with the central finding at large scale, source observations alongside it, and uncertainty marked where the inference occurs.

Do not implement all these patterns in one page. Choose the one that explains the source.

## Give type and color a deliberate role

Offline does not mean one default sans-serif everywhere. Choose from available local families with fallbacks; do not claim that naming a font installs it. Check Cyrillic when the source is Russian.

- Editorial material can use a local serif display face with a neutral sans body. Technical material can use a precise sans with monospace only for code or compact metadata. A single family with contrasting scale and weight can also be enough.
- Use fluid display sizes with `clamp()` and intentional line breaks or `text-wrap: balance`. On desktop, a short headline can be substantially larger than the body; long scientific titles need a different treatment. Do not shrink the explanation to make the title fit.
- Body text usually works at 16–20 px with a line-height around 1.5–1.7 and a measure near 45–75 characters. Diagram labels must be comfortable at actual display size, not just when zoomed.
- Avoid all-caps paragraphs, excessive tracking, tiny gray labels, and layers of low-contrast metadata. Use uppercase sparingly; keep numbers and units together.
- Choose a base, ink, accent, and any necessary semantic colors for this subject. Color may occupy a large purposeful field; it need not be limited to small chips. Maintain readable contrast: at least 4.5:1 for normal text and 3:1 for large text and essential graphical controls.
- A paper-like surface, deep ink background, warm industrial accent, or vivid flat field can all work. Default purple-blue gradients, neon, glass, and beige editorial styling are not substitutes for a decision. No palette is a universal fix.
- Use rules, texture, shadows, and radii according to the concept. A faint grid can support a schematic; random glowing blobs cannot explain one. Most sections need no container background.

## Draw the actual relationship

Prefer HTML/CSS for labeled rows, tables, and steps. Use inline SVG when precise geometry, connectors, or a plot add understanding.

- Encode with position, length, grouping, or direction before color. Keep the same scale for values that will be compared.
- Preserve units, baselines, time ranges, sample definitions, and source notes when provided. Distinguish measured, estimated, and illustrative values visibly.
- Never invent trend lines, percentages, progress bars, satisfaction scores, or decorative dashboards. Qualitative source material calls for qualitative structure.
- Attach labels to their objects and keep connector routes clear. Provide an accessible name and a textual counterpart for important diagrams; avoid repeating the whole diagram to screen readers twice.
- Size labels for reading, independently of quantitative marks. A small segment can keep its true proportion while its annotation moves into a keyed legend; reflow before the label's column becomes too narrow, including at intermediate widths.
- For a narrow screen, use an equivalent stacked process, aligned comparison rows, or a simplified map with its relationships intact. Use local horizontal scrolling only when a table or diagram truly needs it, with a visible cue and keyboard access. Do not hide page overflow to mask a broken layout.

## Interaction should reveal something

Add controls when they answer a reader's question: expand evidence, compare real scenarios, highlight a route, or navigate a long explanation. Use native `details` when it is enough. A static artifact is a valid finished result.

- Core claims stay visible. Do not make hover, a carousel, or a tab hunt necessary to understand the thesis.
- Controls need clear labels, working pointer and keyboard input, visible focus, and state communicated in text or ARIA. No decorative buttons or links to `#` with no destination.
- Motion can guide attention to a relationship or a state change. Avoid perpetual floating, gratuitous counters, cursor effects, and scroll-gated reading. Content starts readable even when scripts fail.
- Honor `prefers-reduced-motion`; do not require animation to understand a diagram. Disable nonessential animation for print.

## Visual acceptance checks

Inspect screenshots as a reader, not only as an implementer:

1. **First screen:** Can the reader name the main point and see the main explanatory structure? If the title consumes the screen, rebalance it.
2. **Thumbnail:** At reduced scale, are a focal point and a reading order still obvious? If every block competes equally, change scale and placement.
3. **Subject swap:** Could content with a different underlying relationship replace the text without changing the main visual or layout? If yes, design the actual relationship instead of recoloring the template. Familiar forms such as tables are welcome when their encoded structure fits the source.
4. **Evidence:** Are important claims, uncertainty, and source references preserved and located together? Do shapes, arrows, or area sizes imply facts absent from the source?
5. **Mobile:** Are labels readable and relationships preserved at a narrow width? Check a full-page capture for overflow, collisions, excessive empty space, and broken reading order.
6. **Usability:** Do controls and focus work, is contrast sufficient, does reduced motion retain meaning, and is essential content available without scripts or remote requests?

When a composition fails, revise the visual grammar, hierarchy, or spatial arrangement. Do not treat decorative polish as a repair. Deliver the inspected version and state any checks that could not be performed.
