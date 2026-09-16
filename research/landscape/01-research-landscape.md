# 01 Research Landscape

## Academic Presentation / Teaching Visualization Landscape

This map identifies the major regions of knowledge relevant to building a future academic presentation generation system. Each region is a domain with its own theories, methods, practitioners, and open questions.

---

## Region 1: Multimedia Learning & Cognitive Load

**What it studies:** How people learn from combinations of words and pictures; the cognitive architecture that constrains learning from multimedia.

**Key theories:**
- Cognitive Theory of Multimedia Learning (Mayer, 2001)
- Cognitive Load Theory (Sweller, 1988)

**Key principles (evidence-based):**
- Multimedia principle: Words + pictures > words alone (d=1.35)
- Temporal contiguity: Synchronized narration + visuals (d=1.31)
- Spatial contiguity: Text near corresponding graphics (d=0.82)
- Coherence: Remove extraneous material (d=0.86)
- Redundancy: Don't add on-screen text to narration (d=0.72)
- Signaling: Highlight essential material (d=0.70)
- Segmenting: Break complex content into parts (d=0.67)

**Open questions:**
- Germane load: Is it a real construct or conceptually redundant?
- Boundary conditions: When do principles stop working?
- Expertise reversal: How do principles change for expert audiences?
- Declining effect sizes: Are effects getting smaller over time?

**Relevance to our project:** Foundational. Every slide design decision should be grounded in these principles. But the principles were validated for narration+slides, not for standalone slides.

---

## Region 2: Academic Presentation Design

**What it studies:** How academics actually design, deliver, and evaluate presentations; what makes research talks and lectures effective.

**Key works:**
- Alley, *The Craft of Scientific Presentations* (2013) — assertion-evidence approach
- Kosslyn, "PowerPoint Presentation Flaws" (2012) — 137 psychological principle violations
- Poz et al., "Ten Simple Rules for Effective Presentation Slides" (2022)
- Le Blanc & Cooper, "Death by PowerPoint" (2026) — medical education slides

**Key findings:**
- 84.4% of medical lecturers violate CTML principles (Le Blanc & Cooper, 2026)
- Minimalist slides produce 28% improvement in recall (VFT/WF Global, 2024)
- Assertion-evidence approach outperforms topic-subtopic approach (Alley & Neeley, 2005)
- Not a single PowerPoint slideshow in a 100+ sample was free of psychological violations (Kosslyn, 2012)

**Open questions:**
- Discipline-specific differences: Should STEM vs. humanities presentations differ?
- Long-term retention: Most studies measure immediate recall only
- Virtual/hybrid: How do principles change for online presentations?
- Assessment: Few validated rubrics exist for academic presentation quality

**Relevance to our project:** Directly relevant. The gap between research knowledge and practice is enormous — this is both a problem and an opportunity.

---

## Region 3: Scientific Communication

**What it studies:** How scientific knowledge is communicated within the scientific community and to the public.

**Key debates:**
- Knowledge deficit model vs. participatory communication
- Top-down dissemination vs. co-creation of knowledge
- Professional communication vs. public communication of science

**Key works:**
- Fischhoff & Scheufele, "The Science of Science Communication" (2013, PNAS)
- Bucchi & Trench, "Rethinking Science Communication" (2021)
- Druckman et al., "An Agenda for Science Communication Research" (2025, PNAS)

**Relevance to our project:** Provides context for understanding that academic presentations are not just information transfer — they are acts of scientific communication with social, cultural, and rhetorical dimensions.

---

## Region 4: Information Visualization & Visual Explanation

**What it studies:** How to represent data, processes, and relationships visually; principles for effective graphical communication.

**Key frameworks:**
- Tufte's principles: data-ink ratio, chartjunk, small multiples, graphical integrity
- Bertin's visual variables: position, size, shape, value, hue, orientation, texture
- Larkin & Simon: Diagrams reduce computation (1987)
- Few, Cairo: Practical visualization design

**Key findings:**
- Decorative elements improve memorability but decrease precision (Bateman et al., 2010)
- Line graphs with manipulated x-axes have largest deceptive impact (OR ≈ 15.4) (Pandey et al., 2015)
- Diagrams facilitate problem solving by reducing search and recognition costs (Larkin & Simon, 1987)
- Graduate visualization training produces measurable improvement (Gutiérrez de Ravé et al., 2026)

**Relevance to our project:** Visual design in academic slides is not decoration — it is explanation. Every visual element must serve a communicative purpose.

---

## Region 5: Instructional Design

