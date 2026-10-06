# Writing without AI tells

## What this is for

LLM prose has a recognizable signature. Editors, Wikipedia's AI Cleanup project, and detection tools now catalogue it in detail, and ordinary readers increasingly react to it with irritation even when they cannot name what they are seeing. This skill lists the attested patterns and gives the replacement for each, so that writing reads as the work of a specific person with a point of view rather than the statistical average of the internet.

Use it two ways. While drafting, keep the patterns in mind so they never enter the text. After drafting, run the revision pass at the end of this document as a dedicated edit.

## The root cause (read this first)

Almost every tell below comes from one of two underlying habits. Fixing the surface phrase without fixing the habit just produces a new variant the reader will still recognize, so internalize these rather than pattern-matching the examples.

**One: manufacturing significance the content has not earned.** The model has learned that signaling importance reads as useful, so it tells the reader something matters instead of showing why, inflates ordinary stakes to world-historical ones, and attaches grand meaning to mundane facts. The fix is almost always to state the concrete thing and delete the significance claim. If the thing matters, the specifics will carry it. If it does not, no amount of framing will save it.

**Two: reaching for a fancier construction than plain statement.** The model's repetition penalty and its training on formal, edited corpora push it away from simple verbs and direct sentences toward ornate vocabulary, contrast framing, and rhetorical scaffolding that sound sophisticated without being sophisticated. The fix is to prefer the plain verb, the direct claim, and the shorter path.

A useful test from a Reddit editor, paraphrased: AI emphasizes everything because it cannot tell what is important. Wherever you see ordinary things that do not need emphasis getting emphasized, that is the tell.

## Fast checklist

The highest-frequency offenders, for a quick scan:

1. Em dashes used for drama or asides. Remove them.
2. Negative parallelism: "It's not X, it's Y." Remove it.
3. The rule of three (lists of three adjectives, phrases, or clauses), especially repeated.
4. Filler transitions: Moreover, Furthermore, Additionally, It's worth noting, In conclusion.
5. Vocabulary fingerprints: delve, leverage, robust, tapestry, landscape, underscore, pivotal, seamless, navigate, foster, harness, realm.
6. Trailing "-ing" clauses that add significance: "...highlighting the importance of..."
7. Fragments as standalone sentences for manufactured punch.
8. Bold-lead-in bullet lists ("**Thing:** description").
9. Stakes inflation and puffery: "this will fundamentally reshape everything."
10. Hollow opener or closer that restates without adding.

## 1. Vocabulary fingerprints

Certain words appear in LLM output at many times their natural rate. None is forbidden in isolation, but each should earn its place, and a cluster of them is a reliable signal. Prefer the plain alternative.

| Avoid / use sparingly | Prefer |
|---|---|
| delve into, dive into, explore (as filler) | look at, examine, or just say the thing |
| leverage (verb), utilize | use |
| harness, unlock, unleash | use, enable, allow |
| robust, powerful, comprehensive | specific capability, or cut |
| seamless, effortless, frictionless | name the actual benefit |
| navigate (the landscape/complexities of) | rewrite the sentence |
| foster, cultivate | build, create, support, encourage |
| underscore, highlight, emphasize (as the verb of a sentence) | show, or cut |
| pivotal, crucial, vital, paramount, key | important only if true, else cut |
| tapestry, landscape, realm, ecosystem, paradigm, synergy | field, area, world, or the specific noun |
| testament to, beacon of, cornerstone of | cut; state the fact |
| myriad, plethora, vast array | many, or a number |
| multifaceted, nuanced, intricate, complex | describe the actual complication |
| meticulous, vibrant, bustling, rich (heritage/history) | a concrete detail instead |
| game-changer, revolutionary, cutting-edge, state-of-the-art | what it actually does |
| resonate, elevate, embark, journey | plain verb or noun |

**The "serves as" dodge.** The model avoids the plain copula and reaches for "serves as," "stands as," "represents," or "marks." Use *is* or *are*.

