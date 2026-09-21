# FOUNDATION.md

## Academic Teaching Skill — Phase 2: Foundation Synthesis

**Status:** Minimal working theory established. No architecture. No product. No code.

**Success criterion for this phase:** We have a theory small enough to test and honest enough to be wrong.

---

## 1. Research Audit

### What Is Actually Established (FACT)

These claims have strong empirical support. We can build on them.

| # | Claim | Source | Evidence | Caveat |
|---|-------|--------|----------|--------|
| F1 | Working memory is limited (~7±2 items, <30s active retention) | Miller (1956) | Hundreds of replications | Exact limit varies by task |
| F2 | Dual-channel processing (auditory + visual) | Paivio (1986); Mayer (2001) | Strong | Assumption, not proven mechanism |
| F3 | Extraneous cognitive load from poor design impairs learning | Sweller (1988) | Hundreds of RCTs | Measurement remains difficult |
| F4 | Words + pictures > words alone (d=1.35) | Mayer (2001) | Meta-analytic | Validated for narration+slides, not standalone |
| F5 | Spatial contiguity improves learning (d=0.82) | Mayer (2001) | Meta-analytic | Same caveat as F4 |
| F6 | Coherence principle improves learning (d=0.86) | Mayer (2001) | Meta-analytic | Same caveat as F4 |
| F7 | Most academic slides violate these principles (84.4%) | Le Blanc & Cooper (2026) | Primary data | Medical education only |
| F8 | Not a single PowerPoint in 100+ sample was violation-free | Kosslyn (2012) | Empirical | Focused on violations, not success |
| F9 | Worked examples help novices reduce extraneous load | Sweller (1988) | RCTs | Expertise reversal: can hinder experts |
| F10 | Diagrams reduce search and recognition costs | Larkin & Simon (1987) | Computational models | Problem-solving diagrams, not slides |

### What Is Observed But Not Validated (OBSERVATION)

These patterns appear in real cases but are not systematically confirmed.

| # | Observation | Source | Strength | Risk |
|---|-------------|--------|----------|------|
| O1 | Best presenters use fewer slides | Winston, Rosling (N=2) | Weak | Small sample, survivorship bias |
| O2 | "Home image" creates coherence | McConnell (N=1) | Weak | Single case |
| O3 | Narrative structure improves clarity | Multiple cases | Correlational | Confound: better presenters may be better narrators |
| O4 | Concrete framing > abstract framing | Baker, Rosling (N=2) | Weak | Small sample |
| O5 | Students expect text-heavy slides | Schmaltz & Enström (2014) | Survey | Expectation ≠ effectiveness |
| O6 | No AI tool handles citations well | Feature audit | Descriptive | Feature audit, not user study |
| O7 | Teaching design is absent from automated systems | Feature audit | Descriptive | May be emerging (Auto-Slides) |

### What Is Reasonable But Unproven (INTERPRETATION)

| # | Interpretation | Basis | Confidence |
|---|----------------|-------|------------|
| I1 | Slides should teach, not just inform | ID theory + practice gap | High — but "teach" is not operationally defined |
| I2 | Visual design ≠ teaching design | Analysis of tools | High — but boundary is unclear |
| I3 | Assertion-evidence is better than topic-subtopic | Alley (2013) + empirical | Medium — single study comparison |
| I4 | Every visual element must serve a communicative purpose | Tufte (1983) | High — but "communicative" is vague |
| I5 | Expertise level must determine design | Expertise reversal effect | High — but how to determine expertise automatically? |

### What Is Untested (HYPOTHESIS)

| # | Hypothesis | What would verify it |
|---|------------|---------------------|
| H1 | AI can generate slides that teach (not just inform) | Controlled study: AI vs. human slides → learning outcomes |
| H2 | Teaching-aware generation > content-only generation | A/B test with real students |
| H3 | Mayer's principles apply to standalone slides (without narration) | Empirical study comparing with/without narration |
| H4 | Multi-agent architecture > single model for this task | Comparison study |
| H5 | Visual-in-the-loop feedback improves quality | A/B test with/without VLM review |

### What Was Deleted (No Longer Treated as Supported)

| Previous Claim | Why Deleted |
|----------------|-------------|
| "Germane load" is a real third type | Debate unresolved; may be redundant with intrinsic load |
| Animation has clear benefit over static | Effect sizes small (d=0.23); context-dependent |
| Best presentations have narrative | Correlational; confounded with presenter skill |
| Minimalist design is universally better | Expertise reversal + student expectations suggest otherwise |

