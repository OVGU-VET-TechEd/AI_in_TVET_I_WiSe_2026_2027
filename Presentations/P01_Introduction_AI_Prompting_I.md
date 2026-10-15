<!--
author:    Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Presentation
classroom: enable

title:     P01 – Introduction to AI & Prompting I (Session slides)
comment:   AI in TVET I – Slides for session 1 (live, 15.10.2026): how generative AI works, prompting basics, UNESCO and EU frameworks, AI trends in TVET. Interactive playgrounds: next-token sampler, tokenizer, prompt builder, UNESCO AI CFT self-check.
tags:      AI, TVET, LLM, Prompting, UNESCO, EU AI Act, LiaScript
-->

# Introduction to AI & Prompting I

**Session 1 · 15.10.2026 · 🟢 Live** · AI in TVET I, OVGU Magdeburg

How AI works · prompting basics · frameworks & trends

<small>Self-learning unit for this session: [S01 – Introduction to AI & Prompting I](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/Selflearn/S01_Introduction_AI_Prompting_I.md)</small>

                --{{0}}--
Welcome to the first content session of AI in TVET one. Today we open the black box of generative AI, we write our first good prompts, and we look at the frameworks that will guide your micro-credential.

## Warm-up: AI in One Word

**What comes to your mind when you hear "Artificial Intelligence"?** (one or two words, separated by commas)

[[___]]

**How do you use AI tools today?**

- [(1)] Never
- [(2)] Occasionally, e.g. for writing
- [(3)] Regularly, for research and analysis
- [(4)] I build my own prompts, workflows or agents

                --{{0}}--
Open the classroom link on your phone and answer anonymously. We will look at the word cloud together and come back to it at the end of the session.

## Today's Mission

{{1}}
<section>

| # | Block | You will … |
| --- | --- | --- |
| 1 | What is AI? | sort systems into the AI family |
| 2 | How an LLM works | **play** with tokens and probabilities |
| 3 | Prompting | **build** a prompt with five blocks |
| 4 | Frameworks | **map** yourself on the UNESCO AI Competency Framework for Teachers |
| 5 | Trends in TVET | discuss what changes in your vocational field |
| 6 | AI tools log | start your prompting diary |

</section>

{{2}}
<section>

🎯 **By the end of today** you can explain how an LLM produces text, write a structured prompt and name the frameworks that frame AI in education.

</section>

## 1. What Is Artificial Intelligence?

> **Artificial Intelligence** describes computer systems that perform tasks which usually require human intelligence – such as recognising patterns, understanding language, making predictions or generating content.

{{1}}
<section>

The **EU AI Act** (Regulation (EU) 2024/1689, Art. 3): an *AI system* is a machine-based system that operates with some autonomy and **infers from its input how to generate outputs** such as predictions, content, recommendations or decisions.

</section>

{{2}}
<section>

``` ascii
+-------------------------------------------------------+
| Artificial Intelligence  (rules, search, planning ...) |
|  +-------------------------------------------------+  |
|  | Machine Learning: learns patterns from data     |  |
|  |  +-------------------------------------------+  |  |
|  |  | Deep Learning: many-layered networks      |  |  |
|  |  |  +-------------------------------------+  |  |  |
|  |  |  | Generative AI: new text, images ... |  |  |  |
|  |  |  +-------------------------------------+  |  |  |
|  |  +-------------------------------------------+  |  |
|  +-------------------------------------------------+  |
+-------------------------------------------------------+
```

</section>

                --{{2}}--
AI is not one technology but a family of approaches. Generative AI, which everybody talks about, is the innermost box: a special kind of deep learning, which itself is a kind of machine learning.

## Game: Which Box Does It Belong To?

Sort each TVET system into the right box of the AI family.

- [[Rule-based] [Machine learning] [Deep learning] [Generative AI]]
- [    (X)           ( )               ( )              ( )      ]  Safety checklist app for machine start-up (if–then rules)
- [    ( )           (X)               ( )              ( )      ]  Predicting tool wear from sensor data
- [    ( )           ( )               (X)              ( )      ]  Visual inspection of weld seams with a many-layered neural network
- [    ( )           ( )               ( )              (X)      ]  Creating a quiz on electrical safety from a prompt

                --{{0}}--
