<!--
author:    Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Textbook

title:     S06 – Hands-on LiaScript (Self-learning unit)
comment:   AI in TVET I – Self-learning unit for session 6 (live, 19.11.2026): LiaScript syntax, GitHub workflow, building learning nuggets with AI, preparing the 10-minute pitch and the final submission.
-->

# S06 – Hands-on LiaScript

> **Session 6 · 19.11.2026 · 🟢 Live · Pitch presentations** – use this unit to build your nuggets and your pitch **before** the session, and as a reference until the final submission (15.01.2027).
>
> **Time needed:** about 2–3 hours of hands-on work

**After this unit you will be able to …**

1. write a LiaScript file with header, slides, media, quizzes and speaker notes,
2. publish it via GitHub and open it with the LiaScript link,
3. generate and revise nugget content with AI using a template,
4. prepare a convincing 10-minute pitch of your micro-credential.

## 1. What Is LiaScript?

LiaScript is an extension of **Markdown** that turns a plain text file into an interactive course: quizzes, animations, text-to-speech, videos and code – without a learning management system. Because the course is plain text, it is easy to version, translate and **generate with AI**.

``` ascii
 your-nugget.md  ──►  GitHub (raw link)  ──►  liascript.github.io/course/?<raw link>
   (plain text)        (storage, versions)       (interactive course in the browser)
```

## 2. The Basic Syntax

### Header

```markdown
<!--
author:   First Last
email:    first.last@st.ovgu.de
version:  0.1.0
language: en
narrator: UK English Female
mode:     Textbook
-->
```

`mode: Presentation` shows one slide at a time (for your pitch); `mode: Textbook` shows the whole page (for self-learning nuggets).

### Structure and text

```markdown
# Course title          ← title
## Section / slide      ← each ## starts a new slide
**bold**, *italic*, [link](https://…), ![image](https://…)
```

### Interactive elements

```markdown
Single choice:
- [( )] wrong
- [(X)] correct

Multiple choice:
- [[X]] correct
- [[ ]] wrong
- [[X]] correct

Text input:
[[welding]]

Hint:
[[?]] Think about the torch angle.
```

### Animations and speaker notes

```markdown
                --{{0}}--
This is read aloud on the slide (text-to-speech).

{{1}}
This block appears after the first click.
```

### Media

```markdown
!?[Video title](https://www.youtube.com/watch?v=…)
?[Audio](https://…/file.mp3)
![Image description](https://…/image.png)
```

Always add image credits (title, author, source, licence – see S05).

**Check:** Which line creates a single-choice option that is correct?

- [( )] `- [[X]] option`
- [(X)] `- [(X)] option`
- [( )] `- {{X}} option`

## 3. GitHub Workflow

1. **Sign up** at <https://github.com> (use your university email).
2. **Create a repository**, e.g. `AI_in_TVET_<your-topic>` (public).
3. **Add a file** → *Create new file* → `nugget_01.md` → paste your LiaScript code → *Commit changes*.
4. Open the file, click **Raw** and copy the link (`https://raw.githubusercontent.com/…`).
5. Open your course: `https://liascript.github.io/course/?<raw link>`.
6. For media: create a folder `media/`, upload images, and link them with their raw link.

**Tip:** Develop and test in the [LiaScript LiveEditor](https://liascript.github.io/LiveEditor/), then copy the final version to GitHub.

## 4. Building a Nugget with AI

Use a **template** so that the AI keeps the correct LiaScript syntax. A suitable starting point is the course's presentation template (see the course website) – or this prompt:

```text
You are an instructional designer for vocational education (TVET).
Create a LiaScript self-learning nugget (mode: Textbook) for this learning objective:
"<learning objective with action verb>"
Target group: <e.g. second-year apprentices in mechatronics>, language level B1.

Structure:
1. Header block (author, version, language: en, narrator: UK English Female)
2. Introduction with a workplace scenario (max. 120 words)
3. Explanation with one ASCII diagram or table
4. Worked example from the workplace
5. Two single-choice questions and one multiple-choice question (LiaScript syntax: - [(X)], - [[X]])
6. Short summary (3 bullet points)
7. References placeholder and licence CC BY 4.0

Rules: Do not invent statistics or references – write <!-- CHECK --> where a source is needed.
Never indent text by 4 or more spaces.
```

**Then revise – this is your job, not the AI's:**

- [ ] Facts correct? Sources added and checked?
- [ ] Learning objective really trained and assessed?
- [ ] Example authentic for the vocational field?
- [ ] Language suitable for the target group?
- [ ] Quiz distractors plausible, feedback helpful?
- [ ] Syntax renders in LiaScript (test!)?
- [ ] Licence and AI declaration added?

Document the prompt, the output and your changes in your **AI tools log** (component 4 of the assessment).

## 5. Preparing Your 10-Minute Pitch

**Setting:** You pitch to a simulated decision panel (provost, curriculum director, industry partners). **10 minutes pitch + 3 minutes questions.**

| Slide | Content | Time |
| --- | --- | --- |
| 1 | Title, your name, one-sentence value proposition | 0:30 |
| 2 | The skill gap: who needs this and why now? (evidence) | 1:30 |
| 3 | Target group and learning outcomes | 1:30 |
| 4 | Structure: nuggets and workload (EU elements) | 1:30 |
| 5 | Live demo: one nugget with an interactive element | 2:00 |
| 6 | Assessment and recognition (badge optional) | 1:00 |
| 7 | AI integration: where AI helps, where humans decide | 1:00 |
| 8 | Ask to the panel + references | 1:00 |

**Criteria:** clear skill gap and outcomes · convincing value · LiaScript use (slides, animations, at least one interactive element) · free speech and timing · references and AI use declared.

**Hand-in of the pitch file:** 18.11.2026, 23:59 (link in Moodle).

## 6. Final Submission Checklist (15.01.2027)

- [ ] **Micro-credential** with all EU mandatory elements
- [ ] **Learning nuggets** as LiaScript files in your GitHub repository (working links)
- [ ] **Pitch presentation** (LiaScript)
- [ ] *Optional:* **digital badge** (image + Open Badges metadata)
- [ ] **AI co-design documentation & reflection** (PDF): AI tools log + reflection paper, 1,000–1,500 words, using the UNESCO AI Competency Framework for Teachers
- [ ] Licences, image credits and AI declaration in every file

## References

- LiaScript. (n.d.). *LiaScript documentation*. https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md
- Council of the European Union. (2022). *Council Recommendation on a European approach to micro-credentials for lifelong learning and employability* (2022/C 243/02). https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022H0627(02)
- 1EdTech. (2024). *Open Badges specification v3.0*. https://www.imsglobal.org/spec/ob/v3p0/
- UNESCO. (2024b). *AI competency framework for teachers*. https://doi.org/10.54675/ZJTE2084

<small>Licence: CC BY 4.0 · Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), checked and revised by the author.</small>
