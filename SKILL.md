---
name: context-to-html
description: Create distinctive, self-contained HTML explainers, visual summaries, infographics, timelines, comparisons, and process maps from supplied content or conversation context. Use for one-page visual artifacts, not full applications or production websites.
---

# Context to HTML

Turn the source into an actual `.html` artifact with a clear editorial point of view and a visual form specific to its subject. A nicely styled transcript or a grid of summary cards is not enough when the material contains relationships worth showing.

Before designing, read [references/visual-standard.md](references/visual-standard.md). It contains art-direction choices, composition examples, and the visual acceptance checks.

## Ground the content

- Use the specified source; for “this conversation”, extract the relevant substance and omit coordination chatter and tool logs.
- Preserve facts, numbers, names, causality, qualifications, and open questions. Keep synthetic examples clearly labeled. Never invent evidence or turn an unknown into a negative claim.
- Match the user's language. Honor their reference, brand, requested format, and existing design system before choosing a new direction.
- Infer the audience and purpose when possible. Ask only when missing source material would materially change the artifact; ordinary design choices do not need approval.

## Make the design decision before the code

Form a short internal brief: **reader takeaway → content relationship → main visual → composition → type and color character**. “Clean, modern, professional” does not decide any of these.

Consider two plausible directions briefly and choose the one that makes the source easiest to understand and remember. Do not generate multiple pages or ask the user to choose unless requested. For a small task, a sentence of internal planning is enough.

- Match visual grammar to the source: sequence, dependency, comparison, composition, quantitative pattern, or argument. Do not draw unsupported connections or charts without data.
- For substantial material, build around one dominant explanatory visual: an annotated process, evidence chain, comparison, map, timeline, or data graphic. Integrate it into the opening composition instead of placing a generic hero above it.
- Use a clear headline that carries the actual conclusion, or the central question when the source has no conclusion, without overstating certainty. Put supporting evidence beside the claim or part of the visual it explains.
- Give sections different jobs and appropriate shapes. Use rows for comparable items, a table for precise comparison, connected steps for a process, and prose for nuance. Cards are useful for independent items, not as the page's universal container.
- Scale the composition to the source. A short note can be one striking typographic composition; do not inflate it into a dashboard or invent sections to fill space.

## Build one portable file

- Create a descriptively named `.html` in the requested location, or the current workspace. Deliver the file, not only code.
- Inline HTML, CSS, JavaScript, and SVG. Default to no build step, CDN, external font, remote asset, or runtime dependency. Use installed fonts with fallbacks; embed supplied local assets when useful. Source links can remain ordinary links.
- Prefer semantic HTML, CSS Grid/Flexbox, custom properties, and inline SVG. Keep essential content available without JavaScript and when opened directly from disk.
- Recompose at narrow widths; do not merely shrink a desktop diagram. Keep labels readable, connectors meaningful, controls keyboard usable, and focus visible. Respect reduced motion and use more than color to convey meaning.
- Escape HTML-significant source text. In interactive features, insert untrusted text with `textContent`, not `innerHTML`.
- Add print styles when the artifact is likely to be saved or shared as a document. Reveal essential expandable content for printing.

## Inspect and revise

When browser tooling is available, open the actual file and inspect desktop and narrow screenshots (for example, 1440 × 900 and 390 × 844), plus the full page and an intermediate width where the layout changes. Check overflow, label collisions, console errors, controls, keyboard focus, and offline dependencies. Otherwise do a structural check and disclose that the render was not verified.

Apply the visual acceptance checks in the reference. If source material with a different underlying relationship could replace the content by changing only text and accent color, revise the composition or main visual. More shadows, gradients, or animation do not fix that failure. Recheck after the revision.

Return a clickable HTML link and one sentence describing the visual approach. Mention material assumptions and any unverified behavior concisely. Do not narrate the internal design deliberation.
