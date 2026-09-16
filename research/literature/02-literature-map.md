# 02 Literature Map

## Foundational Works for Academic Presentation Generation

This map identifies works with foundational significance for building a system that generates academic presentations. Each entry is classified by evidence quality and relevance.

---

## Tier 1: Core Theoretical Foundations

### 1. Mayer, R. E. (2001/2009). *Multimedia Learning*. Cambridge University Press.

- **Domain:** Educational psychology, cognitive science
- **Research question:** How do people learn from words and pictures?
- **Method:** Controlled experiments across dozens of studies
- **Main finding:** Three assumptions (dual channels, limited capacity, active processing) generate 12+ testable principles for multimedia instruction
- **Evidence:** Hundreds of experiments; 6 meta-analyses with large effect sizes
- **Limitations:** Most studies use short lessons with narration, not standalone slides; boundary conditions still being mapped
- **Relevance:** Foundational. The cognitive architecture that constrains all slide design.
- **Status:** ESTABLISHED FINDING

### 2. Sweller, J. (1988). Cognitive load during problem solving: Effects on learning. *Cognitive Science*, 12(2), 257–285.

- **Domain:** Educational psychology
- **Research question:** How does cognitive load affect learning during problem solving?
- **Method:** Randomized experiments comparing worked examples vs. problem solving
- **Main finding:** Three types of cognitive load (intrinsic, extraneous, germane); worked examples reduce extraneous load
- **Evidence:** Robust evidence from hundreds of RCTs; described by Dylan Wiliam as "the single most important thing for teachers to know"
- **Limitations:** Measurement of cognitive load remains challenging; expertise reversal effect complicates application
- **Relevance:** Defines the constraint system for slide design — every design choice must account for cognitive load.
- **Status:** ESTABLISHED FINDING

### 3. Tufte, E. R. (1983). *The Visual Display of Quantitative Information*. Graphics Press.

- **Domain:** Information design, statistical graphics
- **Research question:** How should quantitative information be displayed graphically?
- **Method:** Analysis of 250+ historical graphics; design critique grounded in mathematical principles
- **Main finding:** Data-ink ratio, chartjunk elimination, small multiples, graphical integrity
- **Evidence:** Historical case analysis; widely influential in data visualization practice
- **Limitations:** Prescriptive and aesthetic; less grounded in empirical learning research; primarily for static printed graphics
- **Relevance:** Foundational for how data should appear on slides.
- **Status:** ESTABLISHED FINDING (though some principles are debated)

### 4. Alley, M. (2013). *The Craft of Scientific Presentations* (2nd ed.). Springer.

- **Domain:** STEM communication
- **Research question:** What makes scientific presentations effective?
- **Method:** Analysis of excellent presenters (Feynman, Goodall, Cox, Bolte Taylor); grounded in cognitive science
- **Main finding:** Assertion-evidence approach outperforms topic-subtopic approach; 13 critical errors identified
- **Evidence:** 393+ citations; adopted by Harvard, MIT, Penn State
- **Limitations:** Primarily STEM-focused; practical examples skew toward engineering
- **Relevance:** The most directly applicable framework for academic slide design.
- **Status:** ESTABLISHED FINDING

---

## Tier 2: Empirical Foundations

### 5. Kosslyn, S. M. (2012). PowerPoint presentation flaws and failures: A psychological analysis. *Behavior Research Methods*, 44, 467–481.

- **Domain:** Cognitive psychology
- **Research question:** Do presentations follow psychological principles?
- **Method:** 137 rule violations identified across academic, education, government, and business presentations
- **Main finding:** No field performed significantly better; not a single slideshow was free of violations
- **Evidence:** Systematic empirical evaluation
- **Limitations:** Focused on violations, not on what works; no learning outcome measures
- **Relevance:** Documents the scale of the problem our system would address.
- **Status:** ESTABLISHED FINDING

### 6. Le Blanc, R., & Cooper, N. (2026). Death by PowerPoint. *The Clinical Teacher*, 23(1), e70315.

- **Domain:** Medical education
- **Research question:** Do medical school lecturers adhere to CTML principles?
- **Method:** Primary data collection from medical lectures
- **Main finding:** 84.4% violation rate; mean 38.3 words per slide
- **Evidence:** Primary empirical data
- **Limitations:** Medical education context; may not generalize to all disciplines
- **Relevance:** Documents the problem in a specific academic domain.
- **Status:** ESTABLISHED FINDING

### 7. Schmaltz, R., & Enström, E. (2014). Death to weak PowerPoint: Strategies to create effective slide presentations. *Frontiers in Psychology*, 5, 1138.

- **Domain:** Psychology education
- **Research question:** What strategies create effective slide presentations?
- **Method:** Literature synthesis + practical strategies
- **Main finding:** Strong presentations enhance engagement and retention; weak slides cause distraction, boredom, and impeded learning
- **Evidence:** Literature synthesis
- **Limitations:** Strategy paper, not empirical study
- **Relevance:** Bridges theory and practice for academic slide design.
- **Status:** INTERPRETATION (strategy synthesis)

