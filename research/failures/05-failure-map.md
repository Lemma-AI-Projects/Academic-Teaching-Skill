# 05 Failure Map

## When Academic Slides Fail: A Systematic Record

This map documents the ways academic presentations fail. The purpose is to understand failure modes so that a future system can systematically avoid them.

---

## Failure Mode 1: Cognitive Overload

**What happens:** Too much information on a single slide; audience cannot process the content.

**Evidence:**
- Kosslyn (2012): 137 psychological principle violations across 100+ presentations; zero perfect slides
- Le Blanc & Cooper (2026): Medical lecturers averaged 38.3 words per slide; 84.4% violated CTML principles
- Phillips: Brain needs 500% increase in cognitive load beyond 6 elements per slide

**Why it happens:**
- Presenter knows too much about the topic (expert blind spot)
- Fear of "leaving out important information"
- Software defaults encourage text-heavy slides
- No training in cognitive load theory

**Theory:** Cognitive Load Theory (Sweller, 1988) — extraneous load from poor design consumes working memory needed for learning.

**How a future system could avoid it:**
- Enforce maximum word/element counts per slide
- Apply coherence principle (remove extraneous material)
- Apply signaling principle (highlight essential material)
- Design for ≤6 elements per slide

---

## Failure Mode 2: Redundancy Effect

**What happens:** On-screen text duplicates spoken narration, overloading the visual channel.

**Evidence:**
- Mayer, Heiser & Lonn (2001): Adding on-screen text to narration impairs learning
- Redundancy principle effect size: d=0.72
- Common in academic presentations where slides are "speaker notes"

**Why it happens:**
- Presenter uses slides as teleprompter
- Audience expects readable slides (Schmaltz & Enström, 2014)
- No understanding of dual-channel processing

**Theory:** CTML redundancy principle — words and pictures alone are better than words, pictures, and redundant words.

**How a future system could avoid it:**
- Detect when slide text duplicates likely narration
- Generate visual slides, not text slides
- Provide speaker notes separately from slide content

---

## Failure Mode 3: Split Attention

**What happens:** Audience must mentally integrate information from separate locations (e.g., legend + chart, separate label + diagram).

**Evidence:**
- Spatial contiguity principle: d=0.82 (large effect)
- Kosslyn (2012): Avoid splitting attention between multiple displays
- Sweller et al. (1998): Split-attention effect consumes working memory

**Why it happens:**
- Default chart formats place legends separately
- Labels placed away from referenced elements
- Text on one slide, image on next

**Theory:** Cognitive Load Theory — split attention effect requires extraneous cognitive processing.

**How a future system could avoid it:**
- Apply spatial contiguity: place text near corresponding graphics
- Use direct labeling instead of legends
- Never place explanatory text on a different slide from the figure it explains

---

## Failure Mode 4: Misleading Visualization

**What happens:** Charts and graphs distort data, leading to incorrect conclusions.

**Evidence:**
- Pandey et al. (2015): Line graphs with manipulated x-axes had deceptive impact OR ≈ 15.4
- 3D pie charts: OR ≈ 4.2; dual axes: OR ≈ 6.3
- Tufte's lie factor: ratio of graphic effect to data effect
- Huff (1954): *How to Lie with Statistics* — classic documentation

**Why it happens:**
- Software defaults (truncated axes, 3D effects)
- Intentional or unintentional manipulation
- Lack of statistical visualization literacy

**Theory:** Graphical integrity (Tufte, 1983) — physical representation of numbers must be proportional to quantities.

**How a future system could avoid it:**
- Detect and flag truncated y-axes
- Avoid 3D effects on charts
- Use direct labeling with units
- Apply lie factor = 1 as default
- Detect and warn about dual y-axes

---

## Failure Mode 5: Narrative Absence

**What happens:** Slides are a "data dump" — information without story, structure, or purpose.

**Evidence:**
- Oschatz & Marker (2020): Narrative messages have greater persuasive impact
- Martinez-Conde & Macknik (2019): Narrative improves recall of scientific material
- Common in academic conferences — "here is my data" without "here is why it matters"

**Why it happens:**
- Academic culture values data over narrative
- Presenter focuses on "what I did" rather than "why it matters"
- Time pressure leads to information density over coherence

**Theory:** Narrative transportation theory — stories engage different cognitive processes than lists.

**How a future system could avoid it:**
- Generate narrative arc (problem → approach → results → implications)
- Use ABT method (And, But, Therefore)
- Create "home image" or visual anchor
- Frame each slide as a claim + evidence, not just information

---

## Failure Mode 6: Audience Mismatch

**What happens:** Presentation is designed for the wrong audience — too technical for non-experts, too simple for experts.

