# 08 Open Questions

## What This Field Has Not Solved

These are the questions that remain genuinely unanswered after Phase 1 research. They are organized by priority and difficulty.

---

## Tier 1: Fundamental Questions (Blockers for the Project)

### Q1: How do multimedia learning principles apply to standalone slides?

**Why it matters:** Mayer's CTML was validated for narration + slides. But many academic presentations are viewed without narration (shared slides, poster sessions, self-study). Do the same principles apply?

**Current state:** Almost no research on this specific question.

**What would answer it:** Controlled experiment comparing slide designs with and without narration, measuring learning outcomes.

**Impact on project:** If principles change without narration, we need different design rules for different use cases.

---

### Q2: Can AI generate slides that teach (not just inform)?

**Why it matters:** This is the core value proposition of our future project. But "teaching" requires pedagogical design, not just content presentation.

**Current state:** No system has been validated for teaching effectiveness. Auto-Slides mentions cognitive science but has no learning outcome data.

**What would answer it:** Controlled study comparing AI-generated vs. human-designed slides on actual learning outcomes (not just aesthetic preferences).

**Impact on project:** If the answer is "no," the project may not be viable. If "yes," we need to define what "teaching" means computationally.

---

### Q3: What is the right balance between automation and human involvement?

**Why it matters:** Full automation may produce slides that don't match the presenter's intent or the audience's needs. Full manual defeats the purpose of AI assistance.

**Current state:** The spectrum exists (fully manual → fully automated) but no research identifies the optimal point for academic contexts.

**What would answer it:** User studies with academics using different levels of automation.

**Impact on project:** Determines the fundamental interaction model.

---

## Tier 2: Design Questions (Important but Not Blocking)

### Q4: How should slide design differ across disciplines?

**Why it matters:** A physics lecture, a philosophy seminar, and a medical case presentation have fundamentally different content types, visual needs, and pedagogical approaches.

**Current state:** Almost no discipline-specific research. Kosslyn (2012) found no significant differences between fields in violation rates — but this may mean all fields are equally bad, not that discipline doesn't matter.

**What would answer it:** Cross-disciplinary study comparing effective presentations in different fields.

**Impact on project:** Determines whether we need discipline-specific modules or a universal approach.

---

### Q5: How should figures, equations, and tables from papers be handled?

**Why it matters:** Academic papers contain complex visual and mathematical content. Automated systems must handle these without losing fidelity.

**Current state:** Research systems (Paper2Slides, PaperX) are improving but still struggle with complex layouts. No system handles all types well.

**What would answer it:** Systematic evaluation of figure/equation/table handling across existing systems.

**Impact on project:** Determines technical requirements for document ingestion.

---

### Q6: What is the relationship between slide design and long-term retention?

**Why it matters:** Most presentation research measures immediate recall. But the goal of academic teaching is long-term learning.

**Current state:** Almost no longitudinal studies on presentation effectiveness.

**What would answer it:** Longitudinal study measuring retention days/weeks after exposure to different slide designs.

**Impact on project:** If immediate recall doesn't predict long-term retention, we may need different design criteria.

---

### Q7: How should slides balance narrative engagement with scientific rigor?

**Why it matters:** Narrative improves engagement and recall, but oversimplification can misrepresent science. The tension is real and unresolved.

**Current state:** Debate in science communication literature (Dillon, Craig & Tasker, 2024). No empirical resolution.

**What would answer it:** Controlled study comparing narrative vs. non-narrative academic presentations on both engagement and accuracy perception.

**Impact on project:** Determines how much narrative structure to generate.

---

## Tier 3: Technical Questions (Solvable but Need Research)

### Q8: What metrics should evaluate slide quality?

**Why it matters:** Without evaluation metrics, we cannot improve the system or validate its output.

**Current state:** PPTEval (Content + Design + Coherence) and SlidesBench are early attempts. No validated metrics for pedagogical quality.

**What would answer it:** Develop and validate metrics through expert panel and user studies.

**Impact on project:** Determines how the system can self-evaluate and improve.

---

### Q9: How do virtual/hybrid presentations change the application of multimedia principles?

**Why it matters:** COVID-era shifted many presentations online. Screen-based viewing may change cognitive load patterns.

**Current state:** Limited research; most CTML studies used in-person settings.

**What would answer it:** Comparative study of in-person vs. online presentation effectiveness.

**Impact on project:** May require different design rules for different delivery modes.

---

### Q10: How can cultural differences in visual communication be handled?

**Why it matters:** Color associations, reading direction, visual metaphors, and design preferences vary across cultures.

**Current state:** Most research is Western/English-language focused. Cross-cultural visualization research is emerging but limited.

**What would answer it:** Cross-cultural study of visual communication preferences and effectiveness.

**Impact on project:** May require localization or cultural adaptation modules.

---

## Tier 4: Emerging Questions (Speculative)

### Q11: Will AI tools exacerbate format-over-substance blindness?

**Concern:** If AI makes it easy to produce beautiful slides, audiences may increasingly mistake visual polish for content quality.

**Current state:** No empirical evidence yet. The "Chicken Chicken Chicken" satire (2006) suggests the tendency already exists.

---

### Q12: What happens when AI-generated slides become indistinguishable from human-designed slides?

**Concern:** If AI quality reaches human quality, what is the role of human presenters? Does authenticity matter?

**Current state:** Philosophical question; no empirical evidence.

---

### Q13: Can slides be designed to adapt in real-time based on audience response?

**Concern:** Future systems might adjust content, pacing, or complexity based on audience engagement signals.

**Current state:** Speculative; no existing system does this. Raises ethical questions about audience manipulation.

---

## Questions We Are NOT Asking (Intentionally Excluded)

The following questions are explicitly excluded from this phase:

- "What architecture should we build?" → Phase 2
- "What programming language/framework?" → Phase 2
- "What is the business model?" → Phase 2
- "What is the timeline?" → Phase 2
- "What benchmark should we use?" → Phase 2
- "What rubric should we define?" → Phase 2

These are important but premature. Phase 1 is about understanding the problem space, not designing the solution.
