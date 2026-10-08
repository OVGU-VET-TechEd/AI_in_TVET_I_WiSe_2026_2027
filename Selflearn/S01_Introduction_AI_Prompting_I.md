<!--
author:    Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Textbook

title:     S01 – Introduction to AI & Prompting I: how AI works, frameworks & trends (Self-learning unit)
comment:   AI in TVET I – Self-learning unit for session 1 (live, 15.10.2026): how generative AI works, prompting basics, UNESCO and EU frameworks, AI trends in TVET.
-->

# S01 – Introduction to AI & Prompting I

> **Session 1 · 15.10.2026 · 🟢 Live** – this unit accompanies the live session. Work through it afterwards to consolidate and to prepare the self-learning session on 22.10.2026.
>
> **Time needed:** about 60–75 minutes

**After this unit you will be able to …**

1. explain in your own words how a Large Language Model (LLM) produces text,
2. distinguish machine learning, deep learning and generative AI,
3. write a structured prompt (Role · Task · Context · Format · Examples) and improve it iteratively,
4. name the frameworks that guide AI in education and TVET (UNESCO AI Competency Frameworks, EU AI Act, ICT-CFT),
5. start your **AI tools log** for this seminar.

## 1. What is Artificial Intelligence?

There is no single definition. A practical one for this seminar:

> **Artificial Intelligence** describes computer systems that perform tasks which usually require human intelligence – such as recognising patterns, understanding language, making predictions or generating content.

The EU AI Act (Regulation (EU) 2024/1689, Art. 3) defines an *AI system* as a machine-based system that operates with some autonomy and **infers from its input how to generate outputs** such as predictions, content, recommendations or decisions.

### AI is a family of approaches

``` ascii
+-------------------------------------------------------------+
| Artificial Intelligence                                      |
|   rule-based systems, search, planning, ...                  |
|  +-------------------------------------------------------+  |
|  | Machine Learning: learns patterns from data           |  |
|  |  +-------------------------------------------------+  |  |
|  |  | Deep Learning: neural networks with many layers |  |  |
|  |  |  +-------------------------------------------+  |  |  |
|  |  |  | Generative AI: creates new text, images,  |  |  |  |
|  |  |  | audio, code (e.g. LLMs, diffusion models) |  |  |  |
|  |  |  +-------------------------------------------+  |  |  |
|  |  +-------------------------------------------------+  |  |
|  +-------------------------------------------------------+  |
+-------------------------------------------------------------+
```

| Approach | How it works | TVET example |
| --- | --- | --- |
| Rule-based system | Humans write if–then rules | Safety checklist app for machine start-up |
| Machine learning | Model learns patterns from labelled or unlabelled data | Predicting tool wear from sensor data |
| Deep learning | Many-layered neural networks learn complex patterns | Visual inspection of weld seams |
| Generative AI | Model generates new content from a prompt | Creating a quiz on electrical safety |

**Check:** Which statement is correct?

- [( )] Every AI system is a generative AI system.
- [(X)] Generative AI is a sub-field of deep learning, which is a sub-field of machine learning.
- [( )] Machine learning systems follow only rules written by programmers.
[[?]] Look at the nested boxes above.

## 2. How Does a Large Language Model Work?

A Large Language Model (LLM) such as GPT, Claude or Gemini is trained to **predict the next token** (a word or part of a word) in a text.

{{1}}
<section>

**Step by step**

1. **Tokens:** The text is split into small units. "Vocational education" might become `Voc` · `ational` · ` education`.
2. **Training data:** During pre-training the model sees enormous amounts of text and adjusts billions of numerical **weights** so that its predictions improve.
3. **Probabilities:** For your prompt, the model calculates for every possible next token how likely it is – and picks one. Then it repeats this, token by token.
4. **Fine-tuning:** Afterwards the model is trained with human feedback to follow instructions and to be helpful and safe.
5. **Context window:** The model only "sees" what fits into its context window: your prompt, the conversation so far and any uploaded documents.

</section>

``` ascii
Prompt: "A welder must always wear ..."

  next token        probability
  "protective"      ██████████████  0.62
  "a"               ████            0.17
  "gloves"          ███             0.12
  "safety"          ██              0.07
  ...
```

{{2}}
<section>

