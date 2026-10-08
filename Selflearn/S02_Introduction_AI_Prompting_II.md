<!--
author:    Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Textbook

title:     S02 – Introduction to AI & Prompting II: tools, limitations, ethics (Self-learning unit)
comment:   AI in TVET I – Self-learning unit for session 2 (22.10.2026): AI tools and prompt patterns, limitations of generative AI, human-centred mindset and ethics of AI in education.
-->

# S02 – Introduction to AI & Prompting II

> **Session 2 · 22.10.2026 · 🔵 Self-learning** – I am travelling; work through this unit on your own.
>
> **Time needed:** about 2.5–3 hours
>
> **Hand-in (Moodle): 28.10.2026, 23:59** – see the last chapter.

**After this unit you will be able to …**

1. choose suitable AI tools for discussion, research and content creation,
2. apply prompt patterns to TVET tasks,
3. recognise typical limitations of generative AI and verify AI output,
4. explain the human-centred mindset and key ethical risks of AI in education,
5. relate these risks to the EU AI Act and the UNESCO AI Competency Framework for Teachers.

## 1. Choosing the Right Tool

Different tools are built for different jobs. Use the tool that fits your task – and document it in your AI tools log.

| Purpose | Tools (examples) | Strength | Watch out |
| --- | --- | --- | --- |
| Discussion, drafting, structuring | ChatGPT, Claude, Gemini, Copilot | Flexible, good at language and structure | Can invent facts and references |
| Research with sources | Perplexity, Consensus, Elicit | Show sources; Consensus searches peer-reviewed papers | Read the sources yourself – summaries can be wrong |
| Working with your own documents | NotebookLM, file upload in chat tools | Answers grounded in your material | Only as good as the documents; data protection |
| Images and diagrams | Image generators, diagram tools (e.g. Mermaid code from an LLM) | Fast visuals | Licences, technical accuracy, stereotypes |
| Content for LiaScript | Any LLM + the LiaScript template | Generates Markdown directly | Test the syntax in the LiveEditor |

**Data protection first:** Check which account you use (university licence vs. private account) and never upload personal data of learners.

**Check:** You need three peer-reviewed studies on AI-supported welding training. Which tool fits best as a starting point?

- [( )] An image generator
- [(X)] A research tool such as Consensus or Elicit – followed by reading the papers yourself
- [( )] A chatbot without web access, asked to "list three studies"

## 2. Prompt Patterns for TVET

Prompt patterns are reusable solutions for frequent prompting problems (White et al., 2023).

| Pattern | Template | TVET example |
| --- | --- | --- |
| **Persona** | "Act as …" | "Act as an experienced master craftsman in plumbing." |
| **Audience persona** | "Explain to …" | "Explain to apprentices with German level B1." |
| **Template** | "Use exactly this format: …" | "Fill in this lesson-plan table: phase · time · activity · media." |
| **Flipped interaction** | "Ask me questions until you have enough information to …" | "… design a workshop safety briefing for my group." |
| **Question refinement** | "Suggest a better version of my question." | Improves vague research questions |
| **Cognitive verifier** | "Split the question into sub-questions, answer them, then combine." | Troubleshooting a hydraulic system step by step |
| **Reflection / fact check** | "List the facts in your answer that I should verify." | Before using an answer in teaching material |

**Practice (15 min):** Use the *flipped interaction* pattern to let an AI tool interview you about a lesson you want to plan. Then use the *fact check* pattern on its final suggestion. Document both in your log.

## 3. Limitations of Generative AI

{{1}}
<section>

| Limitation | What happens | What you do |
| --- | --- | --- |
| **Hallucinations** | Fluent but false statements | Verify key facts in primary sources |
| **Fabricated references** | Plausible titles, authors, DOIs that do not exist or do not match | Check each reference via DOI, Google Scholar or the library catalogue |
| **Outdated knowledge** | Training cut-off; regulations change | Ask for dates; check current standards and laws |
| **Bias** | Stereotypes from training data (e.g. gender in trades) | Ask for diverse examples; review critically |
| **Missing local context** | Answers fit the US or UK, not your country's TVET system | Give context; compare with national regulations |
| **Didactically weak output** | Text is correct but not suitable for learning | Apply your pedagogical expertise |

</section>

### Exercise: Check a reference

Ask an AI tool *without web search* for "three peer-reviewed articles on AI in vocational education with DOI". Then check each one:

1. Copy the DOI into `https://doi.org/<DOI>` – does it resolve?
2. Do title, authors, journal and year match?
3. Does the paper really say what the AI claims?

Record the result in your log: How many references were correct?

**Check:** An AI tool gives you a reference with a DOI that resolves to a different paper. What is the correct action?

- [( )] Keep the reference, the DOI is probably just a typo.
- [(X)] Do not use it until you have found and read the actual source.
- [( )] Replace the DOI with one from a similar paper.

## 4. The Human-Centred Mindset

The UNESCO AI Competency Framework for Teachers starts with the **human-centred mindset**: AI should support, not replace, human judgement and responsibility.

{{1}}
<section>

**Three elements (UNESCO, 2024b)**

1. **Human agency** – teachers and learners keep control over decisions about teaching and learning.
2. **Human accountability** – responsibility for decisions stays with humans, not with the tool.
3. **Social responsibility** – AI is used for inclusive, fair and sustainable education.

</section>

### Human agency: enabler or threat?

