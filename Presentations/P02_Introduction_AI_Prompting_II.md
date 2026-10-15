<!--
author:    Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Presentation
classroom: enable

title:     P02 – Introduction to AI & Prompting II: tools, limitations, ethics (Session slides)
comment:   AI in TVET I – Slides for session 2 (self-learning, 22.10.2026): choosing AI tools, prompt patterns, limitations of generative AI, human-centred mindset, bias, EU AI Act, accountability in grading. Interactive: prompt-pattern roulette, reference detective, control/automation map, bias games.
tags:      AI, TVET, Prompt patterns, Hallucination, Bias, Ethics, EU AI Act, UNESCO
-->

# Introduction to AI & Prompting II

**Session 2 · 22.10.2026 · 🔵 Self-learning** · AI in TVET I, OVGU Magdeburg

Tools · limitations · human-centred mindset · ethics

<small>Work through these slides together with the self-learning unit [S02 – Introduction to AI & Prompting II](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/Selflearn/S02_Introduction_AI_Prompting_II.md). **Hand-in: 28.10.2026, 23:59 (Moodle).**</small>

                --{{0}}--
Hello and welcome to session two. I am travelling today, so these slides are your guide. They are full of small experiments and games. Do them, write your observations into your AI tools log, and the hand-in will almost write itself.

## Your Route Today 🗺️

``` ascii
 1 Pick the     2 Prompt      3 Catch the    4 Human in     5 Ethics       6 Case &
   right tool ─► patterns  ─►  hallucination ─► control   ─►  arcade    ─►  hand-in
   (10 min)      (20 min)     (25 min)       (20 min)      (45 min)      (40 min)
```

{{1}}
<section>

**After today you can …** choose suitable AI tools · apply prompt patterns · verify AI output · explain the human-centred mindset · relate ethical risks to the EU AI Act and the UNESCO AI CFT for Teachers.

</section>

## 1. Choosing the Right Tool

| Purpose | Tools (examples) | Strength | Watch out |
| --- | --- | --- | --- |
| Discussion, drafting | ChatGPT, Claude, Gemini, Copilot | Flexible with language & structure | Invents facts and references |
| Research with sources | Perplexity, Consensus, Elicit | Show sources, peer-reviewed papers | Read the sources yourself |
| Your own documents | NotebookLM, file upload | Grounded in your material | Only as good as the documents; data protection |
| Images & diagrams | Image generators, Mermaid via LLM | Fast visuals | Licences, accuracy, stereotypes |
| LiaScript content | Any LLM + template | Markdown directly | Test in the LiveEditor |

{{1}}
<section>

🔐 **Data protection first:** university licence vs. private account – and never upload personal data of learners.

</section>

## Game: Tool Match 🎯

Drag the best starting tool into each gap.

You need three peer-reviewed studies on AI-supported welding training → [->[Image generator|(Consensus or Elicit)|Chatbot without web access]]

You want answers based **only** on your own training regulation PDF → [->[(NotebookLM)|Perplexity|Image generator]]

You want a first draft of a LiaScript nugget → [->[Consensus|(LLM + LiaScript template)|Spell checker]]

                --{{0}}--
Remember the rule: research tools give you a starting point, but you still read the papers. A chatbot without web access asked to list three studies is the classic way to collect fabricated references.

## 2. Prompt Patterns 🧩

Reusable solutions for frequent prompting problems (White et al., 2023).

| Pattern | Template |
| --- | --- |
| **Persona** | "Act as …" |
| **Audience persona** | "Explain to …" |
| **Template** | "Use exactly this format: …" |
| **Flipped interaction** | "Ask me questions until you have enough information to …" |
| **Question refinement** | "Suggest a better version of my question." |
| **Cognitive verifier** | "Split the question into sub-questions, answer them, then combine." |
| **Reflection / fact check** | "List the facts in your answer that I should verify." |

