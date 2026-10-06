# Designing without AI tells

## What this is for

AI-generated interfaces have a recognizable signature, just as AI prose does. Designers, frontend communities, and increasingly ordinary visitors can spot a v0/Lovable/Claude-artifact page at a glance: the centered hero with a gradient word, the three-column grid of icons in rounded boxes, the left-border callout, the eyebrow label above every headline. None of these elements is wrong in isolation. The tell is the combination, the uniformity, and the fact that the same defaults appear regardless of brand, industry, or content.

This skill lists the attested visual tells and gives replacements for each, graded from simple (a five-minute CSS change) to complex (a structural rethink). It closes with a framework for choosing which grade of fix fits the design's overall context, and a revision pass to run before delivering.

Use it two ways. While designing, keep the patterns in mind so they never enter the layout. After building, run the revision pass as a dedicated review.

## The root cause (read this first)

Nearly every tell below comes from three underlying habits. Fix the habit, not just the instance, or the result is a new variant of the same slop.

**One: decoration substituting for content.** The model has learned that icons, badges, gradients, and cards read as "designed," so it adds them to fill visual space instead of letting real content (a product screenshot, a real number, a real customer name, actual UI) carry the page. The fix is almost always to replace the decoration with the specific thing it was standing in for. A page about a session replay tool should show a session replay, not a shield icon in a purple box labeled "Secure."

**Two: symmetry addiction.** Training on component libraries and templated SaaS pages pushes the model toward perfect grids, identical card heights, evenly repeated section rhythms, and centered everything. Human-designed pages have intentional asymmetry: one section is dense, the next breathes; one feature gets 60% of the width because it matters more. The fix is hierarchy. Decide what matters most and let the layout say so.

**Three: defaults left as defaults.** Tailwind's indigo, Inter, rounded-xl, shadow-md, and shadcn/ui's component shapes are excellent defaults, which is exactly why they are now a fingerprint. A design where every value is the framework default announces that nobody made a choice. The fix is a small number of deliberate, brand-specific decisions (one typeface with character, one owned color, one consistent corner radius that is not the default) applied consistently.

A useful test: cover the logo and the copy. If the page could belong to any SaaS company in any industry, it reads as AI regardless of how polished it is.

## Fast checklist

The highest-frequency offenders, for a quick scan:

1. Left-hand accent border on callouts, quotes, or cards (`border-left: 4px solid`).
2. Icon-in-a-rounded-box above every card title; icons used as filler throughout.
3. Eyebrow label above the headline; double eyebrow (pill badge plus uppercase label).
4. Gradient text on one word of the headline; purple/indigo-to-pink gradients anywhere.
5. Three-column grid of identical cards, repeated section after section.
6. Everything wrapped in a card; rounded-2xl and shadow on every container.
7. Centered hero: badge, huge bold headline, gray subhead, two buttons (solid + ghost).
8. Green checkmark bullet lists; three-tier pricing with the middle one highlighted.
9. Dark hero with glowing blurred blobs and glassmorphism.
10. Uniform fade-in-up scroll animations on every element.

## 1. Layout and structure tells

**The left-hand accent border.** A 3–4px colored strip down the left edge of a callout, blockquote, tip box, or card. It is the single most copied "designed" element in AI output because it appears constantly in documentation themes.

- Simple: remove the border and use a subtle background tint alone, or a hairline full border.
- Moderate: differentiate callouts by typography instead: a small bold label ("Note", "Warning") set in the brand color, body in regular text, no container at all.
- Complex: design a real callout language for the site: e.g. indented with a wider left margin and a single sentence set larger, or a footnote/sidenote system in the margin. Match it to the site's editorial voice.

**Uniform section rhythm.** Centered eyebrow → headline → subhead → grid of three cards, repeated four or five times down the page with only the words changing. The page scans as a template being filled.

- Simple: vary alignment per section (left-align one, center another) and vary the grid (3-up, then 2-up, then a single full-width feature).
- Moderate: give one section a fundamentally different treatment: a full-bleed screenshot, a data table, a timeline, a quote set huge with no container.
- Complex: structure the page around the argument rather than around sections. Lead with the strongest proof (product footage, a customer result), let section length follow content weight, and cut sections that exist only to fill the expected rhythm.

**Everything is a card.** Every piece of content boxed in a rounded rectangle with a shadow, including things that do not need containment, producing a page of floating tiles.

