<!--
author:    Dr. Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.1.0
language:  en
narrator:  UK English Female
mode:      Presentation
classroom: enable

title:     P04 – Applications of AI in TVET: tools, agents, AI in pedagogy (Session slides)
comment:   AI in TVET I – Slides for session 4 (live, 05.11.2026, 150 min): five learning objectives, adaptive learning, intelligent tutoring, chatbots, VR/AR, predictive analytics, curriculum alignment, AI agents, AI in pedagogy, micro-credential idea check. Interactive: adaptive-engine simulator, step-by-step hints, rule-based chatbot, accuracy-trap calculator, ESCO task, agent step-through, tool evaluation grid, heutagogy slider, idea canvas, exit ticket. Videos and explorables.
tags:      AI, TVET, Adaptive learning, ITS, Chatbots, VR, Learning analytics, AI agents, Heutagogy, Micro-credentials
-->

# Applications of AI in TVET

**Session 4 · 05.11.2026 · 🟢 Live · 150 min** · AI in TVET I, OVGU Magdeburg

Tools · agents · AI in pedagogy · micro-credential idea check

<small>Self-learning unit for this session: [S04 – Applications of AI in TVET](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/Selflearn/S04_Applications_of_AI_in_TVET.md) · Graphical version of these slides: [HTML slides](https://ovgu-vet-teched.github.io/AI_in_TVET_I_WiSe_2026_2027/Presentations/P04_Applications_of_AI_in_TVET.html)</small>

                --{{0}}--
Welcome back to our second live session. Before we start: your open questions from the two self-learning sessions. Then we tour the application landscape of AI in vocational education, look at AI agents as the newest development, and in the second half we check your micro-credential ideas together.

## Welcome Back! Your Questions First 💬

**What was the most surprising thing in S02 or S03?**

[[___]]

**What is still unclear?**

[[___ ___]]

**How did your reference check go – how many of the AI's references were correct?**

- [(0)] None
- [(1)] One
- [(2)] Two
- [(3)] All three

**Your question on the reading on human-centred AI (Schmager et al., 2025):**

[[___]]

                --{{0}}--
Answer anonymously in the classroom. We take fifteen minutes for the most frequent questions before we move on. If you noted a question on the human-centred AI reading from session one, add it here as well.

## Today's Objectives 🎯

**By the end of today you can …**

<!-- data-type="none" -->
| | You can … | Where we practise it |
| --- | --- | --- |
| **LO1** | **describe** six application areas of AI in TVET – what the system decides, which data it needs, what stays with the teacher – with a vocational example each | Sections 1–2.6 |
| **LO2** | **explain** how AI agents differ from chatbots and where humans must stay in the loop | Section 2.7 |
| **LO3** | **evaluate** an AI tool for your vocational field – and see through misleading evidence such as "99 % accuracy" | Sections 2.5 and 3 |
| **LO4** | **explain** how AI shifts teaching, assessment and the teacher's role | Section 4 |
| **LO5** | **refine** your micro-credential idea with a structured idea check and peer feedback | Section 5 |

{{1}}
<section>

**Rate yourself:** Where do you start?

[(none)(basic)(solid)]
[                    ] LO1 · Six application areas
[                    ] LO2 · AI agents and human oversight
[                    ] LO3 · Evaluating an AI tool
[                    ] LO4 · AI in pedagogy
[                    ] LO5 · My micro-credential idea

</section>

                --{{0}}--
These five objectives frame today's session. They follow the objectives of the self-learning unit S04 and add one new objective on AI agents. At the end of the session, the exit ticket has one question per objective.

                --{{1}}--
Rate yourself now. At the end of the session, you rate yourself again and can see what changed.

## Today's Route 🗺️

<!-- data-type="none" -->
| Time | Block | Objective | How |
| --- | --- | --- | --- |
| 0:00 | Your questions from S02/S03 | – | Classroom poll, Q&A |
| 0:15 | Objectives & route | – | Self-rating |
| 0:20 | **1–2.6** Six application areas | LO1 · LO3 | Game, videos, adaptive-engine simulator, chatbot test, accuracy trap, ESCO |
| 1:00 | **2.7** AI agents | LO2 | Agent step-through |
| 1:12 | ☕ Break | | 10 min |
| 1:22 | **3** Evaluate an AI tool | LO3 | Evaluation grid, compare in pairs |
| 1:37 | **4** AI in pedagogy | LO4 | Vote, heutagogy slider |
| 1:52 | **5** Micro-credential idea check | LO5 | Idea canvas, 90-second pitches, peer feedback |
| 2:25 | Exit ticket & outlook | all | Quiz, self-rating |

                --{{0}}--
Here is our route for the next one hundred and fifty minutes. The first half is about applications and agents, the second half is about you: your evaluation of a tool, your view on pedagogy and your micro-credential idea.

## 1. Where AI Is Used in TVET 🏭

``` ascii
                      ┌──────────────────────┐
                      │   Learner & Teacher  │
                      └──────────┬───────────┘
   ┌───────────────┬─────────────┼──────────────┬────────────────┐
 Adaptive        Intelligent    Chatbots /     VR/AR +        Analytics &
 learning        tutoring       AI assistants  AI simulation  curriculum
 systems         systems                                       alignment
```

{{1}}
<section>

Six families of applications – in practice they are often **combined**, e.g. a welding simulator with automatic feedback that also stores learning data for the trainer.

</section>

{{2}}
<section>

> **Three questions for every application** (S04)
>
> 1. What does the system **decide or suggest**?
> 2. Which **data** does it need?
> 3. What remains the task of the **teacher or trainer**?

</section>

                --{{0}}--
AI in vocational education is not one tool but a family of applications. We look at six of them, from adaptive learning systems to tools that align curricula with the labour market.

                --{{2}}--
Keep these three questions in mind for every application today. They are the core of your evaluation later in section three.

## Game: Match the Application 🃏

- [[Adaptive learning] [ITS] [Chatbot] [VR/AR] [Predictive analytics] [Curriculum alignment]]
- [       (X)          ( )     ( )      ( )            ( )                  ( )        ]  Hydraulics module offers extra exercises after errors
- [       ( )          (X)     ( )      ( )            ( )                  ( )        ]  Step-by-step hints during a fault-finding task
- [       ( )          ( )     (X)      ( )            ( )                  ( )        ]  24/7 answers on workshop safety rules
- [       ( )          ( )     ( )      (X)            ( )                  ( )        ]  Welding simulator analysing torch angle and speed
- [       ( )          ( )     ( )      ( )            (X)                  ( )        ]  Early-warning dashboard for dropout risk
- [       ( )          ( )     ( )      ( )            ( )                  (X)        ]  Matching job advertisements with training regulations

                --{{0}}--
Six applications, six examples. You have one minute.

## 2.1 Adaptive Learning Systems 🧭

Learner model + domain model → next step.

``` ascii
 ┌──────────────────┐  answers, errors,  ┌──────────────────────┐
 │     Learner      │ ─── time ────────► │    Learner model     │
 │  works on a task │                    │ "what the learner    │
 └────────▲─────────┘                    │  already knows"      │
          │                              └──────────┬───────────┘
          │  next task, hint, pace       ┌──────────▼───────────┐     ┌────────────────────┐
          └───────────────────────────── │   Adaptation rules   │ ◄── │    Domain model    │
                                         │  "what comes next?"  │     │ "what there is to  │
                                         └──────────────────────┘     │  learn, in order"  │
                                                                      └────────────────────┘
```

{{1}}
<section>

🔧 **In TVET:** an online hydraulics module notices repeated errors with valve symbols and offers extra exercises before moving on.

**Decides:** next task, difficulty, pace · **Data:** answers, errors, time on task · **Teacher:** sets goals, reads the flags, talks to the learner

</section>

{{2}}
<section>

> **Watch for** (3 min): How does the video define adaptive learning? Which questions should you ask before choosing a platform?

!?[Video: Is adaptive learning what you think it is? (SparkLearn, 3 min)](https://www.youtube.com/watch?v=e3kIBxIJ7zs "SparkLearn · Demystifying Digital Learning · 3:00 · chapters: definition, results, demo")

</section>

                --{{0}}--
An adaptive learning system has two models. The learner model estimates what the learner already knows. The domain model describes what there is to learn and in which order. Adaptation rules combine both and choose the next step.

                --{{1}}--
Here is the answer to our three questions for the hydraulics example. Notice: the system decides about the next task, but the goals and the conversation with the learner stay with the teacher.

## Playground: Be the Adaptive Engine 🎛️

**Try it:** You are the adaptation rules. Move the sliders – what does the system do next?

Learner model – estimated mastery of *valve symbols* (%): <script input="range" min="0" max="100" step="5" value="35" output="mast">@input</script>

Wrong answers in a row: <script input="range" min="0" max="3" step="1" value="2" output="wrong">@input</script>

<script modify="false" style="display:block">
const m = Number(@input(`mast`)), w = Number(@input(`wrong`));
let step, who;
if (w >= 3) { step = "Stop the task series and show a worked example"; who = "🚩 Flag for the trainer: the learner seems stuck – a conversation is needed."; }
else if (w == 2) { step = "Give a hint and an easier task on the same topic"; who = "The system handles this alone – the trainer sees it in the dashboard."; }
else if (m < 40) { step = "Basic task with step-by-step support"; who = "The system handles this alone."; }
else if (m < 75) { step = "Standard task, hints on request"; who = "The system handles this alone."; }
else { step = "Challenge task – or move on to the next topic"; who = "Trainer check: is the learner ready for the real hydraulic test bench?"; }
const col = m < 40 ? "#d03b3b" : (m < 75 ? "#fab219" : "#0ca30c");
`HTML: <div style="border:2px solid #7a003f;border-radius:10px;padding:10px">
<p style="margin:0 0 6px 0"><b>Mastery estimate:</b> ${m} %</p>
<div style="background:#e5e7eb;border-radius:6px;height:12px"><div style="background:${col};height:12px;width:${m}%;border-radius:6px"></div></div>
<p style="margin:8px 0 0 0">➡️ <b>Next step:</b> ${step}<br>👩‍🏫 ${who}</p></div>`
</script>

<small>Simplified, illustrative rules. Real systems estimate mastery statistically from many answers – but the logic "estimate → rule → next step" is the same.</small>

                --{{0}}--
Move the sliders. With two wrong answers in a row the system gives a hint and an easier task. With three, a good system stops and asks a human for help. Where would you set these thresholds for your apprentices?

## 2.1 What the Evidence Says 📈

{{1}}
<section>

- 69 studies: better performance in **41 (59 %)**, higher engagement in **25 (36 %)**; pre-knowledge quizzes most common trigger; Moodle among top platforms (du Plooy et al., 2024)
- Many prototypes, **few implemented systems** that address real learner problems (Kabudi et al., 2021) · publications: 1 (1990) → 636 (2023) (Strielkowski et al., 2025)

</section>

{{2}}
<section>

🎼 **The teacher as conductor:** good vocational teachers *orchestrate* – small groups, real work tasks, adaptive instructions, flexible arrangements (Zhao & Ko, 2024). Software must fit into this orchestration, not replace it.

**Risks:** biased learner models · costs · data protection · "learning in isolation"

</section>

                --{{1}}--
The evidence is promising but mostly from higher education, and many systems never leave the prototype stage.

                --{{2}}--
In vocational classrooms, the teacher orchestrates group work, real work tasks and instructions. Adaptive software is one instrument in this orchestra, not the conductor.

## 2.2 Intelligent Tutoring Systems 🧑‍🏫

An ITS guides the learner **step by step** through a task: it checks every step and gives hints – not only a score at the end.

``` ascii
 OUTER LOOP – which task next?    [ Task 1 ] ─────► [ Task 2 ] ─────► [ Task 3 ]
                                       │
 INNER LOOP – within one task     step ──► feedback / hint ──► step ──► feedback ──► done
```

<small>Inner and outer loop (VanLehn, 2006)</small>

{{1}}
<section>

📊 **Lab vs. field:** one-to-one tutoring was reported to be about **2 standard deviations** better than classroom teaching – Bloom's "2 sigma problem" (Bloom, 1984). A review found step-based ITS (**d = 0.76**) almost as effective as human tutors (**d = 0.79**) (VanLehn, 2011).

🧑‍🏫 **ITS:** 40 field studies show a **complicated picture** – few countries ("intelligent regional gap"), focus on test scores, some lack rigour (Wang et al., 2023) · open-source framework turns individual tutors into **collaborative** ones (Arnau-González et al., 2025)

</section>

{{2}}
<section>

> **🏠 At home – watch for:** What does the AI tutor do differently from a search engine? Which of our three questions (decides · data · teacher) does the video answer – and which not?

!?[Video: How AI could save (not destroy) education – Sal Khan, TED 2023 (15 min)](https://www.youtube.com/watch?v=hJP5GqnTrNo "TED · Sal Khan demos the AI tutor Khanmigo · 15:37")

Critical report on the same tutor in schools: [Meet Khanmigo – 60 Minutes (13 min)](https://www.youtube.com/watch?v=Ia3CPhVkUtg)

</section>

                --{{0}}--
An intelligent tutoring system works on two loops. The outer loop selects the next task, like an adaptive system. The inner loop is special: it follows every single step and gives a hint exactly where the learner is stuck.

                --{{1}}--
In the lab, step-based tutors come close to human tutors. In real schools the picture is more complicated. This gap between lab evidence and field evidence is something you will meet again and again.

## Try It: Step-by-Step Hints 💡

A trainee electronics technician has to replace a faulty ceiling lamp. Before opening the housing, the circuit must be made safe.

**Order:** Put the five safety rules (EN 50110-1) in the right order.

<!-- data-randomize data-show-partial-solution -->
1st [->[ Disconnect completely ]] → 2nd [->[ Secure against reconnection ]] → 3rd [->[ Verify that no voltage is present ]] → 4th [->[ Earth and short-circuit ]] → 5th [->[ Cover adjacent live parts ]]

<details>

<summary>💡 Hint 1</summary>

First make the circuit dead – then make sure it stays dead.

</details>

<details>

<summary>💡 Hint 2</summary>

You can only verify that no voltage is present *after* you have disconnected and secured the circuit. Earthing comes after verifying.

</details>

<details>

<summary>✅ Solution</summary>

Disconnect completely → secure against reconnection → verify that no voltage is present → earth and short-circuit → cover adjacent live parts.

</details>

{{1}}
<section>

**Reflect:** This is how an ITS works – graded hints at the step where you are stuck. It also **logs** every hint you open. Which hint did you need?

- [(0)] None
- [(1)] Hint 1
- [(2)] Hint 2
- [(3)] The solution

</section>

                --{{0}}--
Try it yourself. If you are unsure, open the hints one after another. Notice the design: the first hint is general, the second is specific, and only then comes the solution. Intelligent tutoring systems work exactly like this.

                --{{1}}--
An intelligent tutoring system would store which hints you opened. That is valuable for adaptation – and it is personal learning data. Remember this when we evaluate tools.

## 2.3 Chatbots and AI Assistants 💬

``` ascii
 1966  ELIZA ──────────────► 2016  Jill Watson ──────────► since 2022  LLM chatbots
       rule-based keyword          AI teaching assistant          generate free answers –
       matching                    answers forum questions        and can hallucinate
```

{{1}}
<section>

💬 **Chatbots:** quick, personalised support (Okonkwo & Ade-Ibijola, 2021) · can connect learners with teachers, social workers, psychologists (Mendoza et al., 2022) · teachers adopt them depending on **innovativeness, trust, ease of use – and social pressure** from colleagues and leaders (482 teachers; Celik et al., 2025)

</section>

{{2}}
<section>

> **Watch for** (4.5 min): Which tasks does the AI teaching assistant take over – and which stay with the instructor?

!?[Video: Meet Jill Watson – the AI teaching assistant (AI-ALOE, 4.5 min)](https://www.youtube.com/watch?v=9mbTkmC9_s4 "AI-ALOE (NSF AI Institute) · Jill Watson · 4:31")

</section>

                --{{0}}--
Chatbots are older than you might think. ELIZA, built by Joseph Weizenbaum in 1966, matched keywords with prepared answers. Today's chatbots are based on large language models and generate their answers freely – which makes them flexible, but also lets them invent facts.

                --{{2}}--
Jill Watson is an AI teaching assistant from Georgia Tech. While you watch, note which tasks it takes over and which remain with the human instructor.

## Try It: A Rule-Based Chatbot 🤖

**Try it:** Ask the workshop safety bot a question. Then ask the *same* question in other words.

**Your question:** <script input="text" value="Do I need gloves at the drilling machine?" output="botq" input-always-active>@input</script>

<script modify="false" style="display:block">
const q = `@input(`botq`)`.toLowerCase();
const rules = [
 [/eye|goggle|glasses/, "Wear safety glasses at every machine with chips or sparks, e.g. grinder or lathe.", "eye, goggle, glasses"],
 [/glove/, "No gloves at rotating machines such as drills or lathes – they can be caught. Use gloves for sharp sheet metal.", "glove"],
 [/hair/, "Tie back long hair before you work at rotating machines.", "hair"],
 [/fire|extinguisher/, "Fire extinguisher: next to the exit. Report every fire to the trainer at once.", "fire, extinguisher"],
 [/first aid|injur|cut/, "First-aid kit: at the trainer's desk. Report every injury, even small cuts.", "first aid, injur, cut"],
 [/weld/, "Weld only with welding helmet, leather apron and gloves – and with the fume extraction switched on.", "weld"],
 [/shoe|boot/, "Safety shoes are mandatory in the workshop.", "shoe, boot"]];
const hit = rules.find(r => r[0].test(q));
const answer = hit ? hit[1] : "Sorry, I don't understand. Try one of my keywords: goggles, gloves, hair, fire, first aid, welding, shoes.";
`HTML: <div style="border-left:4px solid #7a003f;padding:6px 10px;background:rgba(122,0,63,0.06)">🤖 <b>SafetyBot:</b> ${answer}</div>
<p><small>Matched keyword: <b>${hit ? hit[2] : "none"}</b></small></p>`
</script>

{{1}}
<section>

**Test:** Try *"My eyes hurt after welding"* and *"Can I wear mittens at the lathe?"* – what goes wrong?

**Compare:** Talk to the original [ELIZA (1966)](https://www.masswerk.at/elizabot/eliza.html) – then think of an LLM chatbot. What does an LLM do better – and which **new** risk does it bring?

- [(1)] It understands paraphrases – but can invent wrong answers (hallucination)
- [(2)] It is always correct because it learned from more data
- [(3)] There is no real difference

</section>

                --{{0}}--
This bot works like the early chatbots: it looks for keywords and returns a prepared answer. Ask it about gloves, goggles or welding.

                --{{1}}--
"My eyes hurt after welding" matches the keyword "eye" and returns the rule on safety glasses – but the learner needs first aid. And "mittens" is not on the keyword list at all. A language model understands such paraphrases, but it can also produce answers that sound right and are wrong.

## 2.4 VR/AR and AI in Skill Training 🥽

Conventional welding training is costly in material, time and infrastructure (Lavrentieva et al., 2020).

<!-- data-type="none" -->
| | VR | AR |
| --- | --- | --- |
| What you see | a fully virtual workshop | virtual workpiece, arc and seam in the real room |
| What you hold | controller or torch replica | a real torch on a real workpiece holder |
| AI / software | tracks torch angle, travel speed and distance, scores every seam | same – trainers can replay each exercise |

{{1}}
<section>

🥽 **VR/AR welding:** safe, material-saving practice (Lavrentieva et al., 2020) · review of 42 studies: mostly **entry-level**, little evidence for distance learning (Chan et al., 2022) · limits: costs, cybersickness, transfer to the real workshop

</section>

{{2}}
<section>

> **Watch for** (3 min, vendor video – watch critically): Which data does the simulator collect? What can it **not** train that a real workshop does?

!?[Video: AugmentedArc augmented reality welding simulator (Miller, 3 min)](https://www.youtube.com/watch?v=wYRymhZrFmk "Miller Welders · vendor video · 3:13")

Example from Germany: [AR welding lab at GSI SLV Nord, Hamburg (Seabery, 1.5 min)](https://www.youtube.com/watch?v=loSmsC6ivuo)

</section>

                --{{0}}--
Welding simulators are the best-known example of AI-supported skill training. Virtual reality puts you into a completely virtual workshop. Augmented reality shows virtual seams on top of the real environment, so you work with a real torch.

                --{{2}}--
This is a vendor video, so watch it with a critical eye. Ask yourself what a simulator cannot train: heat, noise, smell, real material faults – and the transfer to the real workshop.

## 2.5 Predictive Analytics: How an Early-Warning System Works 🚦

``` ascii
 Data              Model            Risk score         Threshold          Action
 grades,      ──►  learns     ──►   0.0 ... 1.0   ──►  e.g. 0.5     ──►   🚩 flagged learner
 attendance,       from past                           set by humans      → conversation,
 background        cohorts                                                  support offer
```

{{1}}
<section>

| Term | Question it answers |
| --- | --- |
| **Recall** | Of all learners who *really* drop out – how many does the system flag? |
| **Specificity** | Of all learners who stay – how many does it correctly leave alone? |
| **Precision** | Of all flagged learners – how many are *really* at risk? |
| **Accuracy** | Of all decisions – how many are correct? |

</section>

{{2}}
<section>

⚖️ The **threshold** is a human decision: lower → more dropouts caught, but more false alarms.

</section>

                --{{0}}--
An early-warning system turns data into a risk score. Humans decide on a threshold above which a learner is flagged. And then humans act: a conversation, a support offer.

                --{{1}}--
Four terms help you to read the numbers. Recall asks how many real dropouts are found. Precision asks how many flagged learners are really at risk. Accuracy mixes everything – and that is the trap on the next slide.

## 2.5 Predictive Analytics: The Accuracy Trap 🪤

> 14,495 students, dropout rate 8.5 %: a standard classifier recognised only **13 %** of dropouts – while being **99 %** right on those who stayed (Gonzalez-Nucamendi et al., 2023).

**Play with it:**

Dropout rate (%): <script input="range" min="1" max="30" step="0.5" value="8.5" output="rate">@input</script>

Recall – share of dropouts detected (%): <script input="range" min="0" max="100" step="1" value="13" output="rec">@input</script>

Specificity – share of stayers correctly ignored (%): <script input="range" min="50" max="100" step="0.5" value="99" output="spec">@input</script>

<script modify="false" style="display:block">
const N = 14495, r = Number(@input(`rate`))/100, rec = Number(@input(`rec`))/100, sp = Number(@input(`spec`))/100;
const D = Math.round(N*r), S = N - D;
const TP = Math.round(D*rec), FN = D - TP, TN = Math.round(S*sp), FP = S - TN;
const acc = (TP+TN)/N, base = S/N;
const cell = (n, label, bg) => `<td style="background:${bg};color:#111;padding:8px;text-align:center"><b>${n.toLocaleString("en")}</b><br><small>${label}</small></td>`;
`HTML: <table style="border-collapse:collapse;margin:6px 0"><tr><th></th><th style="padding:4px 8px">flagged</th><th style="padding:4px 8px">not flagged</th></tr>
<tr><th style="padding:4px 8px">drops out (${D.toLocaleString("en")})</th>${cell(TP,"caught ✅","#bbf7d0")}${cell(FN,"missed ❌","#fecaca")}</tr>
<tr><th style="padding:4px 8px">stays (${S.toLocaleString("en")})</th>${cell(FP,"false alarm ⚠️","#fde68a")}${cell(TN,"correctly ignored","#e5e7eb")}</tr></table>
<p>Accuracy: <b>${(acc*100).toFixed(1)} %</b> · A "model" that flags <i>nobody</i>: <b>${(base*100).toFixed(1)} %</b> · Teachers check <b>${(TP+FP).toLocaleString("en")}</b> flagged learners</p>
<p>${acc - base < 0.02 ? "🪤 <b>Trap!</b> High accuracy – but barely better than doing nothing. " + FN.toLocaleString("en") + " learners at risk are missed." : "📈 Now the system really adds value over doing nothing."}</p>`
</script>

<small>Calculator for illustration, using the study's sample size and dropout rate. In the study, adjusting the decision threshold raised dropout precision above 50 %.</small>

                --{{0}}--
With the original values, accuracy looks great at over ninety percent. But a system that flags nobody at all is almost as accurate. Move the recall slider up and watch what happens to false alarms. This is why accuracy alone tells you very little about an early-warning system.

## Explore: Precision & Recall 🔍

**Try it:** Scroll through the explorable and move the decision threshold. Find the point where you would set it for a dropout early-warning system – and say why.

<iframe src="https://mlu-explain.github.io/precision-recall/" width="100%" height="480" style="border:0;" allowfullscreen title="MLU-Explain: Precision and Recall (Amazon Machine Learning University)"></iframe>

*MLU-Explain: Precision & Recall (Amazon Machine Learning University)* · [Open in a new tab](https://mlu-explain.github.io/precision-recall/)

**Decide:** What matters more for a dropout early-warning system?

- [(recall)] High recall – miss as few at-risk learners as possible
- [(precision)] High precision – avoid false alarms and stigmatisation
- [(depends)] It depends on what happens to flagged learners

                --{{0}}--
This explorable shows the same trade-off with a moving threshold. There is no right answer to the vote. If a flag only leads to a friendly support offer, false alarms cost little. If a flag leads to labelling a learner, precision becomes much more important.

## Predictive Analytics in Vocational Schools

{{1}}
<section>

Istanbul, large vocational and technical high school: a decision tree with oversampling identified at-risk students best; **parental education, family structure, financial hardship** were strong predictors (Korkmaz & Aydın, 2025).

</section>

{{2}}
<section>

🚨 **Remember S02:** predictors like family background are exactly where **bias and stigmatisation** start – and such systems can be **high-risk** under the EU AI Act.

</section>

{{3}}
<section>

Explore fairness trade-offs interactively:

??[PAIR Explorable: Measuring Fairness](https://pair.withgoogle.com/explorables/measuring-fairness/)

</section>

## 2.6 Curriculum Alignment 📊

**Labour-market intelligence:** job ads → AI text classification → skills (ESCO) → compare with the training regulation → update the curriculum

{{1}}
<section>

AI analyses labour-market data to spot emerging skills and update curricula faster (Ejjami, 2024).

**3E model** (Liao & Zheng, 2025): **E**ducation (AI curriculum design) · **E**xperience (VR training) · **E**mployment (industry partnerships, AI labour-market scans) – tested with 10 vocational schools and 15 industry partners.

</section>

{{2}}
<section>

⚠️ Unequal access and biased algorithms can **widen inequalities**. Needed: infrastructure, continuous teacher training, new roles such as *Vocational AI Curriculum Developer* or *AI Data Protection Specialist* (Ejjami, 2024).

</section>

{{3}}
<section>

🇪🇺 **Real example:** Cedefop's *Skills-OVATE* analyses millions of online job advertisements from European countries and shows which occupations and skills employers ask for (Cedefop, n.d.).

!?[Video: Skills-OVATE – online vacancy analysis tool for Europe (Cedefop, 1 min)](https://www.youtube.com/watch?v=QLpoxIgfWTY "Cedefop · 1:07")

</section>

                --{{0}}--
Curriculum alignment uses AI on the other side of education: not on the learner, but on the labour market. Text classification sorts job advertisements into occupations and skills, and these can be compared with what the training regulations cover.

                --{{3}}--
A real example from the European Centre for the Development of Vocational Training: Skills-OVATE analyses online job ads across Europe. The data are a complement to other sources, not a replacement.

## Try It: Your Occupation in ESCO 🔎

ESCO – the European classification of **S**kills, **C**ompetences, Qualifications and **O**ccupations – is the vocabulary that tools like Skills-OVATE use.

1. Open [ESCO: occupations](https://esco.ec.europa.eu/en/classification/occupation_main) (opens in a new tab)
2. Search an occupation from your vocational field, e.g. *mechatronics technician* or *electrician*
3. Note **three essential skills** – and check: are they in the training regulation you know?

**Share:** Which skill would you add to the curriculum?

[[___]]

**Did you find a skill the training regulation does not (yet) cover?**

- [(yes)] Yes
- [(no)] No
- [(unsure)] Not sure

                --{{0}}--
Take three minutes. This is exactly the comparison that AI-based curriculum tools automate on a large scale. Doing it by hand once shows you how much interpretation it needs.

## 2.7 Current Development: AI Agents 🦾

**Chatbot:** one question → one answer. **Agent:** one goal → plans steps, uses tools, checks results, tries again (remember P03).

``` ascii
        ┌──────── PLAN ────────┐
        │                      ▼
     ADJUST                   ACT  ──► tools: web search, code, files
        ▲                      │
        └────── OBSERVE ◄──────┘        + memory
```

{{1}}
<section>

🔧 **In TVET (illustrative):**

- **Tutor agent** – plans an apprentice's revision week from the errors in the tutoring log and schedules matching tasks
- **Course-building agent** – drafts learning nuggets step by step, e.g. the open-source [LiaScript teaching-agent](https://github.com/LiaScript/teaching-agent): outline → didactics → agenda → sessions → materials, with approval at every step

</section>

{{2}}
<section>

⚠️ **The more autonomy, the more human oversight.** Agents *act* – a wrong step is repeated quickly and at scale. High-risk AI systems must allow effective **human oversight** (EU AI Act, Art. 14; European Union, 2024).

</section>

{{3}}
<section>

> **🏠 At home – watch for:** How does the video describe the step from a single model to a "compound AI system" – and what does the agent add?

!?[Video: What are AI agents? (IBM Technology, 12 min)](https://www.youtube.com/watch?v=F8NKVhkZZWI "IBM Technology · Maya Murad · 12:28")

</section>

                --{{0}}--
The newest development is AI agents. A chatbot answers one question. An agent receives a goal, plans several steps, uses tools such as web search or files, observes the result and adjusts its plan.

                --{{1}}--
In vocational education, agents could plan revision for apprentices or build learning material. The LiaScript teaching-agent, for example, builds a course in phases and asks the author for approval at each phase.

                --{{2}}--
Because agents act on their own, a mistake is not one wrong answer – it can be a chain of wrong actions. That is why human oversight matters even more.

## Playground: An Agent Builds Your Nugget 🛠️

Goal: *"Create a 15-minute LiaScript nugget: apprentices evaluate an AI diagnosis suggestion."*

**Agent step:** <script input="range" min="1" max="6" step="1" value="1" output="ag">@input</script>

<script modify="false" style="display:block">
const k = Number(@input(`ag`));
const d = {
 1: ["GOAL","Receives the goal, target group and time frame","–","✋ You set the goal – the agent cannot know your learners.",true],
 2: ["PLAN","Splits the job: outline → content → quiz → test","planning","The agent works alone.",false],
 3: ["ACT · research","Searches the web for sources on vehicle diagnosis","web search","✋ Check every reference – remember the reference check in S02.",true],
 4: ["ACT · write","Writes slides and a quiz as a LiaScript file","file editor","The agent works alone.",false],
 5: ["OBSERVE · test","Renders the file, finds a syntax error, fixes it","LiaScript preview","The agent corrects itself – this is the loop.",false],
 6: ["ADJUST · hand over","Asks you for approval","–","✋ You check content, didactics and licences – and note the AI use in your AI tools log.",true]}[k];
const dots = [1,2,3,4,5,6].map(i => `<span style="display:inline-block;width:26px;height:26px;line-height:26px;text-align:center;border-radius:50%;margin-right:4px;font-size:0.8em;background:${i==k?"#7a003f":(i<k?"#bc7f9f":"#e5e7eb")};color:${i<=k?"#fff":"#333"}">${i}</span>`).join("");
`HTML: <div>${dots}</div><div style="border:2px solid ${d[4]?"#d03b3b":"#7a003f"};border-radius:10px;padding:10px;margin-top:8px">
<h3 style="margin:0">${d[0]}</h3>
<p style="margin:6px 0 0 0"><b>Agent does:</b> ${d[1]}<br><b>Tool:</b> ${d[2]}<br><b>Human role:</b> ${d[3]}</p></div>`
</script>

{{1}}
<section>

**Decide:** At which steps must you as the author check? (several answers)

<!-- data-hint-button="1" data-solution-button="2" -->
- [[X]] Setting the goal and the target group
- [[X]] Checking the sources the agent found
- [[ ]] Fixing the syntax error the agent's own test found
- [[X]] Approving the nugget before it is published
[[?]] Think about where errors would reach your learners unnoticed.

</section>

                --{{0}}--
Move the slider from one to six and follow the agent. The red frames mark the human checkpoints.

                --{{1}}--
Three checkpoints: the goal, the sources and the final approval. The syntax error is a good example of what an agent can safely fix on its own, because its own test shows whether the fix worked.

## ☕ Break – 10 Minutes

After the break you **rate a real AI tool** for your vocational field.

**Think:** Which application from today would you test first in your field?

[[___]]

                --{{0}}--
Ten minutes break. When you come back, have the application you prepared at home ready – we evaluate it with the grid.

## 3. Playground: Evaluate an AI Tool 🔬

**Tool you evaluate:** <script input="text" value="AI welding simulator" output="evtool" input-always-active>@input</script>

Rate 1 (poor) – 5 (excellent):

| Criterion | Rating |
| --- | --- |
| Pedagogical value & evidence | <script input="range" min="1" max="5" step="1" value="4" output="e1">@input</script> |
| Active learner role | <script input="range" min="1" max="5" step="1" value="4" output="e2">@input</script> |
| Teacher can adapt / override | <script input="range" min="1" max="5" step="1" value="3" output="e3">@input</script> |
| Data & privacy (GDPR) | <script input="range" min="1" max="5" step="1" value="3" output="e4">@input</script> |
| Fairness & inclusion | <script input="range" min="1" max="5" step="1" value="3" output="e5">@input</script> |
| Legal frame (AI Act, licence) | <script input="range" min="1" max="5" step="1" value="4" output="e6">@input</script> |
| Costs & sustainability | <script input="range" min="1" max="5" step="1" value="2" output="e7">@input</script> |

<script modify="false" style="display:block">
const names = ["Pedagogy","Learner role","Teacher role","Privacy","Fairness","Legal","Costs"];
const v = [@input(`e1`),@input(`e2`),@input(`e3`),@input(`e4`),@input(`e5`),@input(`e6`),@input(`e7`)].map(Number);
const avg = v.reduce((a,b) => a+b, 0) / v.length;
const min = Math.min(...v), weak = names.filter((n,i) => v[i] === min);
const tool = `@input(`evtool`)`.replace(/</g,"&lt;");
const bars = v.map((x,i) => `<div style="display:flex;align-items:center;gap:6px;margin:2px 0"><span style="width:95px;font-size:0.85em">${names[i]}</span><div style="background:${x<=2?"#dc2626":x==3?"#f59e0b":"#16a34a"};height:14px;width:${x*20}%;max-width:60%;border-radius:3px"></div><span>${x}</span></div>`).join("");
const verdict = min <= 1 ? "🔴 Stop: at least one criterion is a deal-breaker." : (avg >= 3.5 ? "🟢 Promising – pilot it with clear human oversight." : "🟡 Possible – but fix the weak spots first.");
`HTML: <p><b>${tool}</b> · average ${avg.toFixed(1)} / 5</p>${bars}<p>${verdict}<br>Weakest: <i>${weak.join(", ")}</i></p>`
</script>

<details>

<summary>❓ Guiding questions per criterion (S04)</summary>

| Criterion | Questions |
| --- | --- |
| **Pedagogical value** | Which learning outcome does it support? Is there evidence? |
| **Learner role** | Does it promote active learning or passive consumption? |
| **Teacher role** | Who decides? Can the teacher adapt or override? |
| **Data & privacy** | Which data is collected, where is it stored, GDPR? |
| **Fairness & inclusion** | Does it work for all learners (language, disability, devices)? |
| **Legal frame** | Risk level under the EU AI Act? Licence? |
| **Costs & sustainability** | Costs, maintenance, energy, dependency on a provider |

</details>

                --{{0}}--
Use the grid for the application you prepared at home. Compare with your neighbour: did you rate the same tool differently? Why?

## 4. AI in Pedagogy: Six Shifts 🔄

{{1}}
<section>

1. **Personalisation** – individual paths in heterogeneous groups
2. **New teacher roles** – learning designer, coach, critical curator; **AI-TPACK** (Ning et al., 2024)
3. **Feedback & self-regulation** – goal setting, monitoring, reflection (Chang et al., 2023) – risk of offloading thinking
4. **Assessment** – AI drafts tasks & formative feedback; summative decisions stay human
5. **Inclusion** – translation, simple language, assistive features
6. **Self-determined learning (heutagogy)** – learners steer goals and even assessment

<details>

<summary>🔧 What it can look like in TVET (illustrative)</summary>

1. Apprentices with different prior training get different exercise paths in the CNC module.
2. The trainer checks and curates AI-generated work instructions before they are used.
3. An apprentice sets weekly goals with an AI coach; the trainer discusses the reflection.
4. AI drafts practice exam tasks; the examination board decides on the grade.
5. Work instructions in simple language or in the apprentice's first language.
6. A master-craftsperson candidate plans a learning project with AI as a sparring partner.

</details>

</section>

{{2}}
<section>

**Which shift matters most for your vocational field?**

- [(1)] Personalisation
- [(2)] New teacher roles
- [(3)] Feedback & self-regulation
- [(4)] Assessment
- [(5)] Inclusion
- [(6)] Heutagogy

</section>

                --{{1}}--
AI changes not only the tools, but teaching itself. Six shifts are visible in the research. Open the examples if you want to see what they could mean in a vocational school or a training workshop.

                --{{2}}--
Vote for the shift that matters most in your field. We look at the result together and discuss what you would need as a teacher to handle it.

## Playground: AI-Augmented Heutagogy 🪜

**Pedagogy** (teacher decides) → **Andragogy** (learner directs) → **Heutagogy** (learner determines goals, path and even assessment)

!?[Video: Pedagogy, andragogy and heutagogy in under a minute (Rebecca J. Hogue)](https://www.youtube.com/watch?v=1Ysim8-Gb7Y "Rebecca J. Hogue · 0:55")

Ng & Lai (2025): three AI paradigms ↔ SOLO levels ↔ learner autonomy.

**AI paradigm:** <script input="range" min="1" max="3" step="1" value="1" output="heu">@input</script>

<script modify="false" style="display:block">
const k = Number(@input(`heu`));
const d = {
 1: ["AI-informed","Provides information and progress data","Pre-/uni-structural","Low – teachers guide strongly","Apprentice gets a progress dashboard for the hydraulics module.","#93c5fd",33],
 2: ["AI-supported","Adaptive feedback, tailored content","Multi-structural, relational","Growing","AI tutor adapts fault-finding exercises and explains mistakes.","#60a5fa",66],
 3: ["AI-empowered","Partner for open, complex problems","Extended abstract","Full autonomy and agency","Master-craftsperson candidate uses AI as a sparring partner to design an energy concept for a real client.","#2563eb",100]}[k];
`HTML: <div style="border-radius:10px;border:2px solid ${d[5]};padding:10px">
<h3 style="margin:0">${d[0]}</h3>
<p><b>Role of AI:</b> ${d[1]}<br><b>SOLO level:</b> ${d[2]}<br><b>Learner autonomy:</b> ${d[3]}</p>
<div style="background:#e5e7eb;border-radius:6px;height:12px"><div style="background:${d[5]};height:12px;width:${d[6]}%;border-radius:6px"></div></div>
<p>🔧 <i>TVET example (illustrative):</i> ${d[4]}</p></div>`
</script>

<small>The TVET examples are illustrations; the framework itself comes from higher education. Fits continuing education and master-craftsperson training – needs changes to pedagogy, assessment, staff development and infrastructure.</small>

                --{{0}}--
Move the slider from one to three. As the AI becomes more of a partner, the learner needs more autonomy and higher levels of understanding. Discuss: at which level are most apprentices in your field today?

## 5. Micro-credential Idea Check 💡 (live)

Your final product: a **TVET micro-credential** with AI-supported LiaScript nuggets.

> A **micro-credential** is the record of the learning outcomes that a learner has acquired following a small volume of learning. These learning outcomes have been assessed against transparent and clearly defined standards (European Commission, 2021; Council of the European Union, 2022).

{{1}}
<section>

| # | Question |
| --- | --- |
| 1 | Which **skill gap** in which TVET sector? |
| 2 | Who is the **target group**? |
| 3 | Which **UNESCO competency** is the anchor? |
| 4 | 2–3 **learning outcomes** (verb + content + context) |
| 5 | Which **3–6 nuggets**? |
| 6 | How do learners **prove** the outcome? |
| 7 | Where does **AI** support learning – and where not? |
| 8 | Why would an **institution or employer** recognise it? |

</section>

                --{{0}}--
Now it is your turn. Your micro-credential is the core of the final assessment, and you pitch it on the nineteenth of November. Today we check the idea with eight questions. In session five you will describe it in detail with the EU template.

## Playground: Your Idea Canvas 🖼️

**Title:** <script input="text" value="AI-supported fault diagnosis in automotive electrics" output="ic1" input-always-active>@input</script>

**Skill gap:** <script input="text" value="Workshops use AI diagnosis tools, but apprentices can't judge their suggestions" output="ic2" input-always-active>@input</script>

**Target group:** <script input="text" value="3rd-year automotive mechatronics apprentices" output="ic3" input-always-active>@input</script>

**UNESCO anchor:** <script input="text" value="Students CFT – AI techniques and applications (Apply)" output="ic4" input-always-active>@input</script>

**Key learning outcome:** <script input="text" value="Learners can evaluate an AI diagnosis suggestion against measurement data" output="ic5" input-always-active>@input</script>

**Assessment:** <script input="text" value="Practical diagnosis task + short reflection" output="ic6" input-always-active>@input</script>

<script modify="false" style="display:block">
const e = s => s.replace(/</g,"&lt;");
const f = [`@input(`ic1`)`,`@input(`ic2`)`,`@input(`ic3`)`,`@input(`ic4`)`,`@input(`ic5`)`,`@input(`ic6`)`].map(e);
const ok = f.filter(x => x.trim().length > 5).length;
const verbs = /\b(can|able to)\s+(explain|evaluate|apply|design|create|analyse|analyze|compare|use|identify|assess|plan|justify|diagnose)/i.test(f[4]);
`HTML: <div style="border:3px solid #2563eb;border-radius:14px;padding:12px;background:linear-gradient(135deg,rgba(37,99,235,0.08),rgba(22,163,74,0.08))">
<div style="font-size:0.8em;letter-spacing:2px">MICRO-CREDENTIAL IDEA</div><h3 style="margin:4px 0">${f[0]}</h3>
<p>🎯 <b>Gap:</b> ${f[1]}<br>👥 <b>For:</b> ${f[2]}<br>🧭 <b>Anchor:</b> ${f[3]}<br>✅ <b>Outcome:</b> ${f[4]}<br>📝 <b>Proof:</b> ${f[5]}</p></div>
<p>Completeness: ${"🟩".repeat(ok)}${"⬜".repeat(6-ok)} ${verbs ? "· outcome uses an action verb 👍" : "· tip: start the outcome with <i>Learners can + action verb</i>"}</p>`
</script>

                --{{0}}--
Replace the example with your own idea. Take a screenshot of your canvas, then present it to your group in ninety seconds.

## Peer Feedback 🤝

**Groups of three** · 90-second pitch · 2 minutes feedback per idea

Each idea gets **one "What works"** and **one "What if …?"**

**What works:**

[[___ ___]]

**What if …?**

[[___ ___]]

**How ready is your idea?**

- [(1)] 🌱 Just a seed
- [(2)] 🌿 Growing
- [(3)] 🌳 Ready for the EU template

                --{{0}}--
Work in groups of three. Each of you pitches for ninety seconds, then the other two give one thing that works and one "what if" question. Keep the time – the timer is part of the training for your pitch.

## Exit Ticket 🎟️

**🎟️ LO1 · Applications** – A system gives step-by-step hints while an apprentice solves a fault-finding task. It is …

<!-- data-hint-button="1" data-solution-button="2" -->
- [( )] a predictive analytics system
- [(X)] an intelligent tutoring system
- [( )] a curriculum alignment tool
[[?]] Think of the inner loop.

**🎟️ LO2 · Agents** – An agent drafted your nugget and cites five sources. What is your job?

<!-- data-hint-button="1" data-solution-button="2" -->
- [( )] Nothing – the agent tested its own output
- [(X)] Check every reference and the content before publishing
- [( )] Only fix the layout
[[?]] Remember the reference check in S02.

**🎟️ LO3 · Evaluation** – An early-warning system is 92 % accurate; 8.5 % of learners drop out. What do you ask first?

<!-- data-hint-button="1" data-solution-button="2" -->
- [(X)] How many of the real dropouts does it detect (recall)?
- [( )] Which programming language was used?
- [( )] Nothing – 92 % is excellent
[[?]] A system that flags nobody is already 91.5 % accurate.

**🎟️ LO4 · Pedagogy** – In the *AI-empowered* paradigm (Ng & Lai, 2025), the learner …

<!-- data-hint-button="1" data-solution-button="2" -->
- [( )] receives a progress dashboard and is guided strongly by the teacher
- [(X)] uses AI as a partner for open, complex problems with full autonomy
- [( )] does not use AI at all
[[?]] Think of slider position 3.

**🎟️ LO5 · Micro-credential** – Which learning outcome follows *verb + content + context*?

<!-- data-hint-button="1" data-solution-button="2" -->
- [( )] Learners understand AI.
- [( )] Learners will learn about AI diagnosis tools.
- [(X)] Learners can evaluate an AI diagnosis suggestion against measurement data in the workshop.
[[?]] Look for an observable action verb.

                --{{0}}--
One question per learning objective. Answer them alone, then we look at the class results together.

## Next: Session 5 📅

**12.11.2026 · 🔵 Self-learning** – describe your micro-credential with the **EU template** and start your learning nuggets.

✍️ Revise your idea with today's feedback.

**Rate yourself again:** Where are you now?

[(none)(basic)(solid)]
[                    ] LO1 · Six application areas
[                    ] LO2 · AI agents and human oversight
[                    ] LO3 · Evaluating an AI tool
[                    ] LO4 · AI in pedagogy
[                    ] LO5 · My micro-credential idea

🏠 **Optional videos:** Sal Khan (TED, 15 min) · IBM: What are AI agents? (12 min) · 60 Minutes on Khanmigo (13 min) – links in the references.

                --{{0}}--
Compare your rating with the start of the session. Next week is a self-learning week: you describe your micro-credential with the EU template and start your first learning nuggets.

## References

- Arnau-González, P., Solera-Monforte, S., Wu, Y., & Arevalillo-Herráez, M. (2025). A framework for adapting conversational intelligent tutoring systems to enable collaborative learning. *Expert Systems with Applications, 271*, 126663. https://doi.org/10.1016/j.eswa.2025.126663
- Bloom, B. S. (1984). The 2 sigma problem: The search for methods of group instruction as effective as one-to-one tutoring. *Educational Researcher, 13*(6), 4–16. https://doi.org/10.3102/0013189X013006004
- Cedefop. (n.d.). *Skills-OVATE: Skills online vacancy analysis tool for Europe*. https://www.cedefop.europa.eu/en/tools/skills-ovate
- Celik, I., Muukkonen, H., & Siklander, S. (2025). Teacher – artificial intelligence (AI) interaction. *Policy Futures in Education, 24*(1), 164–188. https://doi.org/10.1177/14782103251348551
- Chan, V. S., Haron, H. N. H., Isham, M. I. B. M., & Mohamed, F. B. (2022). VR and AR virtual welding for psychomotor skills: A systematic review. *Multimedia Tools and Applications, 81*, 12459–12493. https://doi.org/10.1007/s11042-022-12293-5
- Chang, D. H., Lin, M. P.-C., Hajian, S., & Wang, Q. Q. (2023). Educational design principles of using AI chatbot that supports self-regulated learning in education. *Sustainability, 15*(17), 12921. https://doi.org/10.3390/su151712921
- Council of the European Union. (2022). *Council Recommendation of 16 June 2022 on a European approach to micro-credentials for lifelong learning and employability* (2022/C 243/02). https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022H0627(02)
- du Plooy, E., Casteleijn, D., & Franzsen, D. (2024). Personalized adaptive learning in higher education: A scoping review. *Heliyon, 10*(21), e39630. https://doi.org/10.1016/j.heliyon.2024.e39630
- Ejjami, R. (2024). AI's impact on vocational training and employability. *International Journal for Multidisciplinary Research, 6*(4). https://doi.org/10.36948/ijfmr.2024.v06i04.24967
- European Commission. (2021). *A European approach to micro-credentials* [Factsheet]. Publications Office of the European Union.
- European Union. (2024). *Regulation (EU) 2024/1689 (Artificial Intelligence Act)*. https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- Gonzalez-Nucamendi, A., Noguez, J., Neri, L., Robledo-Rella, V., & García-Castelán, R. M. G. (2023). Predictive analytics study to determine undergraduate students at risk of dropout. *Frontiers in Education, 8*, 1244686. https://doi.org/10.3389/feduc.2023.1244686
- Kabudi, T., Pappas, I., & Olsen, D. H. (2021). AI-enabled adaptive learning systems: A systematic mapping of the literature. *Computers and Education: Artificial Intelligence, 2*, 100017. https://doi.org/10.1016/j.caeai.2021.100017
- Korkmaz, Ö., & Aydın, M. N. (2025). Detection of early school drop out in vocational and technical high schools in Turkey. *SAGE Open, 15*(3). https://doi.org/10.1177/21582440251370443
- Lavrentieva, O. O., Arkhypov, I. O., Kuchma, O. I., & Uchitel, A. D. (2020). Use of simulators together with virtual and augmented reality in the system of welders' vocational training. *CEUR Workshop Proceedings, 2547*, 201–216. https://ceur-ws.org/Vol-2547/paper15.pdf
- Liao, J., & Zheng, Y. (2025). Integrating artificial intelligence into vocational education: A technical application framework based on the 3E model. ACM. https://doi.org/10.1145/3745238.3745471
- Mendoza, S., Sánchez-Adame, L. M., Urquiza-Yllescas, J. F., González-Beltrán, B. A., & Decouchant, D. (2022). A model to develop chatbots for assisting the teaching and learning process. *Sensors, 22*(15), 5532. https://doi.org/10.3390/s22155532
- Ng, S. H. S., & Lai, J. W. (2025). AI-augmented heutagogy. *Higher Education Research & Development*. https://doi.org/10.1080/07294360.2025.2564977
- Ning, Y., Zhang, C., Xu, B., Zhou, Y., & Wijaya, T. T. (2024). Teachers' AI-TPACK. *Sustainability, 16*(3), 978. https://doi.org/10.3390/su16030978
- Okonkwo, C. W., & Ade-Ibijola, A. (2021). Chatbots applications in education: A systematic review. *Computers and Education: Artificial Intelligence, 2*, 100033. https://doi.org/10.1016/j.caeai.2021.100033
- Schmager, S., Pappas, I. O., & Vassilakopoulou, P. (2025). Understanding human-centred AI: A review of its defining elements and a research agenda. *Behaviour & Information Technology, 44*(15), 3771–3810. https://doi.org/10.1080/0144929X.2024.2448719
- Strielkowski, W., Grebennikova, V., Lisovskiy, A., Rakhimova, G., & Vasileva, T. (2025). AI-driven adaptive learning for sustainable educational transformation. *Sustainable Development, 33*, 1921–1947. https://doi.org/10.1002/sd.3221
- VanLehn, K. (2006). The behavior of tutoring systems. *International Journal of Artificial Intelligence in Education, 16*(3), 227–265.
- VanLehn, K. (2011). The relative effectiveness of human tutoring, intelligent tutoring systems, and other tutoring systems. *Educational Psychologist, 46*(4), 197–221. https://doi.org/10.1080/00461520.2011.611369
- Wang, H., Tlili, A., Huang, R., et al. (2023). Examining the applications of intelligent tutoring systems in real educational contexts. *Education and Information Technologies, 28*(7), 9113–9148. https://doi.org/10.1007/s10639-022-11555-x
- Weizenbaum, J. (1966). ELIZA – A computer program for the study of natural language communication between man and machine. *Communications of the ACM, 9*(1), 36–45. https://doi.org/10.1145/365153.365168
- Zhao, Y., & Ko, J. (2024). Orchestrating vocational education classrooms for adaptive instruction and collaborative learning. *Cogent Education, 11*(1). https://doi.org/10.1080/2331186X.2024.2351238

**Videos:** AI-ALOE. *Meet Jill Watson* (4:31) https://www.youtube.com/watch?v=9mbTkmC9_s4 · Cedefop. *Skills-OVATE* (1:07) https://www.youtube.com/watch?v=QLpoxIgfWTY · Hogue, R. J. *Pedagogy, andragogy, and heutagogy* (0:55) https://www.youtube.com/watch?v=1Ysim8-Gb7Y · IBM Technology. *What are AI agents?* (12:28) https://www.youtube.com/watch?v=F8NKVhkZZWI · Miller Welders. *AugmentedArc* (3:13) https://www.youtube.com/watch?v=wYRymhZrFmk · 60 Minutes. *Meet Khanmigo* (13:18) https://www.youtube.com/watch?v=Ia3CPhVkUtg · Seabery. *AR welding lab GSI SLV* (1:38) https://www.youtube.com/watch?v=loSmsC6ivuo · SparkLearn. *Is adaptive learning what you think it is?* (3:00) https://www.youtube.com/watch?v=e3kIBxIJ7zs · TED. *Sal Khan: How AI could save (not destroy) education* (15:37) https://www.youtube.com/watch?v=hJP5GqnTrNo

**Interactive tools:** [ELIZA (1966)](https://www.masswerk.at/elizabot/eliza.html) · [ESCO classification](https://esco.ec.europa.eu/en/classification/occupation_main) · [LiaScript teaching-agent](https://github.com/LiaScript/teaching-agent) · [MLU-Explain: Precision & Recall](https://mlu-explain.github.io/precision-recall/) · [PAIR: Measuring Fairness](https://pair.withgoogle.com/explorables/measuring-fairness/) · [PAIR: Hidden Bias](https://pair.withgoogle.com/explorables/hidden-bias/)

<small>Licence: CC BY 4.0 · Dr. Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), based on the self-learning unit S04; checked by the author.</small>