**Evidence:**
- Expertise reversal effect: Same design helps novices but hinders experts
- Students expect text-heavy slides and resist minimalist designs (Schmaltz & Enström, 2014)
- HochWeb keynote failure: Audience revolted when content was mismatched

**Why it happens:**
- Presenter designs for themselves, not the audience
- No systematic audience analysis
- Same slides used for different audiences

**Theory:** Expertise reversal effect (Kalyuga et al., 2003) — instructional techniques that are effective for novices can be ineffective or counterproductive for experts.

**How a future system could avoid it:**
- Ask: Who is the audience? What do they already know?
- Adjust jargon level, depth, and visual complexity based on audience
- Provide different versions for different audiences
- Flag technical terms that may need explanation

---

## Failure Mode 7: Visual Clutter / Chartjunk

**What happens:** Decorative elements compete with data for attention.

**Evidence:**
- Tufte (1983): "Above all else, show the data"
- Bateman et al. (2010): Decorated graphics improve memorability for gist but not for data retrieval
- Few (2012): Embellishments make participants less accurate in extracting data values

**Why it happens:**
- Default templates include decorative elements
- Presenter adds images/colors/effects for "visual appeal"
- No understanding of data-ink ratio

**Theory:** Data-ink ratio (Tufte, 1983) — maximize proportion of ink devoted to data.

**How a future system could avoid it:**
- Apply data-ink ratio analysis
- Remove decorative backgrounds, gratuitous images, unnecessary borders
- Test: Can each element be removed without loss of information? If yes, remove it.

---

## Failure Mode 8: AI-Generated Hallucinations

**What happens:** AI generates plausible-looking but incorrect content, charts, or citations.

**Evidence:**
- Documented in LLM applications generally
- No systematic study of AI presentation hallucinations yet
- Gamma, Copilot, and other tools can generate fictional data in charts

**Why it happens:**
- LLMs generate plausible text, not verified text
- No grounding in actual data sources
- Visual generation may create charts that look real but aren't

**HYPOTHESIS:** This will become a major problem as AI presentation tools become more widely used. (Not yet verified.)

**How a future system could avoid it:**
- Ground all content in source documents
- Verify citations against actual references
- Never generate data visualizations without real data
- Flag any content not traceable to a source

---

## Failure Mode 9: Format-Over-Substance Blindness

**What happens:** Beautiful slides with poor content; form perceived as quality.

**Evidence:**
- "Chicken Chicken Chicken" satire (2006): Nonsensical text with scientific formatting received standing ovation
- Dr. Fisher-Katz parody: Every presentation mistake in one talk
- Kosslyn (2012): Observers notice violations but cannot always identify the specific problem

**Why it happens:**
- Audience heuristic: professional-looking = good content
- Tool marketing emphasizes visual polish
- No systematic evaluation of content quality

**HYPOTHESIS:** AI tools may exacerbate this by making it easy to produce beautiful but empty slides. (Not yet verified.)

**How a future system could avoid it:**
- Evaluate content quality separately from visual quality
- Never let visual design mask content weakness
- Ensure every visual element supports a substantive claim

---

## Failure Mode 10: Cultural & Accessibility Failures

**What happens:** Slides are inaccessible or inappropriate for diverse audiences.

**Evidence:**
- ACRL Visual Literacy Standards (2011, 2022): Visuals are never neutral
- Color blindness affects ~8% of males
- Cultural differences in visual interpretation
- Most research is Western/English-language focused

**Why it happens:**
- Default color schemes not tested for accessibility
- Cultural assumptions embedded in visual design
- No systematic accessibility review

**HYPOTHESIS:** Academic presentation tools need explicit accessibility checking. (Not yet verified.)

**How a future system could avoid it:**
- Use colorblind-safe palettes
- Provide alt text for all images
- Test for cultural appropriateness
- Follow WCAG guidelines for visual contrast

---

## Failure Summary Table

| Failure Mode | Severity | Prevalence | Theory | Detectability |
|--------------|----------|------------|--------|---------------|
| Cognitive overload | High | Very high (84.4%) | CLT | High (word count, element count) |
| Redundancy effect | High | High | CTML | Medium (text-narration overlap) |
| Split attention | Medium | High | CLT | Medium (layout analysis) |
| Misleading visualization | High | Medium | Graphical integrity | High (axis/encoding analysis) |
| Narrative absence | Medium | Very high | Narrative theory | Low (requires understanding) |
| Audience mismatch | Medium | High | Expertise reversal | Low (requires audience knowledge) |
| Visual clutter | Medium | High | Data-ink ratio | High (visual analysis) |
| AI hallucinations | High | Unknown | N/A | Medium (fact-checking) |
| Format-over-substance | Medium | High | N/A | Low (requires content analysis) |
| Accessibility failures | Medium | High | WCAG | High (automated checking) |