---

## 2. Core Questions

From the entire research, these are the questions most worth solving. Not "important" — worth solving because they determine whether this project is viable.

### CQ1: Can we define "teaching" in a way that an AI system can execute?

**Why this is the question:** Everything else is downstream. If we cannot operationally define what it means for a slide to "teach" (not just "inform"), we cannot build a system that does it. Current instructional design theories describe principles but not procedures. The gap between "slides should teach" (interpretation I1) and "here is how to compute a teaching sequence" is enormous.

**What we know:** Gagné's 9 events, Merrill's 5 principles, backward design — all describe instructional sequence at a high level. None specifies how to translate a document into such a sequence computationally.

**What we don't know:** Whether an LLM can reliably decompose a source document into pedagogically ordered units. Whether the "teaching" that happens in a 50-minute lecture can happen in a slide deck. Whether teaching design and content selection are separable tasks.

**This question determines:** Whether the project is "AI-assisted slide design" (feasible now) or "AI teaching design" (requires fundamental breakthrough).

---

### CQ2: What is the right intermediate representation?

**Why this is the question:** Every existing system has a representation gap. Commercial tools represent slides as visual layouts. Academic tools represent them as code. Research systems represent them as outlines. None represents the *teaching intent* — what each slide is supposed to do to the learner's understanding.

**What we know:** The representation must capture: (1) what claim is being made, (2) what evidence supports it, (3) what visual structure expresses it, (4) what pedagogical function it serves.

**What we don't know:** Whether a single representation can capture all four. Whether the representation should be symbolic (discrete primitives) or continuous (embeddings). How to handle the transition from semantic representation to visual representation.

**This question determines:** Whether the system has a coherent internal model or is just generating text-to-slides.

---

### CQ3: What is the minimum viable "teaching move"?

**Why this is the question:** If we are building a teaching system, we need atomic operations. What is the smallest unit of teaching that can be expressed on a single slide? Is it an "information unit"? A "claim"? An "explanation"? A "question"?

**What we know:** Instructional design theory describes teaching events (Gagné), teaching principles (Merrill), and cognitive operations (Bloom). But none defines the atomic unit for slide-level teaching.

**What we don't know:** Whether there is a universal atomic unit. Whether the unit varies by discipline, audience, or content type. Whether the unit is defined by its content (what it says) or its function (what it does to the learner).

**This question determines:** Whether we can generate slides compositionally or must generate them holistically.

---

### CQ4: How do we evaluate whether a slide actually helps understanding?

**Why this is the question:** Without evaluation, we cannot improve. Current evaluation is either aesthetic (does it look good?) or structural (does it follow rules?). Neither measures the actual goal: does the learner understand better?

**What we know:** Learning outcome measurement exists in educational research (pre/post tests, transfer tests). But no metric exists for evaluating individual slides or slide sequences in terms of learning impact.

**What we don't know:** Whether slide quality can be evaluated without running experiments with real learners. Whether proxy metrics (cognitive load estimation, visual complexity, content density) predict learning outcomes. Whether VLM-based evaluation can approximate human pedagogical judgment.

**This question determines:** Whether the system can self-improve or requires external validation for every change.

---

### CQ5: What is the minimum viable relationship between Intelligence and Renderer?

**Why this is the question:** The boundary between "deciding what to teach" and "producing visual output" is the architectural spine of the system. If the boundary is wrong, the system will be either too rigid ( Intelligence prescribes everything) or too loose (Renderer makes all decisions).

**What we know:** Existing tools show different points on this spectrum: Beamer gives Intelligence full control (LaTeX code = teaching decisions + rendering). Gamma gives Renderer full control (AI generates everything). Beautiful.ai splits: AI proposes layout, user refines.

**What we don't know:** Whether Intelligence should output a structured document (like a teaching plan) that Renderer executes, or a visual specification (like an SVG description) that Renderer renders, or something in between.

**This question determines:** The system's flexibility, editability, and faithfulness to teaching intent.

---

## 3. Minimal Conceptual Model

```
Source Document
       │
       ▼
   ┌─────────────┐
   │ Intelligence │ ← Teaching principles, audience model
   │   (Select,   │
   │   Sequence,  │
   │   Structure) │
   └──────┬──────┘
          │
          ▼
  Intermediate Representation
  (Teaching Plan: what to teach, in what order, with what function)
          │
          ▼
   ┌─────────────┐
   │   Renderer   │ ← Visual principles, layout rules
   │  (Visualize, │
   │   Layout,    │
   │   Export)    │
   └──────┬──────┘
          │
          ▼
     Slide Deck
          │
          ▼
    Learner encounters slides
          │
          ▼
    (Learning happens or doesn't)
```