- Simple: remove containers from at least half the content; use whitespace and rules (thin horizontal lines) to separate instead.
- Moderate: reserve cards for genuinely interactive or self-contained items (a pricing plan, a linked resource) and set everything else as open composition on the page background.
- Complex: adopt an editorial layout: a typographic grid with columns, generous margins, and content that sits directly on the canvas, the way a well-set magazine page or Stripe-style docs page does.

**The alternating zig-zag.** Feature rows that alternate image-left/text-right, text-left/image-right, with identical proportions each time.

- Simple: break the alternation once: two rows same-side, or one row full-width.
- Moderate: vary the proportions (70/30, then 50/50) and the media type (screenshot, then diagram, then quote).
- Complex: replace the zig-zag with one deep interactive or scroll-driven demonstration of the product doing the three things, instead of three shallow rows asserting them.

**The centered hero formula.** Pill badge on top, tracking-tight 5xl–7xl bold headline (often with a gradient word), one-paragraph gray subhead, primary button plus ghost button, optional floating screenshot below with a glow.

- Simple: left-align the hero, drop the badge, make the headline a specific claim with a real number, use one button.
- Moderate: put real product UI in the hero at equal or greater visual weight than the headline; let the screenshot be straight and sharp rather than tilted-and-glowing.
- Complex: design a hero native to the product: a live embedded demo, an interactive input ("paste your URL"), or an unusual typographic composition. The hero should be un-reusable by any other company.

**Stats row of big numbers.** Three or four oversized figures with labels ("10x faster", "99.9% uptime", "24/7 support"), usually invented or unfalsifiable.

- Simple: cut any number that is not real and sourced; two true numbers beat four hollow ones.
- Moderate: set the one number that matters at large scale inside a sentence with attribution ("Teams at Acme cut replay storage costs 38% in the first quarter").
- Complex: replace the row with the evidence itself: a small chart of real data, a before/after, or a linked case study.

## 2. Component tells

**Icon-in-a-box feature cards.** A lucide/heroicons glyph inside a rounded, tinted square, above a bold title and two lines of text, three across. The definitive AI-page component of 2024–2026.

- Simple: delete the icons entirely; a title and one sharp sentence per feature loses nothing.
- Moderate: replace each icon with a cropped screenshot or micro-illustration of that actual feature in the product.
- Complex: commission or draw a consistent custom illustration/diagram style (line drawings, brand-specific spot illustrations, or annotated product frames) so the visuals carry information rather than category labels.

**Excessive icons generally.** An icon before every heading, every list item, every nav entry. Icons demoted to bullet decoration.

- Simple: strip icons everywhere they merely repeat the word next to them (a clock icon next to "Fast").
- Moderate: keep icons only where they do work: wayfinding in a dense dashboard, status indicators, actions. One icon style, one weight, one size scale.
- Complex: build a small custom icon set (or none at all) that matches the brand's line weight and geometry, rather than pulling from the same three libraries every AI page uses.

**Eyebrows and double eyebrows.** The small uppercase, letter-spaced label above a headline ("FEATURES", "WHY ACME"), and its escalation: a pill badge above the eyebrow above the headline. Three tiers of preamble before the actual content.

- Simple: delete the eyebrow. The headline can carry the section; readers do not need a category label for a section they are already looking at.
- Moderate: where sections genuinely need labeling (long docs-style pages), use a numbered or inline convention instead: "03 / Pricing" set small in the margin, or a running header.
- Complex: restructure headlines to make labels unnecessary: write section headlines that state the point ("One seat, every deal, no per-contact fees") so no meta-label above them is needed. Reserve pills exclusively for genuinely new, dated announcements, at most one per page.

**Checkmark bullet lists.** Green check circles down a feature list, or worse, checks and red crosses in a comparison.

- Simple: plain typographic bullets or an en-space and no marker at all.
- Moderate: turn the list into prose or a two-column definition list (term set bold, one-line specifics beside it, real values not adjectives).
- Complex: for comparisons, a real table with sourced, specific cells ("5 users included" vs "per-seat from €12"), designed with the same care as the rest of the page.

**Templated pricing.** Three tiers, middle one scaled up or ringed, "Most Popular" flag, identical check-listed features.

