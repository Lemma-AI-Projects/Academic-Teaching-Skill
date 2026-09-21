# Postmortem: First Working Prototype

## What We Built

Two versions of a 10-slide deck about Partial Differential Equations:
- **Version A:** Standard AI approach — title, outline, definition, classification table, solution methods, summary, references. 35 bullet points. Text-heavy. Topic-subtopic structure.
- **Version B:** Foundation-informed — frame, context bridge, key idea, three equations, heat demonstration, wave demonstration, classification comparison, boundary conditions, separation of variables process, synthesis. 0 bullet points. Visual-heavy. Claim-evidence structure with speaker notes.

Both generated from the same source material. Same topic. Same depth.

---

## Question 1: What Did We Originally Think Was Most Important?

We thought the most important thing was **the visual design** — making slides look good, having proper layout, clean typography, consistent styling.

We also thought **content completeness** was critical — covering all the topics in the source material.

And we thought **classification and definitions** were the core of teaching PDEs.

---

## Question 2: What Actually Mattered?

After generating both versions, what actually mattered was:

### 1. The STRUCTURE of the deck, not the content
Version A covers the same content as Version B. But the structure is completely different. Version A is a list of topics. Version B is a teaching sequence. The structure determines whether the learner can follow the argument.

### 2. The TRANSITIONS between slides, not the slides themselves
Version A's transitions are: "Here's the outline." "Here's the definition." "Here's why it matters." Version B's transitions are: "You know ODEs — here's how PDEs are different." "Here's the equation — now let me show you what it DOES." The transitions create a narrative. Without them, slides are isolated information cards.

### 3. The SPEAKER NOTES, not the slide text
Version A has no speaker notes. Version B has detailed notes that don't repeat the slide text but explain the TEACHING intention. The speaker notes reveal whether the slide actually serves a pedagogical purpose. Without them, we can't tell if a slide is teaching or just displaying.

### 4. Whether each slide ANSWERS A QUESTION, not whether it COVERS A TOPIC
Version A's slides cover topics. Version B's slides answer questions: "Why should I care?" "How is this different from what I know?" "What does this equation actually DO?" "Why does classification matter?" The question-driven structure is fundamentally different from the topic-driven structure.

---

## Question 3: What Did We Think Was Important But Wasn't?

### 1. Completeness
Version A tries to cover everything: definition, classification, boundary conditions, solution methods, numerical methods, references. Version B deliberately omits numerical methods, most of boundary conditions, and references. But Version B teaches better. **Completeness is not the same as teaching.**

### 2. The outline slide
Version A has an outline slide. Version B doesn't. The outline is a crutch for the presenter, not a help for the learner. In Version B, the flow is clear enough that an outline is unnecessary. **The outline is a symptom of topic-driven design, not evidence of good teaching.**

### 3. The references slide
Version A ends with references. Version B doesn't. References are important for academic integrity but don't contribute to understanding. **References serve the source, not the learner.**

### 4. Visual polish
Both versions use basic styling. Neither is "beautiful." But Version B's visual choices (time sequence diagrams, comparison layouts, process flow) serve specific teaching functions. Version A's visual choices (tables, bullet lists) are default formatting, not visual explanation. **Visual design that doesn't serve teaching is decoration.**

---

## Question 4: What Problems Were Only Visible After Rendering?

### 1. The SVG diagrams in Version B are fragile
The hand-coded SVG time sequences (heat diffusion, wave propagation) work but are brittle. Small changes to viewBox or coordinates could break them. In a real system, these would need to be generated programmatically, not hand-coded.

### 2. Version A's bullet density is overwhelming
When rendered, Version A's 35 bullet points across 10 slides create visual walls of text. The cognitive load is immediately apparent in a way that isn't obvious from the source code. **You have to see the rendered deck to feel the overload.**

### 3. Version B's small fonts are a problem
Several labels in Version B use 12-13px fonts. These are fine on a monitor but would be unreadable in projection. **Font size constraints are only obvious when you imagine the delivery context.**

### 4. The comparison layout in Slide 2 (Version B) is tight
The ODE vs. PDE comparison requires careful reading. At 960px width, the two columns are readable but cramped. In a real presentation, this might need to be two slides or use larger text.