**What follows from this?**

- An LLM produces **plausible** text – not necessarily **true** text. This is why it can *hallucinate* facts and references.
- The output depends heavily on **your prompt and context**.
- Its knowledge ends at the **training cut-off** unless the tool searches the web or uses your documents.
- The same prompt can give **different answers** each time.

</section>

**Check:** Why can an LLM invent a reference that does not exist?

- [( )] Because it copies references from a database that contains errors.
- [(X)] Because it generates the most probable sequence of tokens, and a made-up reference can look very probable.
- [( )] Because the developers want to test users.

**Multimodal models** process and produce more than text: images, audio, video or code. Example: photograph a damaged component and ask the model to describe possible causes – then check the answer with an expert.

## 3. Prompting Basics

A **prompt** is the instruction you give to an AI tool. Good prompts are specific, give context and say what the result should look like.

### The five building blocks

| Block | Question | Example (TVET) |
| --- | --- | --- |
| **Role** | Who should the AI act as? | "You are an experienced trainer for electricians." |
| **Task** | What exactly should it do? | "Create five multiple-choice questions …" |
| **Context** | For whom, why, with which constraints? | "… for first-year apprentices, topic: protective measures against electric shock, based on the attached text." |
| **Format** | What should the output look like? | "Table with question, four options, correct answer, short explanation." |
| **Examples** | What does a good result look like? | "Example question: …" |

### Weak vs. strong prompt

**Weak:**

```text
Make a quiz about electricity.
```

**Strong:**

```text
You are an experienced trainer for electricians in Germany.
Create 5 multiple-choice questions for first-year apprentices on
protective measures against electric shock. Use only the attached text.
Format: table with question | 4 options | correct answer | 1-sentence explanation.
Difficulty: understanding level (Bloom 2). Language: simple English.
```

### Iterate!

Prompting is a dialogue. Review the first output and refine:

``` ascii
 Prompt ──► Output ──► Evaluate ──► Refine prompt ──► Better output
   ▲                                                       │
   └───────────────────────────────────────────────────────┘
```

Typical follow-up prompts: *"Make the distractors more plausible."* · *"Add a workplace scenario to each question."* · *"Which of your statements are uncertain? Mark them."*

### The CLEAR framework

Lo (2023) summarises good prompting as **CLEAR**: **C**oncise · **L**ogical · **E**xplicit · **A**daptive · **R**eflective. *Adaptive* and *reflective* mean: adjust your prompt to the results and critically evaluate the output.

**Practice:** Rewrite this weak prompt using all five building blocks. Paste your result into your AI tools log.

```text
Explain AI to my students.
```

<details>
<summary>Show a possible solution</summary>

```text
You are a vocational teacher training first-year mechatronics apprentices.
Explain in about 200 words what Artificial Intelligence is, using one example
from a production workshop. Format: short text + 3 key terms with definitions.
Example of the tone: "Imagine a camera that learns what a good weld looks like …"
```

</details>

## 4. Frameworks for AI in Education and TVET

This seminar is anchored in international frameworks. You will use them for your micro-credential.

### UNESCO AI Competency Framework for Students (2024)

Four dimensions, each on three progression levels **Understand – Apply – Create**:

1. Human-centred mindset
2. Ethics of AI
3. AI techniques and applications
4. AI system design

### UNESCO AI Competency Framework for Teachers (2024)

Five dimensions, each on three levels **Acquire – Deepen – Create**:

1. Human-centred mindset
2. Ethics of AI
3. AI foundations and applications
4. AI pedagogy
5. AI for professional development

### EU AI Act (Regulation (EU) 2024/1689)

A **risk-based** law:

| Risk level | Meaning | Education example |
| --- | --- | --- |
| Unacceptable | Prohibited | Emotion recognition of learners in education institutions (with narrow exceptions) |
| High risk | Strict obligations (risk management, data quality, human oversight, documentation) | AI that decides on admission, evaluates learning outcomes or monitors behaviour in exams |
| Limited risk | Transparency obligations | Chatbots must disclose that users interact with AI; AI-generated content must be labelled |
| Minimal risk | No specific obligations | Spam filter, spell checker |

Since February 2025, organisations that deploy AI must also take measures to ensure sufficient **AI literacy** of their staff (Art. 4).