### 8. Larkin, J. H., & Simon, H. A. (1987). Why a diagram is (sometimes) worth ten thousand words. *Cognitive Science*, 11(1), 65–100.

- **Domain:** Cognitive science
- **Research question:** What computational advantages do diagrams provide?
- **Method:** Computational analysis of diagrammatic vs. sentential reasoning
- **Main finding:** Diagrams reduce search for relevant information and effort for recognizing operators
- **Evidence:** Computational models; supported by subsequent empirical work
- **Limitations:** Focused on problem-solving diagrams, not presentation slides
- **Relevance:** Explains why visual explanations work in presentations.
- **Status:** ESTABLISHED FINDING

### 9. Poz, K. et al. (2022). Ten simple rules for effective presentation slides. *PLOS Computational Biology*, 17(12).

- **Domain:** Computational biology, science communication
- **Research question:** What rules help create effective academic slides?
- **Method:** Literature synthesis by practitioners
- **Main finding:** 10 rules including single message per slide, avoid bullet points, use simple diagrams, design for cognitive overload (≤6 elements)
- **Evidence:** Literature synthesis
- **Limitations:** Expert opinion, not empirical validation of all 10 rules
- **Relevance:** Practical guidelines directly applicable to academic slide design.
- **Status:** INTERPRETATION (expert synthesis)

---

## Tier 3: Instructional Design Foundations

### 10. Gagné, R. M. (1965). *The Conditions of Learning*. Holt, Rinehart & Winston.

- **Domain:** Educational psychology
- **Research question:** What conditions are necessary for learning to occur?
- **Method:** Derived from U.S. Air Force training research; applied across education
- **Main finding:** Nine events of instruction provide a sequenced framework for instructional design
- **Evidence:** 2025 meta-analysis (Li et al.) of 11 studies: SMD=1.55 for knowledge, SMD=1.83 for problem-solving
- **Limitations:** Linear sequence may not suit all contexts; originally behaviorist/cognitivist
- **Relevance:** Provides a sequenced checklist for structuring presentations as learning events.
- **Status:** ESTABLISHED FINDING

### 11. Merrill, M. D. (2002). First principles of instruction. *Educational Technology Research and Development*, 50(3), 43–59.

- **Domain:** Instructional design
- **Research question:** What are the universal principles of effective instruction?
- **Method:** Synthesis of 22 instructional theories
- **Main finding:** Five principles: task-centered, activation, demonstration, application, integration
- **Evidence:** Students 9x more likely to report mastering objectives when all five implemented (Frick et al., 2007)
- **Limitations:** Theoretical base stronger than direct empirical evidence for the unified framework
- **Relevance:** Provides a principled structure for teaching-oriented presentations.
- **Status:** ESTABLISHED FINDING

### 12. Biggs, J. (1996). Enhancing teaching through constructive alignment. *Higher Education*, 32, 347–364.

- **Domain:** Higher education pedagogy
- **Research question:** How can teaching be aligned with intended outcomes?
- **Method:** Theoretical framework + empirical validation
- **Main finding:** Outcomes, activities, and assessment must be aligned to the same cognitive levels
- **Evidence:** Wang et al. (2012): aligned courses produced deeper learning; Roßnagel et al. (2021): alignment boosted motivation
- **Limitations:** Requires significant upfront design time; designed for course level, not single presentations
- **Relevance:** Prevents the "data dump" problem — slides should be designed backward from intended outcomes.
- **Status:** ESTABLISHED FINDING

### 13. Wiggins, G., & McTighe, J. (1998). *Understanding by Design*. ASCD.

- **Domain:** Curriculum design
- **Research question:** How can instruction be designed for deep understanding?
- **Method:** Synthesis of cognitive psychology research on learning and transfer
- **Main finding:** Three-stage backward design: Desired Results → Evidence → Learning Plan
- **Evidence:** Özyurt et al. (2021): UbD students outperformed peers on achievement and retention
- **Limitations:** Implementation requires significant training; challenging at scale
- **Relevance:** Start with desired takeaway, design backward — prevents slides becoming content coverage.
- **Status:** ESTABLISHED FINDING

### 14. Keller, J. M. (1987). Development and use of the ARCS model. *Journal of Instructional Development*, 10(3), 2–10.

- **Domain:** Motivational design
- **Research question:** How can instructional materials be designed to motivate learners?
- **Method:** Based on expectancy-value theory; validated across multiple studies
- **Main finding:** Four components: Attention, Relevance, Confidence, Satisfaction
- **Evidence:** Li & Keller (2018): 27 studies showed positive effects; Fang et al. (2023): 55 studies confirmed improvement
- **Limitations:** Some studies found no significant relationship between ARCS and learning outcomes
- **Relevance:** Motivation explains up to one-third of achievement differences — slides should systematically address all four.
- **Status:** ESTABLISHED FINDING

---

## Tier 4: Visualization & Design

### 15. Bertin, J. (1967/1983). *Semiology of Graphics*. Mouton / University of Washington Press.