### What this model includes (and why)

- **Source Document:** The input. Without it, the system has nothing to work with.
- **Intelligence:** The layer that makes teaching decisions. Without it, the system is just a layout engine.
- **Intermediate Representation:** The bridge between teaching decisions and visual output. Without it, Intelligence and Renderer cannot be decoupled.
- **Renderer:** The layer that produces visual output. Without it, the system cannot produce slides.
- **Learner:** The ultimate target. Without considering the learner, the system optimizes for the wrong thing.

### What this model deliberately excludes

- **Learner Model:** We do not have a way to model individual learners in real-time. This is a research problem, not an engineering problem. We use "audience type" as a coarse proxy.
- **Knowledge Graph:** No evidence that explicit knowledge graphs improve slide generation. May add later.
- **Memory:** No evidence that slide generation benefits from persistent memory. May add later.
- **Agent/Planner/Evaluator:** These are architectural choices, not conceptual necessities. They may emerge but are not assumed.

### What the model does NOT claim

- This is NOT the only possible model.
- This is NOT proven to be the best model.
- This is the MINIMUM model that explains what we are trying to do.
- If experiments show it is insufficient, it should be revised.

---

## 4. Core Ontology

### Objects We Need

#### Source
- **Why needed:** The system must have input.
- **What it is:** Any academic content: paper, lecture notes, textbook chapter, research data, conceptual outline.
- **Problem it solves:** Defines what the system works with.
- **If removed:** System has no input.

#### Claim
- **Why needed:** The atomic unit of teaching is asserting something is true (or asking whether it is true).
- **What it is:** A proposition that the presentation asks the audience to accept, understand, or evaluate.
- **Problem it solves:** Without claims, we cannot distinguish "information" from "teaching."
- **Relationship to other objects:** A claim is supported by Evidence. A claim is expressed through a Visual Structure. A claim occupies one or more Slides.
- **If removed:** The system cannot tell the difference between a data dump and a lesson.
- **Theoretical support:** Alley's assertion-evidence approach; argumentation theory.

#### Evidence
- **Why needed:** Claims without evidence are assertions. Academic integrity requires evidence.
- **What it is:** Data, citations, examples, demonstrations, or reasoning that supports a claim.
- **Problem it solves:** Ensures the system does not generate unsupported content.
- **Relationship to other objects:** Evidence supports Claims. Evidence comes from the Source.
- **If removed:** The system could generate plausible but unfounded content.
- **Theoretical support:** Scientific method; evidence-based practice.

#### Teaching Move
- **Why needed:** A claim + evidence pair does not specify what the slide DOES to the learner. The teaching move specifies the pedagogical function.
- **What it is:** An operation applied to a claim/evidence pair that determines its pedagogical function (e.g., "introduce," "demonstrate," "compare," "challenge").
- **Problem it solves:** Separates "what to say" from "what to do."
- **Relationship to other objects:** A Teaching Move operates on Claims/Evidence. A Teaching Move is expressed on a Slide.
- **If removed:** Slides become "information cards" instead of "teaching actions."
- **Theoretical support:** Gagné's events of instruction; Merrill's principles; Bloom's taxonomy.

#### Visual Structure
- **Why needed:** The same claim can be expressed visually in many ways. The choice matters.
- **What it is:** The type of visual representation chosen for a claim (e.g., diagram, chart, comparison, process flow, spatial layout).
- **Problem it solves:** Separates "what to show" from "how to show it."
- **Relationship to other objects:** A Visual Structure is chosen based on the Claim's structure and the Teaching Move.
- **If removed:** The system defaults to text or arbitrary images.
- **Theoretical support:** Bertin's visual variables; Tufte's principles; Larkin & Simon's diagram theory.

#### Slide
- **Why needed:** The physical output unit.
- **What it is:** A single visual display containing Claims, Evidence, and Visual Structure, arranged according to visual principles.
- **Problem it solves:** Defines the output format.
- **Relationship to other objects:** A Slide expresses one or more Claims using Evidence and Visual Structure, via a Teaching Move.
- **If removed:** No output.

### Objects We Deliberately Exclude (For Now)