- Simple: equal visual weight for all tiers; a plain "Recommended for teams of 5–20" note instead of a badge; features listed as differences only.
- Moderate: lead with a pricing sentence and a calculator or slider tied to the actual pricing variable (seats, sessions, contacts).
- Complex: design pricing around the buying decision: a chooser ("How many deals do you run per quarter?") that lands the visitor on the right plan, with the full matrix behind a link.

**Testimonial cards with avatar + five stars.** Rounded card, circular headshot, name, title, star row, generic quote.

- Simple: cut the stars and the card; set one strong quote as large open text with a name and company.
- Moderate: one detailed quote with a specific result beats six vague ones; pair it with the customer's logo and a link.
- Complex: replace testimonial cards with a short case-study block: the problem, the number that changed, a one-line quote, real product context.

**The grayscale logo marquee.** "Trusted by" followed by six gray logos, sometimes auto-scrolling.

- Simple: static row, four logos maximum, only ones you may actually use.
- Moderate: attach each logo to a fact ("Acme: 4,000 sessions/day") instead of presenting them as wallpaper.
- Complex: if no real logos exist yet, say something true instead (open-source star count, real usage numbers) rather than faking social proof; an honest page is more credible than a templated one.

**FAQ accordion by default.** Chevron accordions with questions nobody asked, existing because the template has a FAQ section.

- Simple: cut it, or keep only questions with non-obvious answers, set as plain headings and text (which also reads better and is better for SEO).
- Complex: fold real objections into the page where they arise (pricing objections at pricing, security questions near the data section).

## 3. Color and effects tells

**The purple default.** Indigo-600 primaries, violet-to-fuchsia gradients, purple glows. LLMs and page builders converge on purple so hard it now signals "AI-made" on sight.

- Simple: pick any deliberate primary that is not indigo/violet, ideally from the brand (a burnt orange, a deep navy with a warm gold), and use grayscale plus that one accent.
- Moderate: build a small palette from the brand color: one accent, one dark, two grays, one background tint. No gradients unless the brand already owns one.
- Complex: develop a color system with meaning (semantic colors for states, a distinct data-viz ramp) so color choices look decided rather than defaulted.

**Gradient headline text.** `background-clip: text` on the key word of the H1.

- Simple: solid color. If one word needs emphasis, italic, weight change, or the accent color.
- Complex: earn emphasis typographically: a contrasting display face for the key phrase, or restructure the headline so the important word is simply last.

**Glow orbs, mesh blobs, glassmorphism.** Blurred colored circles floating behind a dark hero; frosted-glass cards with backdrop-blur; neon shadows.

- Simple: flat background, real contrast, no decorative blur.
- Moderate: if the background needs texture, use something specific: a faint grid, a subtle noise, a pattern derived from the product (a session-replay tool might use a faint event-timeline motif).
- Complex: replace ambient decoration with meaningful imagery: real product UI, a diagram of the architecture, photography with a consistent treatment.

**Shadow and radius uniformity.** rounded-xl/2xl on everything, the same soft shadow-md on everything, hover-lift on everything.

- Simple: pick one radius (often smaller than the default: 4–8px, or 0 for an editorial feel) and use shadows only on elements that float (menus, modals).
- Complex: define an elevation system with two levels maximum, and let borders and background shifts do most separation work.

## 4. Typography tells

**Inter everywhere, tracking-tight bold.** The default variable font, headline at font-bold tracking-tight, body in gray-500. Competent and completely anonymous.

