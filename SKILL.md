---
name: context-to-html
description: Create a polished, self-contained HTML visual from supplied content or the relevant conversation context. Use for HTML visualizations, visual summaries, infographics, concept pages, explainers, timelines, comparisons, process maps, and presentation-like one-page artifacts; not for full multi-file web applications or production websites.
---

# Context to HTML

Turn the user's source material into an actual `.html` artifact that communicates the ideas more clearly than prose alone. Treat this as information design and editorial composition, not as a generic dashboard template.

Before designing or writing the file, read [references/visual-standard.md](references/visual-standard.md).

## Resolve the source

- When the user points to specific content, use that content.
- When they say "this conversation", "the idea above", or similar, extract the relevant substance from the preceding conversation. Exclude coordination chatter, tool logs, and unrelated turns.
- Preserve facts, numbers, names, qualifications, and causal claims. Do not invent supporting data or silently strengthen uncertain claims.
- Match the user's language unless they request another one.
- Make reasonable structural and visual assumptions without pausing for preferences. Ask only when missing source material would materially change the artifact.

## Shape the story

Identify the main takeaway, the intended audience if evident, and the relationships in the material. Choose a visual grammar that fits those relationships—for example, a timeline for sequence, a flow for causality, a comparison for alternatives, a system map for connected actors, or an editorial explainer for a developing idea. Do not add charts when there is no quantitative evidence.

Organize the page around one clear narrative. Lead with the strongest insight, group supporting material into meaningful sections, and end with implications, decisions, next steps, or open questions when the source supports them. Remove repetition while retaining meaningful nuance.

## Build the artifact

- Create a descriptively named `.html` file at the user's requested location, or in the current workspace when none is specified. Deliver the file, not merely a code block.
- Put all HTML, CSS, JavaScript, and SVG in that one file. By default, use no build step, CDN, external font, remote image, or runtime dependency. Links cited by the source may remain ordinary links.
- Prefer semantic HTML, CSS Grid/Flexbox, CSS custom properties, and inline SVG for diagrams or small data graphics. Properly escape source text that contains HTML-significant characters.
- Make the page responsive, readable, and useful at both desktop and narrow widths. Include print-friendly behavior when it helps the artifact's likely use.
- Use interaction only when it improves comprehension. Any controls must work with pointer and keyboard input; essential information must remain available without JavaScript.
- Respect `prefers-reduced-motion`, maintain visible focus states and adequate contrast, and avoid conveying meaning with color alone.

## Verify and hand off

Open and inspect the rendered file when browser tooling is available. Check at desktop and narrow widths, correct console errors, overflow, clipped labels, broken controls, unreadable contrast, and layout collisions. Otherwise inspect the document for complete structure, inline dependencies, and obvious markup or CSS errors.

Return a clickable link to the HTML file and a concise description of the chosen visual approach. Mention assumptions only when they affect meaning.