- Avoid: "The dashboard serves as a central hub for all your data."
- Prefer: "The dashboard shows all your data in one place."

**Magic adverbs.** "Quietly," "deeply," "fundamentally," "remarkably," "arguably" get sprinkled in to lend weight. Delete them and see if the sentence loses anything. Usually it does not.

## 2. Sentence-shape tells

These survive paraphrase, so they matter more than vocabulary. The model returns to the same handful of shapes across paragraphs, and the repetition is what reads as machine-made.

**Negative parallelism (the single most recognized tell).** "It's not X, it's Y." Also its variants: "not because X, but because Y," "X, not Y," and the cross-sentence version "The question isn't X. The question is Y." Before LLMs, people did not write this way at scale. State the positive claim directly.

- Avoid: "This isn't a feature. It's a philosophy."
- Avoid: "We're not building software, we're building a movement."
- Prefer: "The software enforces one rule: every change is logged." (Say what it is. Drop the contrast.)

**"Not X. Not Y. Just Z."** The dramatic countdown that negates two things before revealing the point.

- Avoid: "Not a tweak. Not a patch. A rebuild."
- Prefer: "We rebuilt it." Then explain.

**Rhetorical question answered immediately.** "The result? Devastating." The model poses a question nobody asked for a beat of drama.

- Avoid: "The catch? It only works online."
- Prefer: "It only works online."

**Trailing participle pseudo-analysis.** A main clause followed by a comma and an "-ing" phrase that asserts significance, legacy, or broader meaning. Instruction-tuned models use this at two to five times the human rate.

- Avoid: "The team shipped the API in March, marking a pivotal moment in the company's evolution."
- Prefer: "The team shipped the API in March." If the consequence matters, write a real sentence about the consequence.

**False ranges.** "From X to Y" where X and Y are not endpoints of any real scale and nothing meaningful sits between them.

- Avoid: "From innovation to transformation, we cover it all."
- Prefer: name the two things plainly, or list what you actually mean.

**Anaphora abuse.** Repeating the same sentence opening three or more times in quick succession ("They assume... They assume... They assume..."). One repetition can land. A stack of them is a tell.

**Tricolon / rule of three.** Grouping ideas in threes: three adjectives, three short phrases, three parallel clauses. A single tricolon is fine. Two or three in the same piece is a pattern-recognition failure. Vary the count. Use two items, or four, or a number.

- Avoid: "fast, reliable, and secure"
- Avoid: "Products solve problems; platforms create worlds. Products scale linearly; platforms scale exponentially. Products..."
- Prefer: cut to the one claim you can defend, with evidence.

## 3. Paragraph and rhythm tells

**Fragments as paragraphs.** Very short sentences or fragments set alone for manufactured emphasis. "Openly. In a book. As a priest." RLHF pushed models toward one-thought-per-line readability, but no one drafts this way, and at volume it reads as inhuman. Write in complete sentences. Earn a fragment rarely, if ever.

**Listicle in a trench coat.** A list disguised as prose by opening each paragraph with "The first... The second... The third..." Often what the model does after being told to stop using bullet lists. If the content is genuinely a list, decide whether a real list or real connected prose serves better, and commit to one.

**Formulaic paragraph shape.** Every paragraph built identically: topic sentence, one supporting point, summary sentence. Real writing varies paragraph length and structure. Let some paragraphs be one sentence of argument and others a developed case.

## 4. Tone and stance tells

**Stakes inflation and puffery.** Everything is the most important development ever. A post about pricing becomes a meditation on the future of civilization. Newer models avoid blatant superlatives like "the best" but still over-signal importance subtly. State what the thing does and let the reader judge its size.

- Avoid: "This will fundamentally reshape how we think about everything."
- Prefer: "This cuts the review cycle from five days to one." (A specific number beats any grand claim.)

**Explaining importance instead of behavior.** Especially in documentation. The text tells you something is significant or powerful rather than telling you what it does or how it works. Replace every "this is a powerful feature that" with the behavior itself.