| Excluded Object | Why Excluded | When to Reconsider |
|-----------------|-------------|-------------------|
| Learner Model | No way to model individual learners in real-time; audience type is sufficient proxy | When we have data on learner variation |
| Knowledge Graph | No evidence it improves slide generation; may add unnecessary complexity | When we need cross-document knowledge connections |
| Deck Sequence Model | premature — we don't know if decks are linear, branching, or state-based | After testing different sequence models |
| Evaluation Metric | We don't know what to measure yet | After CQ4 is partially answered |
| Audience Profile | Too vague — "expert vs. novice" is sufficient for now | When discipline-specific design is needed |

---

## 5. Teaching Primitive

### What Happens When Teaching Occurs?

The question is not "what elements are on a slide?" but "what operation is the teacher performing?"

### Candidate Primitives

| Primitive | What It Does | Example |
|-----------|-------------|---------|
| **Introduce** | Names a concept and establishes its relevance | "The mitochondria is the powerhouse of the cell" |
| **Distinguish** | Shows the boundary between two concepts | "Mitochondria vs. chloroplasts" |
| **Demonstrate** | Shows how something works through concrete example | Animated diagram of cellular respiration |
| **Explain** | Provides causal or mechanistic reasoning | "This happens because..." |
| **Compare** | Places two things side-by-side to reveal similarities/differences | Side-by-side data visualization |
| **Challenge** | Presents a problem or contradiction that requires resolution | "But if X is true, why does Y happen?" |
| **Apply** | Asks the learner to use knowledge in a new context | "Given this data, what would you predict?" |
| **Synthesize** | Connects multiple pieces into a coherent whole | Summary diagram showing how parts fit together |

### The Minimal Teaching Move

A teaching move is defined as:

```
TeachingMove = Operation × Subject × IntendedEffect
```

Where:
- **Operation** is one of the primitives above
- **Subject** is the Claim/Evidence being operated on
- **IntendedEffect** is what should change in the learner's understanding

### What This Is NOT

- This is NOT a complete taxonomy. More primitives may exist.
- This is NOT proven to be universal. Discipline-specific primitives may be needed.
- This is a WORKING DEFINITION that can be tested and revised.

### The Key Distinction

An **information unit** says: "Here is a fact."

A **teaching move** says: "Here is a fact, and by encountering it this way, you should now be able to X."

The difference is the **IntendedEffect**. Without it, we have information delivery, not teaching.

---

## 6. Deck Model

### Three Candidate Models

#### Model A: Linear Sequence

```
Slide 1 → Slide 2 → Slide 3 → ... → Slide N
```

**Assumption:** Each slide leads logically to the next. The deck is a path through content.

**Evidence for:** Most presentations are delivered linearly. Simple to generate.

**Evidence against:** Real learning is not linear. Learners bring different prior knowledge. The same path doesn't work for everyone.

**Suitable for:** Short presentations (<20 slides), single-audience talks.

#### Model B: Teaching Sequence (Gagné-inspired)

```
Gain Attention → Inform Objectives → Stimulate Recall → 
Present Content → Provide Guidance → Elicit Performance → 
Provide Feedback → Assess → Enhance Transfer
```

**Assumption:** The deck follows an instructional design sequence.

**Evidence for:** Gagné's model has strong meta-analytic support (SMD=1.55). Provides pedagogical structure.

**Evidence against:** Designed for full lessons, not 15-minute talks. Rigid sequence may not fit all content. Designed for narration-accompanied instruction, not standalone slides.

**Suitable for:** Teaching lectures, course materials.

#### Model C: State-Transition

```
Learner State₁ → Teaching Move → Learner State₂ → Teaching Move → Learner State₃
```

**Assumption:** Each slide transitions the learner from one understanding state to another.

**Evidence for:** Most theoretically principled. Directly models learning. Aligns with constructive alignment.

**Evidence against:** We cannot observe learner states in real-time. Requires a learner model we don't have. May be computationally intractable.

**Suitable for:** Adaptive systems, intelligent tutoring (not yet for slide generation).

### Our Working Model: Model B (Modified)

We adopt a simplified teaching sequence for v0.1:

```
Frame (What we're exploring)
  → Context (Why it matters)
    → Key Idea (The central claim)
      → Evidence (Supporting data/examples)
        → Elaboration (How it connects/extends)
          → Application (Using the knowledge)
            → Synthesis (How it all fits)
```

**Why this model:**
- Maps to Gagné's events (gain attention, present content, provide guidance, elicit performance)
- Maps to Merrill's principles (task-centered, activation, demonstration, application, integration)
- Simple enough to generate programmatically
- Testable: we can compare this structure against alternatives