**What it studies:** Systematic design of learning experiences; theories for how to structure instruction effectively.

**Key theories:**
- Gagné's Nine Events of Instruction (1965)
- Merrill's Principles of Instruction (2002)
- Constructive Alignment (Biggs, 1996)
- Backward Design (Wiggins & McTighe, 1998)
- ARCS Motivational Model (Keller, 1987)
- Bloom's Taxonomy (1956, revised 2001)
- Problem-Based Learning (Barrows, 1980)

**Key insight:** Instructional design is primarily concerned with learning outcomes, not information delivery. Most academic presentations operate at the information delivery level, not the instructional design level.

**Relevance to our project:** If we want slides that teach (not just inform), we need to incorporate instructional design principles. This is a major gap in current AI presentation systems.

---

## Region 6: Presentation Technology

**What it studies:** Tools and systems for creating, rendering, and delivering presentations.

**Landscape:**
- Traditional: PowerPoint, Keynote, Google Slides
- Academic/developer: Beamer, Slidev, Marp, Reveal.js
- AI commercial: Gamma, Beautiful.ai, Canva AI, Microsoft Copilot
- AI research: PPTAgent, Paper2Slides, Auto-Slides, SlideGen, GDP, PaperX

**Key dimensions:**
- Input: prompt vs. document vs. structured data
- Representation: slides vs. cards vs. code
- Generation: one-shot vs. multi-stage vs. multi-agent
- Citation handling: absent in most commercial tools
- Teaching design: almost entirely absent
- Human involvement: fully manual to fully automated

**Relevance to our project:** No existing system combines academic-grade citation handling + AI generation + beautiful visual design + teaching-aware structure.

---

## Region 7: Narrative & Persuasion in Academic Contexts

**What it studies:** How stories, arguments, and rhetorical structures enhance academic communication.

**Key findings:**
- Narrative messages have greater persuasive impact than non-narrative (meta-analysis: k=14 studies, N=2,834)
- Storytelling format is 20x more likely to be retained than linear facts (HBR, cited in MIT CommLab)
- ABT method (And, But, Therefore) creates engagement through conflict (Randy Olson)
- Transportation (getting "lost in the story") mediates persuasive effectiveness

**Open question:** Can storytelling principles be applied to academic slides without sacrificing scientific rigor?

**Relevance to our project:** Academic presentations that lack narrative are less engaging and less memorable. But the tension between narrative and evidence is real and unresolved.

---

## Region 8: Expertise & Learning

**What it studies:** How experts and novices differ in knowledge organization, problem-solving, and communication.

**Key findings:**
- Experts organize knowledge to support understanding, not just problem-solving
- Expert blind spot: Experts design for themselves, not for novices
- Expertise reversal: Worked examples help novices but can hinder experts
- Students expect text-heavy slides and resist minimalist designs (Schmaltz & Enström, 2014)

**Relevance to our project:** The audience's expertise level must determine the presentation's design. A system that doesn't account for this will produce slides that work for the wrong audience.

---

## How Regions Connect

```
                    ┌─────────────────────┐
                    │   Multimedia        │
                    │   Learning &        │
                    │   Cognitive Load    │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
    ┌─────────▼──────┐  ┌─────▼────────┐  ┌───▼──────────────┐
    │  Instructional  │  │  Academic    │  │  Information     │
    │  Design         │  │  Presentation│  │  Visualization   │
    │                 │  │  Design      │  │  & Visual        │
    │                 │  │              │  │  Explanation      │
    └─────────┬──────┘  └──────┬───────┘  └───┬──────────────┘
              │                │               │
              │    ┌───────────▼──────────┐    │
              └────┤  Scientific          ├────┘
                   │  Communication       │
                   └──────────┬───────────┘
                              │
              ┌───────────────┼───────────────┐
              │               │               │
    ┌─────────▼──────┐ ┌─────▼────────┐ ┌────▼─────────────┐
    │  Narrative &    │ │  Expertise & │ │  Presentation    │
    │  Persuasion     │ │  Learning    │ │  Technology      │
    └────────────────┘ └──────────────┘ └──────────────────┘
```

## What We Don't Know (Top-Level)

1. How to translate multimedia learning principles into automated slide generation rules
2. How to handle the tension between narrative engagement and scientific rigor
3. How to design for varying audience expertise levels automatically
4. How to assess the pedagogical quality of generated slides
5. How discipline-specific norms should influence slide design
6. How to handle figures, equations, and tables from academic papers
7. Whether AI can produce slides that actually teach (not just inform)
