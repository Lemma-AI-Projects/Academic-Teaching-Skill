# 09 Research Log

## What We Searched, Why, What We Found

This log records the research process for Phase 1. It documents search decisions, findings, excluded directions, changed conclusions, and unanswered questions.

---

## Session 1: Multimedia Learning & Cognitive Load

**What was searched:** Richard Mayer's CTML, John Sweller's CLT, multimedia learning principles, cognitive load types, empirical studies on slide design.

**Why:** These are the foundational cognitive science theories that constrain all slide design.

**What was found:**
- 12+ evidence-based principles with effect sizes (temporal contiguity d=1.30 is strongest)
- 8 controversies: germane load debate, measurement challenges, expertise reversal, declining effect sizes
- Strong meta-analytic evidence from 6 meta-analyses
- Slide-specific applications documented in Kosslyn (2012) and Poz et al. (2022)

**What was excluded:**
- Neuroscience of perception (too low-level for slide design decisions)
- Embodied cognition (emerging but not yet applicable)

**Changed conclusions:**
- Initially assumed all 12 principles apply equally to slides. Reality: most were validated for narration+slides, not standalone slides. This is a critical gap.

---

## Session 2: Academic Presentation Design

**What was searched:** Academic presentation practices, scientific communication, lecture design, expert vs. novice presenters, role of narrative.

**Why:** To understand how academics actually design presentations and what makes them effective.

**What was found:**
- 84.4% CTML violation rate in medical education
- Assertion-evidence approach has empirical support
- Expert presenters are more audience-oriented
- Narrative improves persuasion and recall
- Key books: Alley (2013), Kosslyn (2012), Duarte (2008), Reynolds (2019)

**What was excluded:**
- Business presentation research (different context, different goals)
- Public speaking research (delivery, not slide design)

**Changed conclusions:**
- Initially focused on "what makes good slides." Realized the question should be "why do bad slides persist despite knowledge of what works?" — the gap between knowledge and practice is the real problem.

---

## Session 3: Information Visualization & Visual Explanation

**What was searched:** Tufte's principles, Bertin's visual variables, misleading visualizations, decoration vs. explanation, visual literacy.

**Why:** To understand how data and ideas should be represented visually on slides.

**What was found:**
- Data-ink ratio, chartjunk, small multiples are well-established principles
- Line graphs with manipulated x-axes are most deceptive (OR ≈ 15.4)
- Decorative elements improve memorability but decrease precision
- Visual literacy is lacking even in "digital natives"
- Diagrams reduce computational load in problem-solving

**What was excluded:**
- 3D visualization (rarely used in slide presentations)
- Virtual reality visualization (not applicable to slides)

**Changed conclusions:**
- Initially assumed Tufte's principles are universally accepted. Reality: some are debated (e.g., whether all decoration is harmful). The "functional art" perspective (Cairo) offers a more nuanced view.

---

## Session 4: Instructional Design

**What was searched:** Gagné, Merrill, Biggs, Wiggins & McTighe, Keller, Bloom, PBL, worked examples.

**Why:** To understand theories for designing effective learning experiences — the "teaching" dimension.

**What was found:**
- 9 events of instruction with strong meta-analytic support (SMD=1.55)
- 5 first principles of instruction with 9x improvement in mastery
- Backward design improves achievement and retention
- ARCS model improves motivation (27 studies)
- Massive gap between instructional design theory and actual presentation practice

**What was excluded:**
- Constructivism debates (philosophical, not directly applicable)
- Learning analytics (measurement, not design)

**Changed conclusions:**
- Initially thought instructional design was "separate" from presentation design. Realized they are deeply connected — the question is whether slides can serve as instructional events.

---

## Session 5: Existing Presentation Software & AI Systems

**What was searched:** PowerPoint, Keynote, Google Slides, Beamer, Slidev, Marp, Reveal.js, Gamma, Beautiful.ai, Canva AI, Copilot, PPTAgent, Paper2Slides, Auto-Slides, SlideGen, GDP, PaperX.

**Why:** To understand what tools exist and what problems they solve.

**What was found:**
- Five distinct problems are being conflated: content generation, presentation generation, visual design, teaching design, rendering
- No system combines academic citations + AI generation + beautiful design + teaching awareness
- PPTX export is a critical unsolved problem for web-native tools
- Teaching design is almost entirely absent from automated systems
- The frontier is document-to-slides with source fidelity

