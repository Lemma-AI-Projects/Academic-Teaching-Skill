# 07 Evidence Map

## What We Know, What We've Observed, What We Guess

This map categorizes all claims by evidence quality. Every important conclusion in this project must be traceable to one of these categories.

---

## FACT

*Reliably sourced, empirically validated, widely accepted.*

### Cognitive Architecture

| Claim | Source | Evidence |
|-------|--------|----------|
| Working memory is limited to ~7±2 items | Miller (1956) | Hundreds of replications |
| Dual-channel processing: auditory + visual | Paivio (1986); Mayer (2001) | Strong empirical support |
| Cognitive load has three types: intrinsic, extraneous, germane | Sweller (1988) | Debated (germane load questioned) |
| Worked examples reduce extraneous cognitive load | Sweller (1988) | Robust across hundreds of RCTs |

### Multimedia Learning Principles

| Claim | Source | Evidence |
|-------|--------|----------|
| Words + pictures > words alone (multimedia principle) | Mayer (2001) | d=1.35 (meta-analytic) |
| Synchronized narration + visuals > sequential (temporal contiguity) | Mayer (2001) | d=1.31 |
| Text near graphics > text separated (spatial contiguity) | Mayer (2001) | d=0.82 |
| Remove extraneous material (coherence principle) | Mayer (2001) | d=0.86 |
| On-screen text + narration impairs learning (redundancy) | Mayer, Heiser & Lonn (2001) | d=0.72 |
| Cues highlighting essential material improve learning (signaling) | Mayer (2001) | d=0.70 |
| Breaking complex content into segments improves learning | Mayer (2001) | d=0.67 |

### Visualization Principles

| Claim | Source | Evidence |
|-------|--------|----------|
| Data-ink ratio should be maximized | Tufte (1983) | Widely accepted in visualization field |
| Small multiples facilitate comparison | Tufte (1983) | Supported by perceptual research |
| Graphical integrity requires proportional representation | Tufte (1983) | Mathematical/logical basis |
| Line graphs with manipulated x-axes are highly deceptive | Pandey et al. (2015) | OR ≈ 15.4 |
| 3D effects distort perception | Multiple sources | Consistent finding across studies |

### Presentation Practice

| Claim | Source | Evidence |
|-------|--------|----------|
| Most academic presentations violate CTML principles | Kosslyn (2012); Le Blanc & Cooper (2026) | 84.4% violation rate in medical education |
| Minimalist slides improve recall | VFT/WF Global (2024) | 28% improvement in controlled study |
| Assertion-evidence approach outperforms topic-subtopic | Alley & Neeley (2005) | Empirical comparison |
| Animation has small but positive effect over static | Höffler & Leutner (2007); Berney & Bétrancourt (2016) | d=0.23 to 0.37 across meta-analyses |

### Instructional Design

| Claim | Source | Evidence |
|-------|--------|----------|
| Gagné's 9 events outperform traditional lecture | Li et al. (2025) meta-analysis | SMD=1.55 for knowledge; N=825 |
| Backward design improves achievement and retention | Özyurt et al. (2021) | Empirical comparison |
| Constructive alignment deepens learning approaches | Wang et al. (2012) | Empirical finding |
| ARCS model improves motivation | Li & Keller (2018) | 27 studies reviewed |

---

## OBSERVATION

*From real cases; observed but not systematically validated.*

### Presentation Patterns

| Observation | Source | Notes |
|-------------|--------|-------|
| Best presenters use fewer slides | Winston, Rosling cases | N=2, non-random sample |
| "Home image" concept creates coherence | McConnell (Stanford) | Single case observation |
| Narrative structure improves clarity | Multiple case studies | Correlational, not causal |
| Concrete framing > abstract framing | Baker, Rosling cases | N=2, non-random sample |
| Passion is visible in slide design | Tsao, Rosling cases | Subjective observation |

### Technology Patterns

| Observation | Source | Notes |
|-------------|--------|-------|
| PPTX export is broken for web-native AI tools | Gamma, Tome cases | Commercial products |
| No commercial AI tool handles citations well | All commercial tools | Feature audit |
| Teaching design is absent from automated systems | All systems reviewed | Feature audit |
| Markdown-based tools have better LLM generation | Marp, Slidev | Anecdotal evidence |