**False suspense.** "Here's the kicker." "Here's the thing." "Here's where it gets interesting." "Here's what most people miss." These promise a revelation and then deliver an ordinary point. Cut the runway and state the point.

**Pedagogical voice.** "Let's break this down." "Let's unpack this." "Let's dive in." The teacher-to-student register, applied even to expert readers. Just make the point.

**Patronizing analogy.** "Think of it as a Swiss Army knife for X." "It's like a highway system for data." The reflexive metaphor, often less clear than the thing it explains. Use an analogy only when it genuinely clarifies, and then make it specific to the domain.

**"Imagine a world where."** The futurism invitation, followed by a list of wonderful things that follow if the reader accepts the premise. Make the argument on its merits instead.

**Over-hedging.** Every claim softened: "may," "might," "could," "generally," "typically," "tends to," "arguably," "to some extent," "in many cases." Newer models hedge so reflexively that nothing has a spine. A useful tell, per ChatGPT itself: every claim has a counterpoint and no strong opinion stands without a softener. Take positions. Where a real caveat exists, state it once, specifically. Delete the rest.

**Sycophancy and flattery openers.** "Great question!" "That's a fascinating topic." Also the reflex of calling subjects "fascinating," "captivating," "rich," or "vibrant." Skip the warm-up and start with substance.

**False vulnerability.** Performative self-awareness that costs nothing: "Let me be honest with you," "I'll admit I'm biased here," "this isn't a rant, it's a diagnosis." Real candor is specific and uncomfortable. Manufactured candor is polished and risk-free. Cut it.

**Asserting obviousness.** "The truth is simple." "History is unambiguous on this point." "The reality is clear." If you have to announce that your point is obvious, it usually is not. Prove it instead, or drop the claim.