## Playground: Prompt-Pattern Roulette 🎡

Choose a pattern and your vocational field – get a ready-to-paste prompt.

**Pattern:** <script input="select" value="Flipped interaction" options="Persona|Audience persona|Template|Flipped interaction|Question refinement|Cognitive verifier|Fact check" output="pat">@input</script>

**Vocational field:** <script input="text" value="mechatronics" output="field" input-always-active>@input</script>

<script modify="false" style="display:block">
const p = "@input(`pat`)";
const f = `@input(`field`)`.replace(/</g,"&lt;") || "my vocational field";
const lib = {
  "Persona": `Act as an experienced master craftsperson in ${f}. Review my lesson plan for a first-year group and tell me what an expert from the workshop would change.`,
  "Audience persona": `Explain the term "feedback loop" to apprentices in ${f} with German language level B1. Use one example from their daily work and max. 120 words.`,
  "Template": `Fill in this lesson-plan table for a 90-minute lesson in ${f}: phase | time | activity | media | learning objective. Do not add other columns.`,
  "Flipped interaction": `I want to design a workshop safety briefing for my apprentices in ${f}. Ask me questions one at a time until you have enough information. Then propose the briefing.`,
  "Question refinement": `Whenever I ask a question about AI in ${f} training, suggest a better, more precise version of my question first. My question: "Is AI good for apprentices?"`,
  "Cognitive verifier": `A machine in a ${f} workshop stops unexpectedly. Split the troubleshooting into sub-questions, answer each one, then combine them into a step-by-step diagnosis.`,
  "Fact check": `At the end of your answer about safety rules in ${f}, list every fact, number and regulation you mentioned that I should verify in a primary source.`
};
`HTML: <div style="border-left:6px solid #16a34a;padding:8px 12px;font-family:monospace">${lib[p] || ""}</div>`
</script>

✍️ **Practice (15 min):** use *flipped interaction* to plan a lesson, then *fact check* the final suggestion. Log both.

                --{{0}}--
Spin the roulette a few times. Notice how each pattern solves a different problem: the flipped interaction makes the AI ask you, the cognitive verifier slows it down, and the fact check reminds both of you that the answer must be verified.

## 3. Limitations of Generative AI ⚠️

| Limitation | What happens | What you do |
| --- | --- | --- |
| **Hallucinations** | Fluent but false statements | Verify key facts in primary sources |
| **Fabricated references** | Plausible titles, authors, DOIs that don't exist | Check via DOI, Google Scholar, library |
| **Outdated knowledge** | Training cut-off; regulations change | Ask for dates; check current standards |
| **Bias** | Stereotypes from training data | Ask for diverse examples; review critically |
| **Missing local context** | Answers fit the US/UK, not your TVET system | Give context; compare with national rules |
| **Didactically weak output** | Correct but not good for learning | Apply your pedagogical expertise |

## Game: Reference Detective 🕵️

An AI tool without web search produced these three references. **Which one is fabricated?**

- [( )] Flodén, J. (2025). Grading exams using large language models … *British Educational Research Journal, 51*(1), 201–224. doi:10.1002/berj.4069
- [(X)] Müller, K. (2023). AI tutors double apprenticeship completion rates. *Journal of Vocational AI, 12*(3), 45–67. doi:10.0000/jvai.2023.045
- [( )] Idowu, J. A., Koshiyama, A. S., & Treleaven, P. (2024). Investigating algorithmic bias in student progress monitoring. *Computers and Education: Artificial Intelligence, 7*, 100267.
[[?]] Paste each DOI into `https://doi.org/<DOI>` – does it resolve? Does the journal exist?
****************************************

The Müller reference was invented **for this exercise**: the journal does not exist and the DOI does not resolve. Notice how "plausible" it looked – a round, impressive claim, a realistic volume and page range.

****************************************

{{1}}
<section>