**Known limitations:**
- Linear — doesn't adapt to learner variation
- Assumes one "right" sequence for a given content
- May not work for all content types (e.g., math proofs, case studies, data analysis)

**Alternative models to test:**
- Model A (pure linear) as baseline
- Model C (state-transition) as aspirational
- Discipline-specific variants

---

## 7. Teaching Grammar v0.1

### What Teachers Do to Learners

The teaching grammar defines the合法 combinations of teaching primitives. Not every sequence is pedagogically valid.

### Valid Transitions

```
Frame → Context → Key Idea → Evidence → Elaboration → Application → Synthesis
```

**Core rules:**
1. A Key Idea must be preceded by Context (why it matters)
2. Evidence must follow a Key Idea (evidence supports claims)
3. Application must follow Evidence (you can't apply what you haven't been shown)
4. Synthesis must come last (it connects everything)

### Composition Rules

| Rule | Description | Example |
|------|-------------|---------|
| R1 | Frame must establish relevance before any content | "Why should you care about this?" |
| R2 | Each Key Idea must have at least one Evidence unit | Claim without evidence = assertion |
| R3 | Evidence types should match claim types | Data claim → data evidence; mechanism claim → diagram evidence |
| R4 | Application must target the same cognitive level as the Key Idea | Remember-level claim → remember-level application |
| R5 | No more than 3 Key Ideas per 15-minute segment | Cognitive load constraint |

### What This Grammar Does NOT Define