- **Domain:** Cartography, information design
- **Research question:** What are the fundamental visual variables for encoding information?
- **Method:** Analysis of 1,000+ maps and diagrams
- **Main finding:** Seven visual variables (position, size, shape, value, hue, orientation, texture) with specific perceptual properties
- **Evidence:** Cross-cultural applicability; foundational for cartographic education
- **Limitations:** Limited treatment of interaction or animation; some variables less relevant digitally
- **Relevance:** Provides a systematic framework for choosing visual encodings in slides.
- **Status:** ESTABLISHED FINDING

### 16. Duarte, N. (2008). *Slide:ology: The Art and Science of Creating Great Presentations*. O'Reilly Media.

- **Domain:** Professional presentation design
- **Research question:** How should slides be designed for maximum impact?
- **Method:** Case studies from major brands; professional practice at Duarte Design
- **Main finding:** Visual thinking must be learned; slides should be "visual stories"; Glance Test (3-second comprehension)
- **Evidence:** Case studies from TED, Al Gore; widely influential
- **Limitations:** Corporate/business focused; limited empirical research base
- **Relevance:** Practical visual thinking frameworks applicable to academic slides.
- **Status:** INTERPRETATION (practice-based)

### 17. Reynolds, G. (2019). *Presentation Zen* (3rd ed.). New Riders.

- **Domain:** General presentation design
- **Research question:** How can simplicity and restraint improve presentations?
- **Method:** Draws on Mayer's CTML + design principles (CRAP)
- **Main finding:** Apply restraint, simplicity, naturalness; design for how people actually process information
- **Evidence:** 711+ citations; bridges cognitive science and practical design
- **Limitations:** More inspirational than empirical; may oversimplify for complex academic content
- **Relevance:** Bridges cognitive science and practical design for academics.
- **Status:** INTERPRETATION (applied synthesis)

### 18. Few, S. (2012). *Show Me the Numbers*. Analytics Press.

- **Domain:** Data visualization
- **Research question:** How should tables and graphs be designed for clarity?
- **Method:** Systematic treatment of chart selection and design
- **Main finding:** Visualization requires both conceptual understanding and procedural skills
- **Evidence:** Practical examples; bridges statistics and visualization
- **Limitations:** Focused on business analytics, not academic presentations
- **Relevance:** Practical guidance for data-heavy academic slides.
- **Status:** INTERPRETATION (practice-based)

### 19. Cairo, A. (2013). *The Functional Art*. / (2016). *The Truthful Art*. Pearson.

- **Domain:** Information visualization, journalism
- **Research question:** How can visualizations inform and explain rather than decorate?
- **Method:** Practical examples from journalism and data analytics
- **Main finding:** Visualization should be functional art; truthfulness requires statistical literacy
- **Evidence:** Practical case studies
- **Limitations:** Journalism-focused; less applicable to formal academic contexts
- **Relevance:** Emphasizes that every visual element must serve a communicative purpose.
- **Status:** INTERPRETATION (practice-based)

---

## Tier 5: Research Systems (Emerging)

### 20. PPTAgent (EMNLP 2025). icip-cas/PPTAgent.

- **Domain:** AI presentation generation
- **Research question:** Can AI generate editable presentations from documents?
- **Method:** Two-stage edit-based generation; analyzes reference presentations
- **Main finding:** Self-correction mechanism using execution failures as feedback; PPTEval benchmark
- **Evidence:** ~5k GitHub stars; published at EMNLP
- **Limitations:** Requires reference presentations for style; text-heavy
- **Relevance:** Most advanced open-source academic presentation agent.
- **Status:** EMERGING

### 21. Auto-Slides (ICME 2026). Westlake-AGI-Lab/Auto-Slides.

- **Domain:** AI presentation generation
- **Research question:** Can multi-agent systems generate pedagogically sound presentations?
- **Method:** 6-stage pipeline (Parser → Planner → Verification → Repair → Generator → Interactive Editor)
- **Main finding:** Bilingual support; interactive revision; content verification pipeline
- **Evidence:** Published at ICME 2026
- **Limitations:** LaTeX Beamer output (limited audience); early stage
- **Relevance:** First system to explicitly address teaching design in automated generation.
- **Status:** EMERGING

### 22. PaperX (2026).

- **Domain:** Scientific paper-to-presentation
- **Research question:** Can a unified framework convert papers to multiple output formats?
- **Method:** Scholar DAG intermediate representation; cross-modal alignment
- **Main finding:** Single source → PPT, posters, promotional content; iterative VLM feedback
- **Evidence:** Recent (2026)
- **Limitations:** Limited evaluation; early stage
- **Relevance:** Addresses the document-to-presentation pipeline specifically for academic papers.
- **Status:** EMERGING

---

## Conflict Areas

1. **Germane load:** Sweller argues it's a real third type of load; some researchers argue it's conceptually redundant with intrinsic load
2. **Animation vs. static:** Small overall effect sizes (g=0.23); benefit depends heavily on context
3. **Narrative vs. evidence:** Some argue storytelling damages scientific trustworthiness; others advocate "storylistening"
4. **Minimalism vs. expectation:** Students expect text-heavy slides; minimalist designs may initially reduce satisfaction
5. **Expertise reversal:** Same design that helps novices can hinder experts — no universal "best" design