🔎 **Your turn:** ask a chatbot *without web search* for "three peer-reviewed articles on AI in vocational education with DOI". Check every one: DOI resolves? Metadata match? Does the paper say what the AI claims? → **hand-in item 2**

</section>

## Game: Real or Generated? 👀

Generative AI does not only invent references – it invents faces.

??[Which Face Is Real? (University of Washington)](https://www.whichfaceisreal.com)

How many out of 10 did you get right?

- [(0)] 0–3
- [(4)] 4–6
- [(7)] 7–8
- [(9)] 9–10

                --{{0}}--
Play ten rounds. Then think about what this means for images in learning material, and for trust in photos as evidence.

## 4. The Human-Centred Mindset 🧑‍🔧

UNESCO AI CFT for Teachers: AI should **support, not replace**, human judgement.

{{1}}
<section>

1. **Human agency** – teachers and learners keep control over teaching and learning decisions
2. **Human accountability** – responsibility stays with humans, not with the tool
3. **Social responsibility** – AI for inclusive, fair and sustainable education

</section>

{{2}}
<section>

| AI as enabler | AI as threat |
| --- | --- |
| Less admin, more time for mentoring | De-professionalisation: teacher as "tool operator" |
| Personalised material for mixed groups | Decisions shaped by tool defaults and metrics |
| Instant feedback | Over-reliance; weaker critical thinking |

</section>

## Teacher–AI Complementarity

UNESCO Teacher Task Force (2025): teaching **with** AI · teaching **about** AI · **adapting** teaching to a world full of AI.

**Hand over to AI – or keep under human control?**

- [[Hand over (with checks)] [Keep human]]
- [           (X)                ( )    ]  First draft of practice exercises
- [           ( )                (X)    ]  Feedback that needs empathy and knowledge of the learner
- [           (X)                ( )    ]  Routine formatting of a worksheet
- [           ( )                (X)    ]  Decision about a learner's path
- [           (X)                ( )    ]  Filtering information for a lesson
- [           ( )                (X)    ]  Value judgements in a conflict between apprentices

{{1}}
<section>

Deciding *what* to offload is itself a skill – teachers need **metacognitive awareness** to keep their agency.

</section>

## Playground: Human Control × Automation 🎛️

Shneiderman's idea, used by Alfredo et al. (2024): control and automation are **not opposites**. Place an AI tool you know.

**Tool:** <script input="text" value="AI grading assistant" output="hctool" input-always-active>@input</script>

Human control: <script input="range" min="0" max="10" step="1" value="3" output="hc">@input</script>

Computer automation: <script input="range" min="0" max="10" step="1" value="8" output="ca">@input</script>

<script modify="false" style="display:block">
const c = Number(@input(`hc`)), a = Number(@input(`ca`));
const name = `@input(`hctool`)`.replace(/</g,"&lt;");
const x = 30 + c * 26, y = 290 - a * 26;
let q, msg;
if (c >= 5 && a >= 5) { q = "Q4 – high control + high automation"; msg = "The target zone: the system does a lot, but humans can steer, override and understand it."; }
else if (c < 5 && a >= 5) { q = "Q3 – the system decides"; msg = "Watch out: automation bias and lost agency. Who checks? Can learners contest the result?"; }
else if (c >= 5 && a < 5) { q = "Q2 – the user configures"; msg = "Humans are in charge, but the tool takes little work off their hands."; }
else { q = "Q1 – shows information"; msg = "A simple dashboard: low effort for the system, low control for the user."; }
`HTML: <div style="display:flex;flex-wrap:wrap;gap:16px;align-items:center">
<svg viewBox="0 0 320 320" style="width:300px;max-width:100%">
<rect x="30" y="30" width="130" height="130" fill="#fee2e2"/><rect x="160" y="30" width="130" height="130" fill="#dcfce7"/>
<rect x="30" y="160" width="130" height="130" fill="#f1f5f9"/><rect x="160" y="160" width="130" height="130" fill="#e0f2fe"/>
<text x="95" y="50" font-size="11" text-anchor="middle" fill="#111">Q3 system decides</text><text x="225" y="50" font-size="11" text-anchor="middle" fill="#111">Q4 high + high</text>
<text x="95" y="280" font-size="11" text-anchor="middle" fill="#111">Q1 show info</text><text x="225" y="280" font-size="11" text-anchor="middle" fill="#111">Q2 user configures</text>
<line x1="30" y1="290" x2="300" y2="290" stroke="currentColor"/><line x1="30" y1="290" x2="30" y2="20" stroke="currentColor"/>
<text x="165" y="312" font-size="11" text-anchor="middle" fill="currentColor">human control →</text>
<text x="14" y="160" font-size="11" text-anchor="middle" fill="currentColor" transform="rotate(-90 14 160)">automation →</text>
<circle cx="${x}" cy="${y}" r="9" fill="#2563eb"/></svg>
<div style="flex:1;min-width:220px"><p><b>${name}</b> → <b>${q}</b></p><p>${msg}</p></div></div>`
</script>

                --{{0}}--
Place a tool and move the sliders. The review by Alfredo and colleagues found some attention to human control in system design, but very little involvement of end users, especially students, in the design process.

## 5. Ethics Arcade 🕹️

Four short games – each one makes an ethical risk tangible.

| Game | Risk you experience | Time |
| --- | --- | --- |
| [Survival of the Best Fit](https://survivalofthebestfit.com) | How a hiring AI learns bias from your own decisions | 10 min |
| [PAIR: Measuring Fairness](https://pair.withgoogle.com/explorables/measuring-fairness/) | Why "fair" has several, conflicting definitions | 10 min |
| [Stable Bias Explorer (Hugging Face)](https://huggingface.co/spaces/society-ethics/DiffusionBiasExplorer) | Which faces image generators produce for professions | 10 min |
| [AI Incident Database](https://incidentdatabase.ai) | Real failures of AI systems – search "education" or "grading" | 10 min |

{{1}}
<section>

📓 After each game, write **one sentence** in your log: *"This shows that … – in TVET this could mean …"*

</section>

## Play: Survival of the Best Fit 🏢

??[Survival of the Best Fit – a game about hiring bias](https://survivalofthebestfit.com)

                --{{0}}--
You run a fast-growing company and hire people. At some point an algorithm takes over, trained on your earlier decisions. Watch what it learns.

## 5.1 Algorithmic Bias

``` ascii
 Historical data ──► Model learns ──► Biased ──► Unequal
 with inequalities    the pattern    predictions   opportunities
       ▲                                              │
       └──────────── data from the next cohort ◄──────┘
```

{{1}}
<section>

- Bias enters via **data collection, algorithm design, implementation and policy** (Boateng & Boateng, 2025)
- In student progress monitoring, **institutional data** contributed most to discrimination, **assessment data** least – and mitigation reached fairness *without* losing accuracy (Idowu et al., 2024)
- **Individual** vs. **group fairness** can conflict (Idowu et al., 2024)
- **Liberatory design** brings under-represented communities into EdTech design (Gaskins, 2023)

</section>

## Your Call: Which Data Would You Exclude?

An apprenticeship dropout model could use these features. **Which would you exclude?** (select all you would exclude)

- [[school-leaving certificate]] School-leaving certificate
- [[absences]] Absences
- [[migration]] Migration history
- [[company size]] Size of the training company
- [[gender]] Gender
- [[practical grades]] Grades in practical tasks

**Why?** One sentence:

[[___ ___]]

                --{{0}}--
There is no single right answer. But every exclusion and every inclusion is a value decision. Absences, for example, can reflect illness or care duties, not motivation.

## 5.2 Privacy and the EU AI Act

**High risk** in education (Annex III): systems that **determine access or admission**, **evaluate learning outcomes**, **steer the learning process**, or **monitor prohibited behaviour during tests**.

{{1}}
<section>

Obligations include: risk management · data governance · technical documentation & logging · transparency · **human oversight** · accuracy, robustness, cybersecurity

</section>

{{2}}
<section>

**Critical view (Kusche, 2024):** fundamental rights appear as legal rules, values *and* the basis of "trustworthy AI" → the line between high and low risk is partly **political**. *For schools: compliance is the minimum; pedagogical judgement remains necessary.*

</section>

**Check:** Which measures does the AI Act require for high-risk AI in education?

- [[X]] Human oversight
- [[X]] Data governance for training data
- [[ ]] Free access for all learners
- [[X]] Technical documentation
- [[ ]] Use of open-source models only

## 5.3 Would You Let an AI Grade You? 📝

**Before you read on – vote honestly:**

- [(human)] I prefer a human grader
- [(ai)] I prefer an AI grader
- [(mix)] AI suggests, human decides
- [(dontcare)] I don't care

{{1}}
<section>

- AI grades can **deviate considerably** from teacher grades (Flodén, 2025)
- 228 students: most preferred **human** graders; dissatisfied students and those with low grades were more open to AI – acceptance follows fairness *and* self-interest (Jones-Jang et al., 2025)
- 33 teachers: grading GenAI-assisted work involves **value judgements** about the student, and judgements varied a lot → transparency needed (Luo & Dawson, 2025)

</section>

{{2}}
<section>

⚖️ **The final grading decision stays with the teacher – and the rules must be known in advance.** That's why you declare your AI use in this seminar.

</section>

## 5.4–5.6 Inclusion, Sustainability, Well-being

{{1}}
<section>

🌍 **Inclusion:** translation, simplification, assistive tech – *or* wider gaps through paid tools, devices, low AI literacy, poorly handled languages

</section>

{{2}}
<section>

🔋 **Sustainability:** training and using large models consumes energy and water. *Is AI necessary for this task?*

</section>

{{3}}
<section>

🤝 **Well-being:** ten intertwined concerns, from human connection to AI-generated content (Al-Zahrani, 2024) · teacher responsibility linked to student well-being, stronger with **peer collaboration** (Li et al., 2025) · educators in applied education ask for training, policies, ethical frameworks (Shahzad et al., 2025)

</section>

**Which concern worries you most for TVET?**

- [(connection)] Loss of human connection
- [(privacy)] Data privacy
- [(bias)] Algorithmic bias
- [(thinking)] Weaker critical thinking
- [(equity)] Access equity
- [(energy)] Energy & sustainability

## 6. Case: The Dropout Traffic Light 🚦

> A vocational school introduces an AI tool that predicts which first-year apprentices are likely to drop out. Teachers receive a **red/amber/green list** every month.

**1. Which risk level under the EU AI Act might apply?**

- [(minimal)] Minimal
- [(limited)] Limited
- [(high)] High
- [(prohibited)] Prohibited

{{1}}
<section>

**2.** Which data could lead to biased predictions? · **3.** Which decisions must stay with teachers? · **4.** What should learners be told?

<details>
<summary>Possible points</summary>

- If the system steers access to support or influences a learner's path, **high risk** is likely – check Annex III and the exemptions in Art. 6.
- Bias sources: socio-economic background, migration history, previous grades, absences due to illness or care duties.
- Teachers decide on interventions; the list is only an indication.
- Transparency: purpose, data used, right to talk to a human, how to contest.

</details>

</section>

## Hand-in for Session 2 📤

**Deadline: 28.10.2026, 23:59 · Moodle · one PDF**

{{1}}
<section>

1. **AI tools log** with at least **3 entries** (tool choice, prompt pattern, reference check …)
2. **Reference check result**: number of correct / incorrect references + what you learned
3. **Case discussion**: answers to the four questions (max. 1 page)

</section>

{{2}}
<section>

💬 Open questions → start of the live session on **05.11.2026**.

**How confident do you feel about today's topics?**

- [(1)] 😟 Lost
- [(2)] 🙂 Okay
- [(3)] 😎 Ready to teach it

</section>

## References

- Al-Zahrani, A. M. (2024). Unveiling the shadows: Beyond the hype of AI in education. *Heliyon, 10*, e30696. https://doi.org/10.1016/j.heliyon.2024.e30696
- Alfredo, R., Echeverria, V., Jin, Y., Yan, L., Swiecki, Z., Gašević, D., & Martinez-Maldonado, R. (2024). Human-centred learning analytics and AI in education: A systematic literature review. *Computers and Education: Artificial Intelligence, 6*, 100215. https://doi.org/10.1016/j.caeai.2024.100215
- Boateng, O., & Boateng, B. (2025). Algorithmic bias in educational systems. *World Journal of Advanced Research and Reviews, 25*(1), 2012–2017. https://doi.org/10.30574/wjarr.2025.25.1.0253
- European Union. (2024). *Regulation (EU) 2024/1689 (Artificial Intelligence Act)*. https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- Flodén, J. (2025). Grading exams using large language models. *British Educational Research Journal, 51*(1), 201–224. https://doi.org/10.1002/berj.4069
- Gaskins, N. (2023). Interrogating algorithmic bias: From speculative fiction to liberatory design. *TechTrends, 67*, 417–425. https://doi.org/10.1007/s11528-022-00783-0
- Idowu, J. A., Koshiyama, A. S., & Treleaven, P. (2024). Investigating algorithmic bias in student progress monitoring. *Computers and Education: Artificial Intelligence, 7*, 100267. https://doi.org/10.1016/j.caeai.2024.100267
- Jones-Jang, S. M., Chung, M., Choi, J., Kim, N., & Lee, S. (2025). Fairness perceptions of AI in grading systems. *Computers and Education: Artificial Intelligence, 8*, 100419. https://doi.org/10.1016/j.caeai.2025.100419
- Kusche, I. (2024). Possible harms of artificial intelligence and the EU AI act: Fundamental rights and risk. *Journal of Risk Research*. https://doi.org/10.1080/13669877.2024.2350720
- Li, H., Zhang, J., Khan, W. A., & Lamsali, H. (2025). Teacher responsibility, AI integration, and student well-being. *Acta Psychologica, 260*, 105532. https://doi.org/10.1016/j.actpsy.2025.105532
- Luo, J., & Dawson, P. (2025). Exploring value judgements in grading. *Studies in Higher Education*. https://doi.org/10.1080/03075079.2025.2552825
- Shahzad, F., Avunduk, Z. B., Ullah, Z., & Arslan, A. (2025). Understanding management educators' perspectives on AI adoption. *The International Journal of Management Education, 23*, 101274. https://doi.org/10.1016/j.ijme.2025.101274
- Teacher Task Force. (2025). *Promoting and protecting teacher agency in the age of artificial intelligence* [Position paper]. UNESCO.
- UNESCO. (2024b). *AI competency framework for teachers*. https://doi.org/10.54675/ZJTE2084
- White, J., Fu, Q., Hays, S., et al. (2023). *A prompt pattern catalog to enhance prompt engineering with ChatGPT* (arXiv:2302.11382). https://arxiv.org/abs/2302.11382

**Interactive tools:** [Which Face Is Real?](https://www.whichfaceisreal.com) · [Survival of the Best Fit](https://survivalofthebestfit.com) · [PAIR Explorables](https://pair.withgoogle.com/explorables/) · [Stable Bias Explorer](https://huggingface.co/spaces/society-ethics/DiffusionBiasExplorer) · [AI Incident Database](https://incidentdatabase.ai)

<small>Licence: CC BY 4.0 · Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), based on the self-learning unit S02; checked by the author.</small>