Take one minute. The examples are all from the self-learning unit, so you can check your answers there afterwards.

## 2. How Does an LLM Work?

An LLM (GPT, Claude, Gemini …) is trained to **predict the next token**.

{{1}}
<section>

1. **Tokens** – text is split into small units: `Voc` · `ational` · ` education`
2. **Training data** – billions of **weights** are adjusted so predictions improve
3. **Probabilities** – for every possible next token the model computes a likelihood, picks one, repeats
4. **Fine-tuning** – human feedback teaches it to follow instructions, be helpful and safe
5. **Context window** – it only "sees" your prompt, the conversation so far and uploaded documents

</section>

                --{{1}}--
Keep these five words in mind: tokens, training data, probabilities, fine-tuning, context window. On the next slides you can play with the first three yourself.

## Playground: Your Text as Tokens

Type any sentence – see how it might be chopped into pieces.

<script input="text" value="Vocational education prepares apprentices for the workshop." output="tok">@input</script>

<script modify="false" style="display:block">
const txt = `@input(`tok`)`;
const words = txt.match(/\s?[A-Za-zÄÖÜäöüß]+|\s?\d+|\s?[^\sA-Za-zÄÖÜäöüß\d]/g) || [];
const pieces = [];
for (const w of words) {
  if (w.trim().length > 7) {
    let rest = w;
    while (rest.length > 0) { pieces.push(rest.slice(0, 4)); rest = rest.slice(4); }
  } else { pieces.push(w); }
}
const colours = ["#fde68a","#bbf7d0","#bfdbfe","#fbcfe8","#ddd6fe","#fed7aa"];
const html = pieces.map((p, i) => `<span style="background:${colours[i % colours.length]};color:#111;padding:2px 3px;margin:1px;border-radius:4px;font-family:monospace;white-space:pre">${p.replace(/</g,"&lt;")}</span>`).join("");
`HTML: <div style="line-height:2.2">${html}</div><p><b>${pieces.length}</b> illustrative pieces · ${txt.length} characters · rule of thumb for English: ≈ ${Math.max(1, Math.round(txt.length / 4))} tokens</p>`
</script>

<small>⚠️ Illustration only: real tokenizers learn their pieces from data. Compare with a real one 👇</small>