**Vague attributions.** "Experts argue," "industry reports suggest," "observers have noted," "several publications have cited." Unnamed authorities, often with inflated counts (one person's view presented as consensus, "several" meaning two). Name the source or drop the claim.

**Invented concept labels.** Coining authoritative-sounding compounds and using them as if established: "the supervision paradox," "the acceleration trap," "workload creep." They name a thing to skip arguing for it. Several in one piece is a strong slop signal. Make the argument; do not brand it.

## 5. Transitions and connectors

LLMs pad with logical connectors that signal structure without adding content. Heavy use of overt transitions is one of the oldest and most reliable signals.

Avoid as filler: Moreover, Furthermore, Additionally, In addition, It's worth noting that, It's important to note, It bears mentioning, Importantly, Notably, Interestingly, That being said, As we can see, Ultimately, In conclusion, In summary, Overall, At the end of the day, When it comes to, In today's fast-paced world, In an era of, In the realm of.

The fix is usually deletion. Well-ordered sentences connect through their content and rarely need a signpost. Where a real logical turn exists, a plain "but," "so," "still," or "because" carries it. Vary connectors and use them only when the logic genuinely shifts.

## 6. Formatting tells

**Em dashes.** Compulsive use for dramatic pauses, asides, and pivots is among the most discussed tells. The em dash is legitimate in human writing, so its presence alone proves nothing, but LLM output overuses it badly. Default: do not use em dashes. Use a period, a comma, parentheses, or a colon, whichever the sentence actually wants.

**Bold-lead-in lists.** The signature LLM list item: a bolded phrase, a colon, then a description. "**Scalability:** the system grows with you." Almost nobody writes this by hand. Use plain lists, or fold the points into prose, and do not open every item with a bolded label.

**Rule-of-three headers and punchy slogans.** "No hardware. No fees. Just growth." Effective once. Used in every section of a page, it reads as templated. Vary it.

**Over-bolding.** Bolding phrases throughout for emphasis in a way that emphasizes everything and therefore nothing. Reserve bold for genuine signposting, and use little of it.

**Emoji as section markers and decorative bullets.** A common chatbot habit (the 🚀, the ✅, the 🤔 before "Let's delve deeper"). Avoid unless the medium and audience clearly call for it.

**Title-case headings and rigidly uniform structure.** Headings styled Like This Throughout, sections of near-identical length, a list dropped into the middle of otherwise flowing prose. Let structure follow content.

**Other surface tells when writing for a non-US audience.** LLMs default to American spelling and the Oxford comma. If the house style is British or Dutch-English, switch "-ize" to "-ise," restore the "u" in "colour" and "behaviour," and match the local serial-comma convention. (This is a giveaway only when it clashes with the intended register; it is not wrong in itself.)

## 7. Openers and closers

**Openers.** Avoid the throat-clearing introduction that defines the obvious or sets a "fast-paced world" scene. Open on the actual claim, the specific detail, or the tension that earns the reader's attention.

**Closers.** Avoid the conclusion that restates everything already said, especially one that starts with "In conclusion," "In summary," "Overall," or "Ultimately," and resolves a little too neatly. End on the strongest concrete point, a real implication, or simply stop. A piece does not need a bow on it.

## House defaults (hard rules)

These are stricter than "use sparingly." Treat them as defaults to be overridden only with a specific reason:

- **No em dashes** anywhere in copy.
- **No antithesis / negative parallelism** ("not X, but Y" and all its variants).
- **No rhetorical fragments** used for punch.
- **Thesis first.** Lead with the claim, then support it. Do not bury the point under setup.
- **Specific numbers over vague claims.** "Cut onboarding from 6 weeks to 9 days," not "dramatically faster onboarding."
- **Direct feedback without diplomatic softening.** Say the real thing plainly. Do not cushion criticism in praise sandwiches or hedge it into vagueness.

## Revision pass

Run this as a dedicated edit after drafting:

1. Search the text for em dashes. Remove each one and repunctuate.
2. Search for "not just," "isn't," "rather than," and "instead of." Check each for negative parallelism and rewrite as a direct positive claim.
3. Search for the connector list in section 5 (Moreover, Furthermore, It's worth noting, In conclusion, and so on). Delete or downgrade each.
4. Scan for the vocabulary in section 1. Replace clusters of fingerprint words with plain language.
5. Find every "-ing" clause hanging off the end of a sentence. Cut the ones that only assert significance.
6. Count the tricolons and the lists of three. Keep at most one. Vary the rest.
7. Find standalone fragments and short one-line paragraphs used for drama. Rejoin them into full sentences.
8. Find every claim of importance ("crucial," "pivotal," "fundamentally," "reshape," "powerful"). For each, either replace it with the concrete specific that proves it, or delete it.
9. Find hedges ("may," "might," "tends to," "arguably," "generally"). Take a position or keep one real caveat.
10. Reread the opener and closer. Cut throat-clearing and any conclusion that only restates.
11. Read the whole thing aloud. Where the rhythm is monotonously even, vary sentence length on purpose.

## Calibration

These are defaults, not absolute laws of writing. Skilled human writers use em dashes, tricolons, and the occasional sharp fragment to good effect. The reason to avoid them here is that LLMs overuse them so heavily that they now read as machine output regardless of how well they are deployed, and a clean default is the safer position.

Two cautions:

Do not over-correct into stilted prose. Stripping every dash and contrast while leaving the writing lifeless misses the point. The aim is a clear human voice, not a sanitized one.

Do not treat the surface fixes as the whole job. The deeper tells (manufactured significance, hollow structure, polished shallowness) survive paraphrase. Removing the word "delve" from a paragraph that still says nothing leaves a paragraph that still says nothing. Fix the substance first: have a real point, ground it in specifics, take a position. The surface edits then matter far less, because writing with genuine content and a genuine point of view rarely reads as AI in the first place.

## Sources

Drawn from Wikipedia's *Signs of AI writing* (WikiProject AI Cleanup), Grammarly's research on common AI words, the tropes.fyi catalogue, Pangram Labs' detection guide, NPR's reporting on the Wikipedia guide, and several editor field guides current as of mid-2026. The specific tells are empirically attested across these sources; the framing and defaults are tuned for clean, direct B2B and technical writing.
