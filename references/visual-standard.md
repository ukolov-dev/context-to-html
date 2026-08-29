# Visual standard for single-file HTML artifacts

Use these principles to make each artifact feel intentionally designed for its content rather than poured into a reusable template.

## 1. Begin with information design

Determine what the reader should understand, feel, or decide after viewing the page. Establish a clear hierarchy:

1. A concise thesis or framing statement.
2. The most important evidence, structure, or relationships.
3. Supporting detail and nuance.
4. A useful conclusion: implications, next actions, unresolved questions, or a summary.

Select the visual form from the content:

| Relationship in the source | Useful visual forms |
| --- | --- |
| Sequence or evolution | Timeline, stepped path, chapters |
| Cause, dependency, or workflow | Connected flow, decision tree, pipeline |
| Alternatives or trade-offs | Side-by-side comparison, spectrum, matrix |
| Hierarchy or composition | Layered stack, tree, nested regions |
| Actors or connected concepts | Ecosystem map, hub-and-spoke, network |
| Quantitative pattern | Bars, dots, slope, compact data table |
| Argument or emerging idea | Editorial explainer, annotated manifesto, evidence chain |
| Plan or operating model | Phases, workstreams, milestones, responsibility map |

Do not visualize a relationship that the source does not support. If the material is qualitative, favor structure, labels, annotated flows, and strong editorial layout over invented metrics.

## 2. Create a content-specific art direction

Choose a visual concept that reflects the material's tone: analytical, optimistic, urgent, technical, archival, playful, or restrained. Let that concept shape the palette, geometry, iconography, density, and motion.

- Use a small, coherent palette: a base surface, readable text, one primary accent, and optional semantic colors.
- Use high-saturation color selectively for emphasis. Avoid default purple-blue gradients, excessive glass effects, and neon-on-dark styling unless they genuinely fit the subject.
- Use borders, shadows, textures, patterns, and gradients with restraint and a clear purpose.
- Create depth through scale, spacing, alignment, contrast, and layering—not through decoration alone.
- Vary composition across sections while maintaining shared tokens and alignment. Avoid a page made entirely from identical rounded cards.

## 3. Typography and hierarchy

Use system fonts so the file remains offline and portable. A strong default stack is:

```css
font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
```

For editorial or archival concepts, a local serif stack can provide contrast:

```css
font-family: Iowan Old Style, Baskerville, "Times New Roman", serif;
```

- Use fluid type with `clamp()` for major headings.
- Keep body copy comfortably readable, generally around 16–19 px with generous line height and a sensible line length.
- Create obvious contrast between title, section heading, body, annotation, and metadata.
- Prefer short labels and direct sentences inside diagrams. Move explanation into nearby annotations rather than shrinking the type.
- Use uppercase and letter spacing sparingly, mainly for compact labels.

## 4. Composition and visual rhythm

Use a centered content frame with responsive side padding, but allow important diagrams or bands to break the normal text measure. Combine dense and quiet areas so the reader can scan and pause.

- Align elements to an intentional grid.
- Use whitespace to separate changes in thought, not just to create emptiness.
- Give the hero section a distinct role: establish the thesis and visual premise rather than repeating every later detail.
- Make the primary visual understandable at a glance, then reward closer reading with annotations or supporting detail.
- On narrow screens, recompose diagrams into stacked steps or scrollable regions only when stacking would destroy meaning. Never rely on viewport-wide fixed positioning.

## 5. Diagrams and data graphics

Prefer HTML/CSS for structured blocks and inline SVG for connector lines, plots, or precise geometry. Keep labels legible and attached to the objects they describe.

- Encode hierarchy with position and scale before relying on color.
- Add units, baselines, and source notes to quantitative graphics when available.
- Use consistent direction for flows unless a deliberate loop or return path is being shown.
- Ensure arrows and connectors remain visible at responsive breakpoints.
- Provide a textual counterpart or accessible label for important SVG content.
- Do not use decorative charts, meaningless progress rings, or fake dashboard statistics.

## 6. Motion and interaction

Static clarity is the default. Add interaction only for genuine layers of information, comparisons, or navigation.

- Good uses: expandable evidence, a meaningful scenario toggle, synchronized highlighting, or compact section navigation.
- Weak uses: gratuitous counters, constant floating animation, parallax, cursor followers, or hiding core content behind hover.
- Keep motion subtle and short. Disable or simplify it for `prefers-reduced-motion: reduce`.
- Make controls visibly interactive, keyboard reachable, and stateful through text or ARIA—not color alone.

## 7. Single-file engineering

Define design tokens in `:root` for colors, spacing, radii, shadows, and content width. Keep CSS organized by page region. Keep JavaScript small, local, and progressive.

The artifact should work when opened directly from disk:

- no module imports or fetch calls needed to render essential content;
- no externally hosted fonts, scripts, styles, or images by default;
- no framework-specific runtime;
- no broken asset paths;
- valid language metadata, document title, viewport settings, and meaningful heading order.

When source material includes code-like strings or markup, encode them safely. Avoid assigning untrusted source text through `innerHTML` in interactive features.

## 8. Final quality pass

Judge the rendered result, not only the source code.

- **Fidelity:** Every important claim is traceable to the source; uncertainty and open questions remain visible.
- **Narrative:** The reader can identify the thesis, follow the structure, and understand the conclusion.
- **Visual fit:** The design feels specific to the subject and the chosen diagram matches the actual relationships.
- **Hierarchy:** The most important content dominates; annotations and secondary detail stay secondary.
- **Craft:** Spacing, alignment, typography, connectors, borders, and color are consistent and deliberate.
- **Responsiveness:** No horizontal clipping, overlapping labels, microscopic text, or unusable controls at narrow widths.
- **Accessibility:** Contrast, focus, semantics, keyboard use, reduced motion, and non-color cues are covered.
- **Portability:** The single file opens offline and does not depend on unavailable resources.

If the page still resembles a generic card dashboard, revise the composition and art direction before handing it off.
