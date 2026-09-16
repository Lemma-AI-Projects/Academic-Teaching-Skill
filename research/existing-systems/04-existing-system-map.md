# 04 Existing System Map

## Presentation Software & AI Systems: What They Actually Do

This map analyzes existing tools by what problem they solve, not by feature comparison. The goal is to understand the landscape of solutions and identify what remains unsolved.

---

## Dimension 1: What Problem Does Each Tool Solve?

### Traditional Tools

| Tool | Problem Solved | Input | Output |
|------|---------------|-------|--------|
| **PowerPoint** | Create polished visual slides from scratch | Manual authoring | .pptx |
| **Keynote** | Create beautiful animated presentations on Apple | Manual authoring | .key |
| **Google Slides** | Collaborative slide creation in browser | Manual authoring | Google Slides format |

**Analysis:** These tools solve the *rendering* problem — they provide a canvas for humans to create slides. They do NOT solve content generation, teaching design, or visual explanation.

### Academic/Developer Tools

| Tool | Problem Solved | Input | Output |
|------|---------------|-------|--------|
| **Beamer** | Version-controlled, reproducible academic slides | LaTeX source | PDF |
| **Slidev** | Developer-friendly slide authoring with code highlighting | Markdown + Vue | HTML/PDF |
| **Marp** | Simple Markdown-to-slides conversion | Markdown | HTML/PDF/PPTX |
| **Reveal.js** | Highly customizable web-based presentations | HTML/Markdown | HTML |

**Analysis:** These tools solve the *reproducibility* and *developer workflow* problems. Beamer excels at citations and math. Slidev excels at code-heavy presentations. None solve content generation or teaching design.

### AI Commercial Systems

| Tool | Problem Solved | Input | Output |
|------|---------------|-------|--------|
| **Gamma** | Fast prompt-to-deck generation | Text prompt/files | Web cards/PDF/PPTX |
| **Beautiful.ai** | Professional-looking slides without design skill | Prompt/outline/document | PPTX/PDF |
| **Canva AI** | Visual design for non-designers | Short text prompt | Canva format/PPTX |
| **Microsoft Copilot** | M365-integrated AI slide creation | Prompt/files/email | Native .pptx |

**Analysis:** These tools solve the *speed* problem — going from idea to deck in 30-60 seconds. They do NOT solve academic citation handling, teaching design, or deep content understanding.

### AI Research Systems

| System | Problem Solved | Input | Output |
|--------|---------------|-------|--------|
| **PPTAgent** | Document-to-slides with style transfer | Document + reference slides | PPTX |
| **Paper2Slides** | Research paper to presentation | PDF/Word/Excel | Slides/posters |
| **Auto-Slides** | Pedagogically structured presentations | Documents | Beamer PDF + scripts |
| **SlideGen** | Visual-in-the-loop slide generation | Text | PPTX |
| **GDP** | Non-linear narrative from documents | Long documents | Slides |
| **PaperX** | Unified paper-to-multiple-formats | Scientific papers | PPT/posters/promotional |

**Analysis:** These tools solve the *document-to-slides* problem. They represent the frontier of academic presentation automation. But none combine all dimensions well.

---

## Dimension 2: Five Distinct Problems (Not One)

Most discussions conflate these. They are separate:

### 1. Content Generation
**What:** Writing the text, structuring the narrative, selecting what to include/exclude.
**Who does it well:** Gamma Agent, Copilot, Beautiful.ai AI chat
**Who doesn't:** Beamer, Slidev, Marp, Keynote, Canva

### 2. Presentation Generation
**What:** Transforming source material (paper, notes, outline) into slide structure.
**Who does it well:** PPTAgent, Paper2Slides, Auto-Slides, GDP, PaperX
**Who doesn't:** All commercial tools (they work from prompts, not documents)

### 3. Visual Design
**What:** Layout, typography, color, visual hierarchy, spacing.
**Who does it well:** Beautiful.ai (Smart Slides), Keynote, Canva
**Who doesn't:** Beamer (dated aesthetic), most research systems

### 4. Teaching Design
**What:** Pedagogical structure, learning objectives, assessment alignment, motivational design.
**Who does it well:** Almost nobody. Auto-Slides is the closest (explicitly applies cognitive science principles).
**Who doesn't:** All commercial tools, most research systems

### 5. Rendering
**What:** Converting abstract representation to visual output (PDF, HTML, PPTX).
**Who does it well:** Beamer (PDF), Reveal.js (HTML), Marp (HTML/PDF/PPTX), PPTAgent (HTML→PPTX)
**Who doesn't:** Gamma (PPTX export is architecturally broken)

---

## Dimension 3: Citation Handling (Critical for Academia)

| Tool | Citation Support | Quality |
|------|-----------------|---------|
| Beamer | BibTeX/BibLaTeX native | Gold standard |
| Auto-Slides | Via LaTeX compilation | Excellent |
| Paper2Slides | RAG-powered source tracing | Good |
| GDP | Content attribution to source paragraphs | Good |
| PaperX | Scholar DAG with cross-modal references | Good |
| PPTAgent | References from source document | Moderate |
| Gamma | Agent can research with citations | Weak |
| Copilot | Web source attribution | Weak |
| Beautiful.ai | None | None |
| Canva | None | None |
| PowerPoint (manual) | Manual referencing | Manual |

**Key finding:** No commercial AI tool handles academic citations well. This is a critical gap.

---

## Dimension 4: The PPTX Export Problem

PPTX is the universal interchange format. But web-native AI tools struggle to export to it:

- **Gamma:** Cards → fixed slides = layout flattening, font substitution, lost animations. TrustPilot 2.0/5.
- **Tome:** No PPTX export was fatal for enterprise. Shut down April 2025 despite 20M users and $81.6M raised.
- **Beautiful.ai:** PPTX export works but has issues with complex layouts.
- **Marp:** Only tool with native PPTX export among developer tools.

**HYPOTHESIS:** PPTX export fidelity is a make-or-break feature for academic adoption. (Not yet verified.)

---

## Dimension 5: Teaching Design Gap

This is the most important observation:

**No existing system systematically addresses teaching design.**

- Commercial tools focus on visual design and speed
- Research systems focus on content extraction and layout
- Only Auto-Slides explicitly mentions "cognitive science principles" in its pipeline
- No tool asks: "What should the audience learn?" before generating slides
- No tool evaluates: "Does this slide support the stated learning objective?"
- No tool considers: "What is the audience's expertise level?"

**HYPOTHESIS:** The gap between "presentation generation" and "teaching design" is where the most value can be created. (Not yet verified.)

---

## Dimension 6: Human Involvement Spectrum

```
Fully Manual ←————————————————————→ Fully Automated
PowerPoint    Keynote    Google    Beautiful.ai    Gamma    Copilot    Auto-Slides
               Marp      Slides                                   Paper2Slides
                          Reveal.js                               SlideGen
```

**Key question for our project:** Where on this spectrum should an academic presentation tool sit?

**HYPOTHESIS:** Full automation is wrong for academic presentations. The optimal point is probably "AI generates structure + content, human reviews and refines." (Not yet verified.)

---

## What No Existing System Does

1. **Ingest an academic paper** and generate a presentation that:
   - Preserves citation integrity
   - Applies teaching design principles
   - Adapts to audience expertise level
   - Produces beautiful, publication-quality visuals
   - Handles figures, equations, and tables from the paper
   - Maintains narrative coherence
   - Provides editable output in standard formats

2. **Evaluate its own output** against pedagogical criteria

3. **Explain its design decisions** to the human reviewer

This gap is the potential space for our future project.