- It does NOT specify visual layout (that's Visual Grammar)
- It does NOT specify content selection (that's Intelligence)
- It does NOT specify sequence optimization (that's open)
- It does NOT define all possible teaching sequences (it defines one minimal valid sequence)

### Known Violations That May Be Valid

| Violation | When It Might Be Valid |
|-----------|----------------------|
| Skip Context | Expert audience, obvious relevance |
| Multiple Evidence per Claim | Complex or contested claims |
| Application before Evidence | Problem-based learning (present problem, then reveal) |
| No Synthesis | Short presentations (<10 slides) |

---

## 8. Visual Grammar v0.1

### Conceptual Structure → Visual Representation

The visual grammar maps the STRUCTURE of knowledge to VISUAL FORM. Not "what topic" but "what relationship."

| Knowledge Structure | Visual Representation | When to Use |
|---------------------|----------------------|-------------|
| **Sequence** (A → B → C) | Timeline, process diagram, flow chart | Showing steps, history, causation chain |
| **Hierarchy** (A contains B, C, D) | Tree diagram, nested boxes, organization chart | Showing classification, structure, containment |
| **Comparison** (A vs. B) | Side-by-side panels, small multiples, mirror layout | Showing similarities/differences |
| **Distribution** (values across range) | Histogram, box plot, density chart | Showing variation, spread, patterns |
| **Relationship** (A correlates with B) | Scatter plot, network diagram, connected nodes | Showing correlation, connection, association |
| **Causality** (A causes B) | Arrow diagram, before/after, mechanism diagram | Showing cause-effect, mechanism, process |
| **State** (current condition) | Status diagram, condition table, snapshot | Showing current state, conditions, status |
| **Transformation** (A becomes B) | Before/after, morphing animation, change diagram | Showing change, process, evolution |
| **Space** (where things are) | Map, spatial layout, spatial metaphor | Showing location, spatial relationships |

### Rules for Visual Choice

1. **Match structure to representation.** A sequence should use a sequence visualization, not a comparison visualization.
2. **Minimize elements.** Each visual should have ≤6 distinguishable elements (cognitive load constraint).
3. **Label directly.** Place labels on the visualization, not in a separate legend (spatial contiguity).
4. **Use color purposefully.** Color should encode information, not decorate.
5. **Ensure lie factor = 1.** Proportional representations must be proportional.

### When Visuals INCREASE Cognitive Load

| Situation | Why It Increases Load | Alternative |
|-----------|----------------------|-------------|
| 3D effects on 2D data | Distorts perception; adds irrelevant dimensions | Use 2D |
| Decorative images | Compete with data for attention | Remove |
| Multiple chart types on one slide | Requires switching mental models | Use one chart type |
| Animated charts without narration | Viewer cannot control pace; transience effect | Use static or provide pause controls |
| Complex network diagrams | Too many nodes/edges to process | Simplify or decompose |

### What This Grammar Does NOT Define

- It does NOT specify exact coordinates, sizes, or colors (that's Renderer)
- It does NOT specify text content (that's Intelligence)
- It does NOT guarantee effectiveness (that requires evaluation)
- It does NOT cover all possible visual forms (it covers the most common knowledge structures)

---

## 9. Intelligence / Renderer Boundary

### The Interface

```
┌─────────────────────────────────────────┐
│            INTELLIGENCE                  │
│                                         │
│  Input: Source Document + Audience Type  │
│                                         │
│  Operations:                            │
│  - Content Selection (what to include)  │
│  - Teaching Sequencing (order)          │
│  - Claim Extraction (what to assert)    │
│  - Evidence Mapping (what supports)     │
│  - Teaching Move Assignment (function)  │
│  - Visual Structure Choice (representation type) │
│                                         │
│  Output: Teaching Plan                  │
│  (sequence of TeachingMoves with        │
│   Claims, Evidence, and VisualStructure) │
└─────────────────┬───────────────────────┘
                  │
                  │ Teaching Plan
                  │ (JSON / structured document)
                  │
                  ▼
┌─────────────────────────────────────────┐
│             RENDERER                     │
│                                         │
│  Input: Teaching Plan                   │
│                                         │
│  Operations:                            │
│  - Layout (coordinates, spacing)        │
│  - Typography (fonts, sizes, hierarchy) │
│  - Color (palette, contrast)            │
│  - Shapes (boxes, arrows, connectors)   │
│  - Charts (from data specifications)    │
│  - Animation (transitions, reveals)     │
│  - Export (PPTX, PDF, HTML)             │
│                                         │
│  Output: Visual Slide Deck              │
└─────────────────────────────────────────┘
```

### What Belongs in Intelligence (Evidence-Based)

| Decision | Why It's Intelligence | Evidence |
|----------|----------------------|----------|
| Content selection | Teaching decision: what matters for learning | Constructive alignment (Biggs); backward design (Wiggins) |
| Teaching sequence | Pedagogical decision: order affects learning | Gagné's events; Merrill's principles |
| Claim extraction | Argumentative decision: what to assert | Alley's assertion-evidence approach |
| Evidence mapping | Integrity decision: what supports claims | Scientific method; academic norms |
| Teaching move assignment | Pedagogical decision: what the slide does | Bloom's taxonomy; instructional design |
| Visual structure choice | Cognitive decision: what representation reduces load | Larkin & Simon (1987); Bertin (1967) |

### What Belongs in Renderer (Evidence-Based)

| Decision | Why It's Renderer | Evidence |
|----------|------------------|----------|
| Exact coordinates | Aesthetic/technical decision | Layout theory (no strong evidence for "best" layouts) |
| Typography choices | Aesthetic decision within constraints | Readability research (sans-serif > serif for projection) |
| Color palette | Aesthetic decision within constraints | Color theory; accessibility (WCAG) |
| Shape drawing | Technical decision | Graphics rendering |
| Chart generation from specifications | Technical decision | Data visualization libraries |
| Animation | Technical decision | Animation research (context-dependent) |
| Export format | Technical decision | Platform requirements |

### What Is Genuinely Uncertain

| Decision | Current Assignment | Why It's Uncertain |
|----------|-------------------|-------------------|
| Number of claims per slide | Intelligence | Could be Renderer (layout constraint) |
| Slide density | Intelligence | Could be Renderer (layout constraint) |
| When to use animation | Intelligence | Could be Renderer (technical decision) |
| Accessibility adaptations | Renderer | Could be Intelligence (pedagogical decision) |

### The Key Principle

> **Intelligence decides WHAT and WHY. Renderer decides HOW.**

If a decision affects what the learner understands or learns, it belongs in Intelligence.
If a decision affects how something looks but not what it teaches, it belongs in Renderer.

---

## 10. Critical Unknowns

These are the 3 questions that will most likely determine whether this system succeeds or fails.

### Unknown 1: Can LLMs reliably extract teaching structure from academic content?

**Why it matters:** If an LLM cannot reliably decompose a paper into claims, evidence, and pedagogical sequence, the entire Intelligence layer fails. The system becomes a fancy template engine.

**What we know:** LLMs are good at summarization and extraction. They can follow instructions about format. They can identify arguments in text.

**What we don't know:** Whether they can do this with pedagogical integrity. Whether they can distinguish "important for experts" from "important for learners." Whether they can generate sequences that actually teach rather than just organize.

**Possible experiment:** Give an LLM a 10-page paper. Ask it to extract: (1) the 5 most important claims, (2) the evidence for each, (3) a teaching sequence. Have domain experts evaluate. Compare against human-generated sequences.

**Success signal:** Experts rate LLM sequences as pedagogically valid >70% of the time.

**Failure signal:** Experts identify systematic pedagogical errors (e.g., claiming before context, evidence before claim, wrong cognitive level).

---

### Unknown 2: Can visual structure be automatically matched to knowledge structure?

**Why it matters:** If we cannot automatically choose the right visual representation for a given knowledge structure, the Renderer either makes bad choices or defaults to text. The "visual explanation" value proposition collapses.

**What we know:** Knowledge structures can be classified (sequence, hierarchy, comparison, etc.). Visual representations exist for each structure. The mapping is not arbitrary.

**What we don't know:** Whether an LLM can reliably classify knowledge structure and choose appropriate visual representation. Whether the mapping is context-dependent (same structure, different visualization in different disciplines). Whether generated visualizations actually reduce cognitive load compared to text.

**Possible experiment:** Give an LLM 20 knowledge claims from different domains. Ask it to: (1) classify the knowledge structure, (2) propose a visual representation. Have visualization experts evaluate. Compare against text-only versions.

**Success signal:** Experts agree with classification >80% of the time. Generated visualizations are rated as clearer than text.

**Failure signal:** Systematic misclassification. Visualizations that add confusion rather than clarity.

---

### Unknown 3: Can we evaluate slide quality without running learning experiments?

**Why it matters:** If every design change requires a full learning experiment, iteration is impossibly slow. We need proxy metrics that predict learning impact.

**What we know:** Cognitive load can be estimated (though imperfectly). Visual complexity can be measured. Content density can be counted. These correlate with learning outcomes in controlled studies.

**What we don't know:** Whether these proxies are reliable enough for iterative design. Whether VLM-based evaluation can approximate pedagogical judgment. Whether structural metrics (does it follow the grammar?) predict effectiveness.

**Possible experiment:** Generate 30 slide sequences with varying quality (some follow principles, some violate them). Measure: (1) proxy metrics (word count, element count, visual complexity, structural compliance), (2) human ratings of pedagogical quality. Check correlation.

**Success signal:** Proxy metrics correlate with human ratings at r > 0.6.

**Failure signal:** No correlation, or correlation only for superficial features (e.g., "looks clean") not pedagogical features (e.g., "teaches effectively").

---

## 11. Minimal Experiments

### Experiment A: Teaching Structure Extraction

**Question:** Can an LLM extract pedagogically valid structure from an academic paper?

**Setup (30 minutes):**
1. Select 3 academic papers (1 STEM, 1 social science, 1 humanities — use open-access papers)
2. For each paper, prompt an LLM:
   - "Extract the 5 most important claims from this paper"
   - "For each claim, identify the supporting evidence"
   - "Propose a teaching sequence for presenting this paper's key ideas in 15 minutes"
3. Collect outputs

**Evaluation (30 minutes):**
1. Have 2 domain experts independently rate each sequence:
   - Is the sequence pedagogically valid? (Yes/No)
   - Are the claims actually important? (1-5)
   - Is the evidence correctly identified? (Yes/No)
   - Would this sequence help a novice understand the paper? (1-5)
2. Compare across papers and domains

**What we learn:**
- Whether LLMs can do pedagogical extraction at all
- Whether performance varies by domain
- What kinds of errors are systematic

**Time:** ~1 hour

---

### Experiment B: Visual Structure Matching

**Question:** Can visual representations be automatically matched to knowledge structures?

**Setup (30 minutes):**
1. Create 20 knowledge claims from different domains:
   - 5 sequences (processes, timelines)
   - 5 hierarchies (classifications, structures)
   - 5 comparisons (A vs. B)
   - 5 relationships (correlations, connections)
2. For each claim, prompt an LLM:
   - "What type of knowledge structure is this?"
   - "What visual representation would best express this?"
   - "Generate a description of the visualization"
3. For each description, create the visualization (using any tool — hand-drawn, code, or AI-generated)
4. Also create a text-only version of each claim

**Evaluation (30 minutes):**
1. Show paired versions (visual vs. text) to 5 people unfamiliar with the content
2. Ask: "Which version helps you understand this idea faster?" and "Which version helps you remember this idea better?"
3. Record preference and any confusion

**What we learn:**
- Whether automatic visual structure matching works
- Which knowledge structures are hardest to visualize
- Whether visualization actually helps (or just looks nice)

**Time:** ~1 hour

---

### Experiment C: Blind Pedagogical Evaluation

**Question:** Can people distinguish "teaching slides" from "information slides"?

**Setup (20 minutes):**
1. Select 2 real academic presentations (from open-access sources like MIT OCW)
2. Create two versions of each:
   - Version A: Original slides (information-focused)
   - Version B: Modified slides following our Teaching Grammar (claim + evidence + teaching move structure)
3. Ensure both versions cover the same content

**Evaluation (40 minutes):**
1. Show slides to 5 people (without narration)
2. Ask:
   - "After viewing these slides, what is the main idea?" (comprehension)
   - "What would you do with this knowledge?" (application)
   - "Which version would you prefer to learn from?" (preference)
   - "Which version feels like it's teaching you something?" (teaching perception)
3. Compare responses between versions

**What we learn:**
- Whether our teaching grammar produces perceivably different slides
- Whether people can detect "teaching" without narration
- Whether our modifications actually help or just add structure

**Time:** ~1 hour

---

## 12. Open Questions (Carried Forward)

These remain genuinely unanswered after Phase 2. They should be investigated before or during Phase 3.

1. **Does the teaching grammar apply to all academic disciplines?** We have no evidence for discipline-specific differences. The grammar may need variants.

2. **How many claims can a learner process per slide?** The "≤6 elements" rule is from cognitive load theory but hasn't been validated for claims specifically.

3. **Should slides be designed for viewing with or without narration?** Most Mayer principles assume narration. Standalone slides (shared decks, poster sessions) may need different rules.

4. **Can the teaching grammar handle mathematical proofs?** Our primitives (Introduce, Distinguish, etc.) may not map to mathematical reasoning.

5. **What is the right level of abstraction for the intermediate representation?** Too abstract = Renderer has too much freedom. Too concrete = Intelligence is too rigid. Where is the right balance?

6. **How should the system handle contested knowledge?** Academic fields have debates. Should slides present one side, both sides, or the debate itself?

7. **Can VLM-based evaluation replace human evaluation?** We hypothesize yes, but have no evidence.

---

## 13. What We Explicitly Do NOT Know

The following are things we have decided NOT to address in this phase. This is not because they are unimportant, but because addressing them now would be premature.

| Topic | Why We Don't Address It |
|-------|------------------------|
| Architecture | Premature — we don't know enough about the Intelligence/Renderer boundary |
| Programming language/framework | Premature — depends on architecture |
| Business model | Premature — depends on whether the system works |
| Timeline | Premature — depends on unknowns |
| Benchmark | Premature — we don't know what to measure yet |
| Final rubric | Premature — depends on evaluation research |
| Complete teaching taxonomy | Premature — our primitives are a starting point, not a final answer |
| Universal visual grammar | Premature — our mappings are a starting point |
| Learner modeling | Out of scope — no reliable way to model individual learners in real-time |
| Real-time adaptation | Out of scope — requires learner modeling we don't have |
| Multi-language support | Out of scope — English only for now |
| Cultural adaptation | Out of scope — most research is Western-focused |

---

## Summary

### What We Have

- A minimal conceptual model (Source → Intelligence → IR → Renderer → Slides → Learner)
- A core ontology (Source, Claim, Evidence, Teaching Move, Visual Structure, Slide)
- A teaching primitive definition (Operation × Subject × IntendedEffect)
- A deck model (simplified teaching sequence)
- A teaching grammar v0.1 (valid transitions between primitives)
- A visual grammar v0.1 (knowledge structure → visual representation mappings)
- An Intelligence/Renderer boundary definition
- 3 critical unknowns with proposed experiments
- 3 minimal experiments completable in ~3 hours total

### What We Don't Have

- Proof that any of this works
- Evidence that the teaching grammar produces better learning outcomes
- Evidence that visual structure matching works automatically
- Evidence that we can evaluate quality without experiments
- A working system
- A complete theory

### What We Believe (But Cannot Yet Prove)

- Teaching is a different problem than information delivery
- Slides can be designed to teach, not just inform
- The gap between Intelligence and Renderer is where the most value lives
- Avoiding failures may be more tractable than achieving excellence
- The minimum viable system is a teaching-aware content extractor + visual structure matcher

### The Honest Assessment

This foundation is a HYPOTHESIS. It says: "If we build a system that extracts teaching structure from academic content and matches visual representations to knowledge structures, it will produce slides that teach better than current tools."

This has not been tested. It may be wrong. The experiments in Section 11 are designed to find out.

**Phase 2 success criterion met:** We have a theory small enough to test and honest enough to be wrong.

**Next phase:** Theory → Experimental Prototype.