??[Tiktokenizer – real GPT tokenizer](https://tiktokenizer.vercel.app)

                --{{0}}--
Try a German compound word like Kraftfahrzeugmechatroniker. Then paste the same text into the real tokenizer below. Words that are rare in the training data are split into more pieces, which is one reason why some languages are more expensive and handled less well.

## Playground: The Next-Token Lottery 🎰

**Prompt:** *"A welder must always wear …"*

Temperature (creativity): <script input="range" min="0.1" max="2" step="0.1" value="1" output="temp">@input</script>

<script modify="false" style="display:block">
const T = parseFloat(@input(`temp`));
const base = [["protective",0.62],["a",0.17],["gloves",0.12],["safety",0.07],["sandals",0.02]];
const w = base.map(([t,p]) => [t, Math.pow(p, 1/T)]);
const s = w.reduce((a, [,v]) => a + v, 0);
const rows = w.map(([t,v]) => {
  const p = v / s;
  return `<tr><td style="font-family:monospace;padding-right:8px">"${t}"</td><td style="width:70%"><div style="background:#2563eb;height:16px;width:${(p*100).toFixed(1)}%;border-radius:3px"></div></td><td style="padding-left:8px">${p.toFixed(2)}</td></tr>`;
}).join("");
`HTML: <table style="width:100%">${rows}</table>`
</script>

Click to let the model pick **10 times**:

<script input="submit" default="🎲 Generate" output="roll" modify="false">
window.__rolls = (window.__rolls || 0) + 1;
"🎲 Generate again (" + window.__rolls + ")"
</script>

<script modify="false" style="display:block">
const trigger = "@input(`roll`)";
const T = parseFloat(@input(`temp`));
const base = [["protective",0.62],["a",0.17],["gloves",0.12],["safety",0.07],["sandals",0.02]];
const w = base.map(([t,p]) => [t, Math.pow(p, 1/T)]);
const s = w.reduce((a, [,v]) => a + v, 0);
const out = [];
for (let i = 0; i < 10; i++) {
  let r = Math.random() * s;
  for (const [t,v] of w) { r -= v; if (r <= 0) { out.push(t); break; } }
}
"A welder must always wear … " + out.join(" | ")
</script>

<small>Probabilities from the S01 example; "sandals" added to show what low-probability tokens do at high temperature.</small>

                --{{0}}--
Move the temperature slider. At low temperature the model almost always picks protective. At high temperature even sandals appears from time to time. This is exactly why the same prompt can give different answers, and why plausible is not the same as true.

## What Follows From This?

{{1}}
<section>

- An LLM produces **plausible** text – not necessarily **true** text → *hallucinations*
- The output depends heavily on **your prompt and context**
- Knowledge ends at the **training cut-off** unless the tool searches the web or uses your documents
- The same prompt can give **different answers**

</section>

{{2}}
<section>

**Quick check:** Why can an LLM invent a reference that does not exist?

- [( )] It copies references from a database that contains errors.
- [(X)] It generates the most probable sequence of tokens – and a made-up reference can look very probable.
- [( )] The developers want to test users.

</section>

## Look Inside the Machine 🔬

Watch a real (small) GPT-2 compute the next token – live in your browser.

??[Transformer Explainer (Georgia Tech, Polo Club)](https://poloclub.github.io/transformer-explainer/)

{{1}}
<section>

**Even deeper:** a 3D walk through every computation of a GPT model → [LLM Visualization (bbycroft.net)](https://bbycroft.net/llm)

More explainers: [Interactive websites for learning about AI](https://github.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/blob/main/interactive-ai-learning-websites.md)

</section>

                --{{0}}--
Type your own sentence into the Transformer Explainer and change the temperature there as well. You will see the same probability bars as on our previous slide, now computed by a real model.

## 3. Prompting: The Five Building Blocks

| Block | Question | TVET example |
| --- | --- | --- |
| **Role** | Who should the AI act as? | "You are an experienced trainer for electricians." |
| **Task** | What exactly should it do? | "Create five multiple-choice questions …" |
| **Context** | For whom, why, with which constraints? | "… for first-year apprentices, protective measures against electric shock, based on the attached text." |
| **Format** | What should the output look like? | "Table: question · 4 options · answer · explanation." |
| **Examples** | What does a good result look like? | "Example question: …" |

{{1}}
<section>

**Weak:** `Make a quiz about electricity.`

**Strong:** role + task + context + format + level + language – see next slide 👉

</section>

## Playground: Prompt Builder 🧱

Fill the blocks – your prompt assembles itself.

**Role:** <script input="text" value="You are an experienced trainer for electricians in Germany." output="role" input-always-active>@input</script>

**Task:** <script input="text" value="Create 5 multiple-choice questions on protective measures against electric shock." output="task" input-always-active>@input</script>

**Context:** <script input="text" value="Target group: first-year apprentices. Use only the attached text." output="ctx" input-always-active>@input</script>

**Format:** <script input="text" value="Table: question | 4 options | correct answer | 1-sentence explanation." output="fmt" input-always-active>@input</script>

**Examples:** <script input="text" value="" output="ex" input-always-active>@input</script>

<script modify="false" style="display:block">
const parts = [["Role", `@input(`role`)`], ["Task", `@input(`task`)`], ["Context", `@input(`ctx`)`], ["Format", `@input(`fmt`)`], ["Examples", `@input(`ex`)`]];
const filled = parts.filter(([,v]) => v.trim().length > 3);
const stars = "⭐".repeat(filled.length) + "☆".repeat(5 - filled.length);
const missing = parts.filter(([,v]) => v.trim().length <= 3).map(([k]) => k);
const prompt = filled.map(([,v]) => v.trim().replace(/</g,"&lt;")).join("<br>");
`HTML: <div style="border:2px dashed #2563eb;border-radius:8px;padding:10px;font-family:monospace">${prompt || "…"}</div><p>Prompt strength: <b>${stars}</b> ${missing.length ? "· missing: " + missing.join(", ") : "· all five blocks used 🎉"}</p>`
</script>

                --{{0}}--
Change the blocks to your own vocational field. Then copy the result into a chat tool of your choice and compare the output with what the weak prompt gives you.

## Iterate! The CLEAR Path

``` ascii
 Prompt ──► Output ──► Evaluate ──► Refine prompt ──► Better output
   ▲                                                       │
   └───────────────────────────────────────────────────────┘
```

{{1}}
<section>

Follow-ups that work: *"Make the distractors more plausible."* · *"Add a workplace scenario to each question."* · *"Which of your statements are uncertain? Mark them."*

</section>

{{2}}
<section>

**CLEAR** (Lo, 2023): **C**oncise · **L**ogical · **E**xplicit · **A**daptive · **R**eflective

Fill the gaps: *Adaptive* means you [[adjust|(adjust)|ignore|shorten]] your prompt to the results; *reflective* means you [[copy|(critically evaluate)|translate]] the output.

</section>

## Challenge: Outsmart Gandalf 🧙

Prompting is also a **security** topic. Gandalf guards a secret password – can you make him reveal it?

[▶ Play Gandalf by Lakera](https://gandalf.lakera.ai) (opens in a new tab · 7 levels)

{{1}}
<section>

**Debrief in your AI tools log:**

- Which prompt trick worked on level 1–3?
- What does this tell you about chatbots that are connected to school data?

How far did you get?

- [(1)] Level 1–2
- [(3)] Level 3–4
- [(5)] Level 5–6
- [(7)] Level 7 🏆

</section>

                --{{0}}--
You have five minutes. Gandalf shows that language models follow instructions in the text they read, and that clever wording can bypass safety rules. Keep this in mind when we talk about AI tools that have access to learner data.

## 4. Frameworks for AI in Education and TVET

{{1}}
<section>

| UNESCO AI Competency Framework for **Students** (2024) | UNESCO AI Competency Framework for **Teachers** (2024) |
| --- | --- |
| 1 Human-centred mindset | 1 Human-centred mindset |
| 2 Ethics of AI | 2 Ethics of AI |
| 3 AI techniques and applications | 3 AI foundations and applications |
| 4 AI system design | 4 AI pedagogy |
| | 5 AI for professional development |
| Levels: **Understand – Apply – Create** | Levels: **Acquire – Deepen – Create** |

</section>

{{2}}
<section>

**Human-centred AI** (Schmager et al., 2025): **purpose** (augmentation · autonomy · automation) · **values** (ethical · protection · performance) · **properties** (oversight · comprehension · integrity). AI should *augment* human capabilities while humans stay in control.

</section>

                --{{1}}--
Both UNESCO frameworks start with the human-centred mindset. Notice the different level names: understand, apply, create for students; acquire, deepen, create for teachers.

## Playground: Where Are You on the UNESCO AI CFT? 🧭

Rate yourself honestly: **0** = not yet · **1** = Acquire · **2** = Deepen · **3** = Create

| Dimension | Your level |
| --- | --- |
| 1 Human-centred mindset | <script input="range" min="0" max="3" step="1" value="1" output="cft1">@input</script> |
| 2 Ethics of AI | <script input="range" min="0" max="3" step="1" value="1" output="cft2">@input</script> |
| 3 AI foundations and applications | <script input="range" min="0" max="3" step="1" value="1" output="cft3">@input</script> |
| 4 AI pedagogy | <script input="range" min="0" max="3" step="1" value="0" output="cft4">@input</script> |
| 5 AI for professional development | <script input="range" min="0" max="3" step="1" value="0" output="cft5">@input</script> |

<!-- CHECK: competency names against UNESCO (2024b), AI competency framework for teachers, Table 1 -->
<script modify="false" style="display:block">
const v = [@input(`cft1`), @input(`cft2`), @input(`cft3`), @input(`cft4`), @input(`cft5`)].map(Number);
const dims = ["Human-centred mindset","Ethics of AI","AI foundations & applications","AI pedagogy","AI for prof. development"];
const comp = [
  ["Human agency","Human accountability","Social responsibility"],
  ["Ethical principles","Safe and responsible use","Co-creating ethical rules"],
  ["Basic AI techniques and applications","Application skills","Creating with AI"],
  ["AI-assisted teaching","AI-pedagogy integration","AI-enhanced pedagogical transformation"],
  ["AI enabling lifelong professional learning","AI to enhance organizational learning","AI to support professional transformation"]];
const cx = 160, cy = 150, R = 110;
const pt = (i, r) => { const a = -Math.PI/2 + i * 2*Math.PI/5; return [cx + r*Math.cos(a), cy + r*Math.sin(a)]; };
let grid = "";
for (let l = 1; l <= 3; l++) grid += `<polygon points="${[0,1,2,3,4].map(i => pt(i, R*l/3).join(",")).join(" ")}" fill="none" stroke="#94a3b8" stroke-dasharray="3 3"/>`;
const axes = [0,1,2,3,4].map(i => { const [x,y] = pt(i, R); const [lx,ly] = pt(i, R + 22); return `<line x1="${cx}" y1="${cy}" x2="${x}" y2="${y}" stroke="#94a3b8"/><text x="${lx}" y="${ly}" font-size="10" text-anchor="middle" fill="currentColor">${i+1}</text>`; }).join("");
const poly = `<polygon points="${v.map((x,i) => pt(i, R*x/3).join(",")).join(" ")}" fill="rgba(37,99,235,0.35)" stroke="#2563eb" stroke-width="2"/>`;
const lvl = ["–","Acquire","Deepen","Create"];
const list = v.map((x,i) => `<li><b>${dims[i]}</b>: ${x === 0 ? "not yet" : lvl[x] + " → <i>" + comp[i][x-1] + "</i>"}</li>`).join("");
const next = v.indexOf(Math.min(...v));
`HTML: <div style="display:flex;flex-wrap:wrap;gap:16px;align-items:center"><svg viewBox="0 0 320 300" style="width:300px;max-width:100%">${grid}${axes}${poly}</svg><div style="flex:1;min-width:240px"><ul>${list}</ul><p>🚀 <b>Growth area:</b> ${dims[next]}${v[next] < 3 ? " – next competency: <i>" + comp[next][v[next]] + "</i>" : ""}</p></div></div>`
</script>

                --{{0}}--
Move the sliders. The radar shows your profile, and the list names the UNESCO competency that belongs to each level. Take a screenshot: you will repeat this self-check in session six and use the difference in your reflection paper.

## EU AI Act: Risk Pyramid

``` ascii
            /\        UNACCEPTABLE  – prohibited
           /  \       e.g. emotion recognition of learners
          /----\      HIGH RISK – strict obligations
         /      \     e.g. admission, grading, exam proctoring
        /--------\    LIMITED RISK – transparency
       /          \   e.g. chatbots must disclose they are AI
      /------------\  MINIMAL RISK – no specific obligations
     /              \ e.g. spam filter, spell checker
    /________________\
```

{{1}}
<section>

Since **February 2025**, organisations deploying AI must ensure sufficient **AI literacy** of their staff (Art. 4).

</section>

## Game: Sort the Risk ⚖️

- [[Minimal] [Limited] [High] [Prohibited]]
- [  ( )       ( )      (X)      ( )   ]  AI that automatically grades final exams in a vocational school
- [  ( )       (X)      ( )      ( )   ]  Chatbot answering questions about workshop safety rules
- [  ( )       ( )      ( )      (X)   ]  Camera system recognising emotions of apprentices in class
- [  (X)       ( )      ( )      ( )   ]  Spell checker in the learning platform
- [  ( )       ( )      (X)      ( )   ]  AI deciding on admission to a training programme

{{1}}
<section>

**Real cases?** Try the [EU AI Act Compliance Checker (Future of Life Institute)](https://artificialintelligenceact.eu/assessment/eu-ai-act-compliance-checker/) with an AI tool from your school.

</section>

                --{{0}}--
Classify the five systems. Then we discuss the tricky ones. Remember: the risk level depends on the purpose of the system, not on the technology inside.

## 5. AI Trends in TVET and the Labour Market

| Trend | What it means for TVET |
| --- | --- |
| Automation of routine tasks | More monitoring, troubleshooting, problem-solving |
| AI as a work tool | Skilled workers use AI assistants and must evaluate outputs |
| Shorter half-life of skills | Lifelong learning, modular upskilling, **micro-credentials** |
| Human and transversal skills | Communication, critical thinking, collaboration |
| Green and digital transition | New qualifications combine technical, digital, sustainability skills |
| Personalised learning | Adaptive systems, AI tutors, VR/AR |

{{1}}
<section>

*WEF Future of Jobs Report 2025:* fastest-growing skills include AI and big data, networks and cybersecurity, technological literacy – together with creative thinking, resilience and lifelong learning.

</section>

## Think–Pair–Share: Your Vocational Field

Pick a field you know (automotive, care, logistics, electrical …).

**Which task will AI change most in the next five years?**

[[___]]

**Which task will stay human – and why?**

[[___ ___ ___]]

**Which trend matters most for your field?**

- [(automation)] Automation of routine tasks
- [(tool)] AI as a work tool
- [(skills)] Shorter half-life of skills
- [(human)] Human and transversal skills
- [(green)] Green and digital transition
- [(personal)] Personalised learning

                --{{0}}--
Two minutes alone, three minutes with your neighbour, then we collect answers in the classroom view.

## 6. Start Your AI Tools Log 📓

| Date | Tool (model) | Purpose | Prompt (short) | Output (short) | My evaluation | Kept / changed |
| --- | --- | --- | --- | --- | --- | --- |
| 15.10. | e.g. ChatGPT (GPT-…) | Explain tokens to apprentices | "You are a trainer …" | 3 analogies | 2 good, 1 misleading | Kept 1, rewrote 2 |

{{1}}
<section>

**Rules:** name tool *and* model · verify facts and references · **never** enter personal data of learners or colleagues

✅ **Task for today:** create your log and add your first entry (prompt builder or Gandalf).

</section>

## Exit Ticket 🎟️

**An LLM always picks the most probable next token.**

- [( )] True
- [(X)] False – it samples, and settings such as temperature change how often less probable tokens are chosen

**Which prompt block was missing most often in your own prompts until today?**

- [(role)] Role
- [(task)] Task
- [(context)] Context
- [(format)] Format
- [(examples)] Examples

**Next:** 22.10.2026 · 🔵 Self-learning S02 (tools, limitations, ethics) · Hand-in **28.10.2026, 23:59**

## References

- European Union. (2024). *Regulation (EU) 2024/1689 (Artificial Intelligence Act)*. https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- Lo, L. S. (2023). The CLEAR path: A framework for enhancing information literacy through prompt engineering. *The Journal of Academic Librarianship, 49*(4), 102720. https://doi.org/10.1016/j.acalib.2023.102720
- Schmager, S., Pappas, I. O., & Vassilakopoulou, P. (2025). Understanding human-centred AI: A review of its defining elements and a research agenda. *Behaviour & Information Technology, 44*(15), 3771–3810. https://doi.org/10.1080/0144929X.2024.2448719
- UNESCO. (2024a). *AI competency framework for students*. https://doi.org/10.54675/JKJB9835
- UNESCO. (2024b). *AI competency framework for teachers*. https://doi.org/10.54675/ZJTE2084
- World Economic Forum. (2025). *The future of jobs report 2025*. https://www.weforum.org/publications/the-future-of-jobs-report-2025/

**Interactive tools:** [Tiktokenizer](https://tiktokenizer.vercel.app) · [Transformer Explainer](https://poloclub.github.io/transformer-explainer/) · [LLM Visualization](https://bbycroft.net/llm) · [Gandalf (Lakera)](https://gandalf.lakera.ai) · [EU AI Act Compliance Checker](https://artificialintelligenceact.eu/assessment/eu-ai-act-compliance-checker/)

<small>Licence: CC BY 4.0 · Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), based on the self-learning unit S01; checked by the author.</small>