### Audience Patterns

| Observation | Source | Notes |
|-------------|--------|-------|
| Students expect text-heavy slides | Schmaltz & Enström (2014) | Survey data |
| Students resist minimalist designs initially | Schmaltz & Enström (2014) | Survey data |
| Expert presenters are more audience-oriented | Mehr (2023) | Computing conference study |

---

## INTERPRETATION

*Explanations of facts or observations; reasonable but not proven.*

### About Slide Design

| Interpretation | Basis | Confidence |
|----------------|-------|------------|
| Slides should teach, not just inform | Instructional design theory + presentation practice gap | High |
| Assertion-evidence approach should be the default for academic slides | Alley (2013) + empirical support | High |
| Visual design and teaching design are different problems that need different solutions | Analysis of existing tools | High |
| The "Glance Test" (3-second comprehension) applies to academic slides | Duarte (2008) + cognitive load theory | Medium |
| Every visual element must serve a communicative purpose | Tufte (1983) + Few (2012) | High |

### About AI Systems

| Interpretation | Basis | Confidence |
|----------------|-------|------------|
| No existing system combines all dimensions well | Feature audit of 15+ systems | High |
| The gap between presentation generation and teaching design is where most value can be created | Analysis of existing tools | Medium |
| Full automation is wrong for academic presentations | Expertise considerations + academic culture | Medium |
| PPTX export fidelity is make-or-break for academic adoption | Tome failure + Gamma complaints | Medium |

### About Audience

| Interpretation | Basis | Confidence |
|----------------|-------|------------|
| Audience expertise level must determine slide design | Expertise reversal effect | High |
| Academic culture values data over narrative | Observation of conference presentations | Medium |
| Training in CTML would improve slide quality | Kosslyn (2012) + Le Blanc & Cooper (2026) | High |

---

## HYPOTHESIS

*尚未验证的假设. Marked as such. Not treated as facts.*

### About System Design

| Hypothesis | What would verify it | Status |
|------------|---------------------|--------|
| AI can generate slides that actually teach (not just inform) | Controlled study comparing AI-generated vs. human-designed slides on learning outcomes | UNTESTED |
| Teaching-aware generation produces better learning outcomes than content-only generation | A/B test with real students | UNTESTED |
| Multi-agent architecture is better than single-model for academic presentation generation | Comparison study | UNTESTED |
| Visual-in-the-loop feedback improves slide quality | A/B test with/without VLM review | UNTESTED |
| Citation-aware generation is essential for academic adoption | User study with researchers | UNTESTED |

### About Principles

| Hypothesis | What would verify it | Status |
|------------|---------------------|--------|
| Mayer's principles apply equally to standalone slides (without narration) | Empirical study | UNTESTED |
| The same slide design cannot work for both expert and novice audiences | Expertise reversal study in presentation context | UNTESTED |
| Narrative structure in academic slides improves long-term retention | Longitudinal study | UNTESTED |
| Minimalist design is better for all academic contexts | Cross-disciplinary study | UNTESTED |

### About Failure Modes

| Hypothesis | What would verify it | Status |
|------------|---------------------|--------|
| AI tools will exacerbate format-over-substance blindness | Longitudinal study of AI-generated vs. human-designed slides | UNTESTED |
| AI hallucinations in academic presentations are a significant problem | Empirical study of AI-generated content accuracy | UNTESTED |
| Automated cognitive load detection can predict slide effectiveness | Validation study | UNTESTED |

---

## OPEN QUESTION

*Currently unknown; no reliable evidence.*

1. How should slide design differ across disciplines (STEM vs. humanities vs. social sciences)?
2. What is the optimal balance between automation and human involvement for academic presentations?
3. How should figures, equations, and tables from papers be handled in automated slide generation?
4. Can AI produce slides that are both beautiful and pedagogically effective?
5. What is the role of animation in academic presentations (beyond small effect sizes)?
6. How should cultural differences in visual communication be handled?
7. What metrics should be used to evaluate the quality of academic presentation slides?
8. How do virtual/hybrid presentations change the application of multimedia learning principles?
9. What is the relationship between slide design and long-term knowledge retention?
10. How can slides balance narrative engagement with scientific rigor?