| AI as enabler | AI as threat |
| --- | --- |
| Less administrative work, more time for mentoring | De-professionalisation: teacher becomes a "tool operator" |
| Personalised material for heterogeneous groups | Pedagogical decisions shaped by tool defaults and metrics |
| Instant feedback for learners | Over-reliance; weaker critical thinking |

Research on human-centred learning analytics shows that involving teachers and learners in the design of AI tools is still the exception (Alfredo et al., 2024).

**Reflection:** Where in your future teaching would you *never* hand a decision to an AI tool? Write 2–3 sentences in your log.

## 5. Ethics of AI in Education

### 5.1 Algorithmic bias

``` ascii
 Historical data ──► Model learns ──► Biased ──► Unequal
 with inequalities    the pattern    predictions   opportunities
       ▲                                              │
       └──────────── data from the next cohort ◄──────┘
```

Example: A model trained on past admission data in male-dominated trades may rate female applicants lower. Studies on student progress monitoring show that such models can produce systematically different error rates for groups of learners (Idowu et al., 2024).

### 5.2 Privacy and the EU AI Act

Learning analytics collect large amounts of learner data. The EU AI Act classifies AI systems that **determine access or admission**, **evaluate learning outcomes**, **steer the learning process** or **monitor prohibited behaviour during tests** as **high risk** (Annex III). Providers and deployers must ensure, among other things:

- a risk management system,
- data governance (relevant, representative training data),
- technical documentation and logging,
- transparency towards users,
- **human oversight**,
- accuracy, robustness and cybersecurity.

### 5.3 Accountability in grading

Studies comparing human and LLM grading of the same exams find that AI grades can deviate considerably from teacher grades (Flodén, 2025). Students' acceptance of AI grading depends on whether they perceive it as fair (Jones-Jang et al., 2025). **The final grading decision remains with the teacher.**

### 5.4 Inclusion and the digital divide

AI can help (translation, text simplification, assistive technologies) – or widen gaps (paid tools, missing devices, low AI literacy, languages that models handle poorly).

### 5.5 Sustainability

Training and using large models consumes energy and water. Ask: Is AI necessary for this task, or is a simpler tool enough?

**Check:** Which measures does the EU AI Act require for high-risk AI in education? (several answers)

- [[X]] Human oversight
- [[X]] Data governance for training data
- [[ ]] Free access for all learners
- [[X]] Technical documentation
- [[ ]] Use of open-source models only

## 6. Case Discussion

> A vocational school introduces an AI tool that predicts which first-year apprentices are likely to drop out. Teachers receive a red/amber/green list every month.

Answer in your log:

1. Which risk level under the EU AI Act might apply, and why?
2. Which data could lead to biased predictions?
3. Which decisions must stay with the teachers?
4. What should learners be told about the system?

<details>
<summary>Possible points</summary>

- If the system steers access to support or influences decisions on learners' educational path, a high-risk classification is likely – check Annex III and the exemptions in Art. 6.
- Bias sources: socio-economic background, migration history, previous school grades, absence data due to illness or care duties.
- Teachers decide on interventions; the list is only an indication.
- Transparency: purpose, data used, right to talk to a human, how to contest.

</details>

## 7. Hand-in for Session 2

**Deadline: 28.10.2026, 23:59 · Moodle**

Upload one PDF with:

1. **AI tools log** with at least **3 entries** from this unit (e.g. tool choice, prompt pattern, reference check).
2. **Reference check result** (section 3): number of correct / incorrect references and what you learned.
3. **Case discussion** (section 6): answers to the four questions (max. 1 page).

Open questions are discussed at the start of the next live session on 05.11.2026.

## References

- Alfredo, R., Echeverria, V., Jin, Y., Yan, L., Swiecki, Z., Gašević, D., & Martinez-Maldonado, R. (2024). Human-centred learning analytics and AI in education: A systematic literature review. *Computers and Education: Artificial Intelligence, 6*, 100215. https://doi.org/10.1016/j.caeai.2024.100215
- European Union. (2024). *Regulation (EU) 2024/1689 (Artificial Intelligence Act)*. https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- Flodén, J. (2025). Grading exams using large language models: A comparison between human and AI grading of exams in higher education using ChatGPT. *British Educational Research Journal, 51*(1), 201–224. https://doi.org/10.1002/berj.4069
- Idowu, J. A., Koshiyama, A. S., & Treleaven, P. (2024). Investigating algorithmic bias in student progress monitoring. *Computers and Education: Artificial Intelligence, 7*, 100267. https://doi.org/10.1016/j.caeai.2024.100267
- Jones-Jang, S. M., Chung, M., Choi, J., Kim, N., & Lee, S. (2025). Fairness perceptions of AI in grading systems. *Computers and Education: Artificial Intelligence, 8*, 100419. https://doi.org/10.1016/j.caeai.2025.100419
- UNESCO. (2023). *Guidance for generative AI in education and research*. https://doi.org/10.54675/EWZM9535
- UNESCO. (2024b). *AI competency framework for teachers*. https://doi.org/10.54675/ZJTE2084
- White, J., Fu, Q., Hays, S., Sandborn, M., Olea, C., Gilbert, H., Elnashar, A., Spencer-Smith, J., & Schmidt, D. C. (2023). *A prompt pattern catalog to enhance prompt engineering with ChatGPT* (arXiv:2302.11382). https://arxiv.org/abs/2302.11382

<small>Licence: CC BY 4.0 · Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), checked and revised by the author.</small>