**What was excluded:**
- Video presentation tools (not slide-based)
- Whiteboard tools (different medium)
- Specific pricing comparisons (not relevant to research)

**Changed conclusions:**
- Initially assumed "AI presentation generation" was one problem. Realized it's at least 5 separate problems, each with different solutions.

---

## Session 6: Case Studies

**What was searched:** Patrick Winston (MIT), Susan McConnell (Stanford), Hans Rosling (Gapminder), Terence Tao (ICM 2026), Demis Hassabis (Nobel 2024), David Baker (Nobel 2024), Doris Tsao (Caltech).

**Why:** To observe what excellent academic presentations actually look like.

**What was found:**
- Best presenters use fewer slides
- "Home image" concept creates coherence
- Narrative structure improves clarity even in technical contexts
- Animation + narration > static + narration
- Concrete framing > abstract framing
- Passion is visible in design

**What was excluded:**
- Business presentations (different context)
- TED talks by non-scientists (different goals)
- Poor presentations (documented separately in Failure Map)

**Changed conclusions:**
- Initially wanted to extract "best practices" from cases. Realized this is premature — the sample is too small and non-random. Better to accumulate observations before theorizing.

---

## Session 7: Failure Cases

**What was searched:** Boeing/NASA Columbia slides, medical education violations, cognitive overload examples, misleading visualizations, "Chicken Chicken Chicken" satire, AI hallucination risks.

**Why:** To understand how and why academic presentations fail.

**What was found:**
- 10 distinct failure modes documented
- Cognitive overload is the most prevalent (84.4% violation rate)
- Misleading visualizations have measurable deceptive impact (OR up to 15.4)
- Format-over-substance blindness is a real phenomenon
- AI hallucinations are an emerging concern
- The system should be designed to systematically avoid failures, not just add templates

**What was excluded:**
- Delivery failures (voice, body language — not slide design)
- Technology failures (projector, connectivity — not design)
- Content failures (wrong data, bad methodology — not presentation)

**Changed conclusions:**
- Initially focused on "what makes good slides." Shifted to "what makes slides fail" — because avoiding failures may be more tractable than achieving excellence.

---

## Session 8: Concept Glossary

**What was searched:** Definitions and distinctions for: presentation, lecture, teaching, explanation, communication, visualization, visual explanation, narrative, argument, slide, deck, learning objective, cognitive load, instructional design, slide design, presentation design, educational technology.

**Why:** These terms are easily confused and used differently across fields.

**What was found:**
- 18 terms with careful distinction
- Key ambiguities documented
- Cross-field differences identified

**Changed conclusions:**
- Initially assumed "presentation design" and "slide design" were the same. Realized they operate at different levels — presentation design is holistic, slide design is component-level.

---

## Session 9: Evidence Map

**What was searched:** Classification of all claims into FACT, OBSERVATION, INTERPRETATION, HYPOTHESIS, OPEN QUESTION.

**Why:** To ensure intellectual honesty and traceability.

**What was found:**
- Strong FACT base from cognitive science and multimedia learning
- Limited OBSERVATION base (small, non-random case studies)
- Several INTERPRETATIONS that could become hypotheses
- 13 HYPOTHESES that need testing
- 10 OPEN QUESTIONS that remain genuinely unanswered

**Changed conclusions:**
- Initially had more "facts" than justified. Reclassified several claims as INTERPRETATIONS when we realized the evidence was weaker than assumed.

---

## Directions Explicitly Excluded

1. **Business presentation design** — Different goals (persuasion/sales vs. teaching/communication)
2. **Public speaking/delivery** — Important but outside slide design scope
3. **Video/animation production** — Different medium
4. **Virtual reality/augmented reality** — Not slide-based
5. **Assessment design** — Related but separate field
6. **Learning management systems** — Infrastructure, not content
7. **Specific programming languages/frameworks** — Phase 2 decision
8. **Business model/market analysis** — Phase 2 decision

---

## Questions Still Unanswerable

1. What is the optimal ratio of text to visuals on academic slides? (No systematic research)
2. How many slides per minute is optimal? (Rule of thumb exists, no empirical basis)
3. Should slides be designed for printing or screen viewing? (Context-dependent, no universal answer)
4. How should equations be presented on slides? (Mathematical notation research exists but not in presentation context)
5. What is the role of handouts vs. slides? (Different media, different purposes)