### Further anchors

- **UNESCO ICT Competency Framework for Teachers (ICT-CFT, Version 3, 2018)** – ICT skills of teachers in six aspects and three levels.
- **UNESCO Guidance for Generative AI in Education and Research (2023)** – recommendations for a human-centred use of GenAI, e.g. an age limit of 13 for independent use in the classroom.

**Check:** Which levels does the UNESCO AI Competency Framework for **Teachers** use?

- [( )] Understand – Apply – Create
- [(X)] Acquire – Deepen – Create
- [( )] Remember – Understand – Apply

**Check:** An AI system that automatically grades final exams in a vocational school is, under the EU AI Act, …

- [( )] minimal risk
- [( )] limited risk
- [(X)] high risk
- [( )] prohibited

## 5. AI Trends in TVET and the Labour Market

AI changes **what** people need to learn in vocational education and **how** they learn.

| Trend | What it means for TVET |
| --- | --- |
| Automation of routine tasks | Job profiles change; more monitoring, troubleshooting and problem-solving |
| AI as a work tool | Skilled workers use AI assistants (diagnosis, documentation, planning) and need to evaluate outputs |
| Shorter half-life of skills | Lifelong learning, modular upskilling, micro-credentials |
| Human and transversal skills | Communication, critical thinking, collaboration become more important |
| Green and digital transition | New qualifications combine technical, digital and sustainability skills |
| Personalised learning | Adaptive systems, AI tutors, immersive training (VR/AR) |

The World Economic Forum's *Future of Jobs Report 2025* names AI and big data, networks and cybersecurity, and technological literacy as the fastest-growing skills – together with creative thinking, resilience and lifelong learning.

**Reflection:** Choose a vocational field you know (e.g. automotive, care, logistics). Which tasks will AI change in the next five years? Which tasks remain human? Note 3 points in your AI tools log.

## 6. Start Your AI Tools Log

Throughout the seminar you document **every** relevant AI use. This log is part of component 4 of the final assessment.

| Date | Tool (model) | Purpose | Prompt (short) | Output (short) | My evaluation | What I kept / changed |
| --- | --- | --- | --- | --- | --- | --- |
| 15.10. | e.g. ChatGPT (GPT-…) | Explain tokens to apprentices | "You are a trainer …" | 3 analogies | 2 good, 1 misleading | Kept analogy 1, rewrote 2 |

**Rules**

- Name the exact tool and model.
- Verify facts and references against primary sources.
- Never enter personal data of learners or colleagues into AI tools.

**Task for today:** Create your log (Word, Excel or Markdown) and add your first entry from the practice in section 3.

## Summary

- AI is a family of approaches; generative AI is the newest and most visible part.
- LLMs predict probable tokens – their output must be checked.
- Good prompts combine Role · Task · Context · Format · Examples and are refined iteratively.
- UNESCO frameworks (Students, Teachers) and the EU AI Act set the frame for AI in education.
- **Next:** 22.10.2026 · 🔵 Self-learning unit S02 · Hand-in by 28.10.2026, 23:59.

## References

- European Union. (2024). *Regulation (EU) 2024/1689 laying down harmonised rules on artificial intelligence (Artificial Intelligence Act)*. Official Journal of the European Union. https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- Lo, L. S. (2023). The CLEAR path: A framework for enhancing information literacy through prompt engineering. *The Journal of Academic Librarianship, 49*(4), 102720. https://doi.org/10.1016/j.acalib.2023.102720
- UNESCO. (2018). *UNESCO ICT competency framework for teachers* (Version 3). UNESCO. https://unesdoc.unesco.org/ark:/48223/pf0000265721
- UNESCO. (2023). *Guidance for generative AI in education and research*. UNESCO. https://doi.org/10.54675/EWZM9535
- UNESCO. (2024a). *AI competency framework for students*. UNESCO. https://doi.org/10.54675/JKJB9835
- UNESCO. (2024b). *AI competency framework for teachers*. UNESCO. https://doi.org/10.54675/ZJTE2084
- World Economic Forum. (2025). *The future of jobs report 2025*. https://www.weforum.org/publications/the-future-of-jobs-report-2025/

<small>Licence: CC BY 4.0 · Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), checked and revised by the author.</small>