### 5. The process flow in Slide 9 (Version B) may not render well at all sizes
The five-step process flow with arrows uses flexbox. At smaller viewport sizes, the steps could wrap awkwardly. **Responsive design matters even for presentations.**

---

## Question 5: What Should Change in the Next Round?

### 1. The Renderer needs real constraints
Version B's visual structures (time sequences, comparison layouts, process flows) are good but hand-coded. A real Renderer needs to generate these from the Teaching Plan, not from HTML templates. The Renderer should accept a structured description and produce visual output.

### 2. Font sizes need minimum constraints
12-13px is too small for projection. The Renderer should enforce minimum font sizes (16px for body text, 24px for labels).

### 3. The teaching grammar needs testing
We proposed Frame → Context → Key Idea → Evidence → Distinguish → Explain → Demonstrate → Synthesize. This worked for PDEs. But does it work for other topics? We need to test with at least 3 different topics before generalizing.

### 4. The Intelligence layer needs to be separated from the Renderer
In this prototype, Intelligence and Renderer are mixed in the same HTML file. In a real system, the Intelligence layer should output a structured Teaching Plan (JSON or similar), and the Renderer should consume it. This separation is essential for iterative improvement.

### 5. Speaker notes generation needs its own model
The speaker notes in Version B are good but were generated as part of the same process as the slides. In a real system, speaker notes should be generated by a separate process that knows the teaching intention and can explain the pedagogical reasoning.

---

## Question 6: What Do We Still Not Know?

### 1. Whether Version B actually teaches better
We have a hypothesis (Version B teaches better because it follows teaching principles). We have no evidence. We need human evaluation to confirm or refute this. The feedback template is ready but hasn't been used yet.

### 2. Whether the teaching grammar generalizes
We tested it on PDEs (a mathematical topic with clear structure). Would it work for:
- A biology lecture (more descriptive, less formal)?
- A philosophy seminar (more argumentative, less visual)?
- A history presentation (more narrative, less analytical)?

### 3. Whether the visual structures actually reduce cognitive load
We believe the time sequence diagrams help learners understand diffusion and propagation. But we haven't measured this. The visual structures might look good but not actually improve understanding.

### 4. Whether the claim-evidence structure is detectable
We manually created claims and evidence for each slide. Can an LLM reliably extract these from source material? This is the Critical Unknown #1 from FOUNDATION.md, and this prototype doesn't answer it.

### 5. Whether the intermediate representation is right
We went directly from source to HTML. We didn't use an intermediate representation (Teaching Plan as JSON). The prototype works but doesn't test whether the IR is sufficient for the Renderer.

---

## Key Observations

### The most surprising finding
**The biggest difference between Version A and Version B is not visual. It's structural.** Version A covers the same content. But the structure — the order, the transitions, the teaching moves — is completely different. This suggests that the Intelligence layer (teaching decisions) matters more than the Renderer (visual decisions).

### What we got right
- The claim-evidence structure works. Each slide has a clear purpose.
- The teaching sequence works. The flow from Frame to Synthesize is coherent.
- The speaker notes are valuable. They reveal whether a slide is actually teaching.
- The visual structures (time sequences, comparisons, process flows) serve specific functions.

### What we got wrong
- We underestimated the difficulty of generating SVG diagrams programmatically.
- We overestimated how much content we could fit on a single slide.
- We assumed font size wouldn't matter at prototype stage. It does.
- We thought completeness was important. It's not.

### The prototype's real value
This prototype answered one question: **Is the Foundation worth pursuing?**

The answer is: **Yes, but with caveats.**

The teaching grammar, claim-evidence structure, and visual mapping principles produced a measurably different deck. Whether it's BETTER is unknown. But it's different in ways that align with our theory. That's enough to continue.

---

## Next Steps

1. **Get human feedback** on both versions using the feedback template
2. **Test the teaching grammar** on 2 more topics (different domains)
3. **Separate Intelligence from Renderer** in code
4. **Build a minimal Renderer** that takes a Teaching Plan (JSON) and produces HTML
5. **Test LLM-based claim extraction** from source material

The prototype showed us what we're building toward. Now we need to validate whether it works.