- Simple: change the headline face to something with character that fits the brand (a grotesque with quirks, a serif for editorial credibility, a mono accent for a dev tool) and keep a workhorse for body.
- Moderate: set a real type scale (not the framework's default steps), tighten the measure to 60–75 characters, and use weight and size, not color alone, for hierarchy.
- Complex: full typographic identity: display face, text face, mono for data/code, consistent optical sizing, punctuation details (real quotes, proper spacing) that templates never get right.

**Gray-on-white body text.** Body copy at gray-500/60% opacity because the template dims everything under a headline. Low contrast, low confidence.

- Simple: body at near-black (#1a1a1a-ish) on white; reserve gray for genuinely secondary metadata.

**Interchangeable headline voice.** "Build faster. Ship smarter." headline patterns are a writing tell rendered in 72px. Apply the companion `deslop-writing` skill to all display copy; the two skills should always run together on marketing pages.

## 5. Motion tells

**Fade-in-up on everything.** Every section slides up 20px and fades in on scroll, staggered, identical easing. Plus pulsing "live" dots and infinite logo marquees.

- Simple: remove scroll animations entirely; a static page reads as more confident and loads as faster.
- Moderate: animate at most one or two moments that deserve it (the hero product demo, a chart drawing in) and honor `prefers-reduced-motion`.
- Complex: motion as product demonstration: an interactive or auto-playing sequence showing the actual tool working, which is worth a hundred fade-ins.

## 6. Choosing the right fix for the context

The graded alternatives above are not a menu to maximize. Match the grade of fix to the item's context:

**Weight by surface.** A marketing homepage and a pitch deck justify complex fixes: they exist to differentiate, and templated design directly undermines the message. Internal dashboards, admin tools, and utilitarian docs mostly need the simple fixes: defaults are less damaging where the visitor is captive and the goal is function; there, clarity beats character.

**Weight by audience.** Design-literate audiences (developers, founders, investors, marketers) spot AI tells fastest and discount for them hardest. Developer-tool and B2B SaaS buyers see dozens of AI-built pages weekly; for them, escalate to moderate/complex fixes on anything public. For audiences who do not live on tech Twitter, the simple grade usually clears the bar.

**Weight by claim.** The more a page claims craft, taste, or seniority (an agency, a design tool, a premium product, a personal site), the more a single tell costs. A product that sells "we notice what others miss" cannot ship an icon-grid template.

**One system, not scattered fixes.** Choose two or three signature decisions (typeface, accent color, one distinctive layout device) and apply them everywhere, rather than applying a different clever fix per section. Consistency of deliberate choices is what reads as human; variety of tricks reads as another kind of template.

**Budget honestly.** A simple fix executed consistently beats a complex fix executed halfway. If there is no time or asset budget for custom illustration, do the icon-deletion fix cleanly rather than shipping four mismatched screenshot crops.

**Never sacrifice function.** Accessibility contrast, keyboard behavior, load performance, and information clarity outrank de-slopping. If a fix hurts usability, take the lower grade.

## Revision pass

Run this as a dedicated review after building:

1. Search the code for `border-l`, `border-left`. Rework every decorative left-border callout.
2. Count the icons. Delete every icon that only repeats its neighboring word; check whether the remainder can become product imagery.
3. Find every eyebrow and badge above a headline. Delete, or justify each one individually.
4. Search for `bg-gradient`, `bg-clip-text`, indigo/violet/purple classes, and `backdrop-blur`. Replace with the brand palette and flat surfaces.
5. Count the cards. Un-card at least half; check radii and shadows are one deliberate system.
6. Scan section by section: does the same eyebrow-headline-grid rhythm repeat? Vary alignment, density, and treatment; give the most important section a unique layout.
7. Check the hero against the formula (badge, gradient word, two buttons, glowing screenshot). Replace formula elements with something specific to this product.
8. Verify every number, logo, testimonial, and star rating is real. Cut anything invented.
9. Check typography: is it all Inter/default at default sizes? Is body text gray-500? Fix contrast and pick a deliberate headline face.
10. Remove blanket scroll animations; keep at most two intentional motions; check `prefers-reduced-motion`.
11. Run the cover test: hide the logo and copy. If the page could be any company's, iterate.
12. Run `deslop-writing` on all visible copy, headlines included.

## Calibration

These are defaults, not laws. Every catalogued element exists because it sometimes works: a left border is fine in genuinely doc-style content, an icon grid can be right for a category-scanning use case, and centered heroes converted long before LLMs existed. The reason to avoid them is frequency: AI tools deploy them so uniformly that they now signal "nobody designed this" regardless of individual merit.

Two cautions:

Do not over-correct into brutalist affectation. Stripping every convention to prove humanity produces its own template, and an unusable page is worse than a generic one. Conventions users rely on (nav placement, button affordances, form patterns) stay.

Do not treat surface fixes as the whole job. The deep tell is decoration without content: a page of adjectives, icons, and invented stats reads as hollow even with a bespoke typeface. Fix the substance first: show the product, use real numbers, name real customers, make one specific argument. Pages with real content and a few deliberate visual decisions rarely read as AI, whatever components they use.

## Sources and pairing

Patterns drawn from designer and frontend community documentation of v0/Lovable/Bolt/ChatGPT/Claude output conventions, shadcn/Tailwind default fingerprints, and landing-page teardown commentary current as of mid-2026. This skill is the visual companion to `deslop-writing`; run both on any public-facing page, since copy tells and design tells almost always co-occur.
