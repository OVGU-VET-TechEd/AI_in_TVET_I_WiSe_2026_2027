<!--
author:    Dr. Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Presentation
classroom: enable

title:     P04 – Applications of AI in TVET: tools, agents, AI in pedagogy (Session slides)
comment:   AI in TVET I – Slides for session 4 (live, 05.11.2026): adaptive learning, intelligent tutoring, chatbots, VR/AR, predictive analytics, curriculum alignment, AI in pedagogy, micro-credential idea check. Interactive: accuracy-trap calculator, tool evaluation grid, heutagogy slider, idea canvas.
tags:      AI, TVET, Adaptive learning, ITS, Chatbots, VR, Learning analytics, Heutagogy, Micro-credentials
-->

# Applications of AI in TVET

**Session 4 · 05.11.2026 · 🟢 Live** · AI in TVET I, OVGU Magdeburg

Tools · agents · AI in pedagogy · micro-credential idea check

<small>Self-learning unit for this session: [S04 – Applications of AI in TVET](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/Selflearn/S04_Applications_of_AI_in_TVET.md)</small>

                --{{0}}--
Welcome back to our second live session. Before we start: your open questions from the two self-learning sessions. Then we tour the application landscape of AI in vocational education, and in the second half we check your micro-credential ideas together.

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

                --{{0}}--
Answer anonymously in the classroom. We take ten minutes for the most frequent questions before we move on.

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

## 2.2–2.4 Tutors, Chatbots, Simulators

{{1}}
<section>

🧑‍🏫 **ITS:** 40 field studies show a **complicated picture** – few countries ("intelligent regional gap"), focus on test scores, some lack rigour (Wang et al., 2023) · open-source framework turns individual tutors into **collaborative** ones (Arnau-González et al., 2025)

</section>

{{2}}
<section>

💬 **Chatbots:** quick, personalised support (Okonkwo & Ade-Ibijola, 2021) · can connect learners with teachers, social workers, psychologists (Mendoza et al., 2022) · teachers adopt them depending on **innovativeness, trust, ease of use – and social pressure** from colleagues and leaders (482 teachers; Celik et al., 2025)

</section>

{{3}}
<section>

🥽 **VR/AR welding:** safe, material-saving practice (Lavrentieva et al., 2020) · review of 42 studies: mostly **entry-level**, little evidence for distance learning (Chan et al., 2022) · limits: costs, cybersickness, transfer to the real workshop

</section>

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

{{1}}
<section>

AI analyses labour-market data to spot emerging skills and update curricula faster (Ejjami, 2024).

**3E model** (Liao & Zheng, 2025): **E**ducation (AI curriculum design) · **E**xperience (VR training) · **E**mployment (industry partnerships, AI labour-market scans) – tested with 10 vocational schools and 15 industry partners.

</section>

{{2}}
<section>

⚠️ Unequal access and biased algorithms can **widen inequalities**. Needed: infrastructure, continuous teacher training, new roles such as *Vocational AI Curriculum Developer* or *AI Data Protection Specialist* (Ejjami, 2024).

</section>

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

## Playground: AI-Augmented Heutagogy 🪜

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

Each idea gets **one "What works"** and **one "What if …?"**

**What works:**

[[___ ___]]

**What if …?**

[[___ ___]]

**How ready is your idea?**

- [(1)] 🌱 Just a seed
- [(2)] 🌿 Growing
- [(3)] 🌳 Ready for the EU template

## Next: Session 5 📅

**12.11.2026 · 🔵 Self-learning** – describe your micro-credential with the **EU template** and start your learning nuggets.

✍️ Revise your idea with today's feedback.

## References

- Arnau-González, P., Solera-Monforte, S., Wu, Y., & Arevalillo-Herráez, M. (2025). A framework for adapting conversational intelligent tutoring systems to enable collaborative learning. *Expert Systems with Applications, 271*, 126663. https://doi.org/10.1016/j.eswa.2025.126663
- Celik, I., Muukkonen, H., & Siklander, S. (2025). Teacher – artificial intelligence (AI) interaction. *Policy Futures in Education, 24*(1), 164–188. https://doi.org/10.1177/14782103251348551
- Chan, V. S., Haron, H. N. H., Isham, M. I. B. M., & Mohamed, F. B. (2022). VR and AR virtual welding for psychomotor skills: A systematic review. *Multimedia Tools and Applications, 81*, 12459–12493. https://doi.org/10.1007/s11042-022-12293-5
- Chang, D. H., Lin, M. P.-C., Hajian, S., & Wang, Q. Q. (2023). Educational design principles of using AI chatbot that supports self-regulated learning in education. *Sustainability, 15*(17), 12921. https://doi.org/10.3390/su151712921
- du Plooy, E., Casteleijn, D., & Franzsen, D. (2024). Personalized adaptive learning in higher education: A scoping review. *Heliyon, 10*(21), e39630. https://doi.org/10.1016/j.heliyon.2024.e39630
- Ejjami, R. (2024). AI's impact on vocational training and employability. *International Journal for Multidisciplinary Research, 6*(4). https://doi.org/10.36948/ijfmr.2024.v06i04.24967
- Gonzalez-Nucamendi, A., Noguez, J., Neri, L., Robledo-Rella, V., & García-Castelán, R. M. G. (2023). Predictive analytics study to determine undergraduate students at risk of dropout. *Frontiers in Education, 8*, 1244686. https://doi.org/10.3389/feduc.2023.1244686
- Kabudi, T., Pappas, I., & Olsen, D. H. (2021). AI-enabled adaptive learning systems: A systematic mapping of the literature. *Computers and Education: Artificial Intelligence, 2*, 100017. https://doi.org/10.1016/j.caeai.2021.100017
- Korkmaz, Ö., & Aydın, M. N. (2025). Detection of early school drop out in vocational and technical high schools in Turkey. *SAGE Open, 15*(3). https://doi.org/10.1177/21582440251370443
- Lavrentieva, O. O., Arkhypov, I. O., Kuchma, O. I., & Uchitel, A. D. (2020). Use of simulators together with virtual and augmented reality in the system of welders' vocational training. *CEUR Workshop Proceedings, 2547*, 201–216. https://ceur-ws.org/Vol-2547/paper15.pdf
- Liao, J., & Zheng, Y. (2025). Integrating artificial intelligence into vocational education: A technical application framework based on the 3E model. ACM. https://doi.org/10.1145/3745238.3745471
- Mendoza, S., Sánchez-Adame, L. M., Urquiza-Yllescas, J. F., González-Beltrán, B. A., & Decouchant, D. (2022). A model to develop chatbots for assisting the teaching and learning process. *Sensors, 22*(15), 5532. https://doi.org/10.3390/s22155532
- Ng, S. H. S., & Lai, J. W. (2025). AI-augmented heutagogy. *Higher Education Research & Development*. https://doi.org/10.1080/07294360.2025.2564977
- Ning, Y., Zhang, C., Xu, B., Zhou, Y., & Wijaya, T. T. (2024). Teachers' AI-TPACK. *Sustainability, 16*(3), 978. https://doi.org/10.3390/su16030978
- Okonkwo, C. W., & Ade-Ibijola, A. (2021). Chatbots applications in education: A systematic review. *Computers and Education: Artificial Intelligence, 2*, 100033. https://doi.org/10.1016/j.caeai.2021.100033
- Strielkowski, W., Grebennikova, V., Lisovskiy, A., Rakhimova, G., & Vasileva, T. (2025). AI-driven adaptive learning for sustainable educational transformation. *Sustainable Development, 33*, 1921–1947. https://doi.org/10.1002/sd.3221
- Wang, H., Tlili, A., Huang, R., et al. (2023). Examining the applications of intelligent tutoring systems in real educational contexts. *Education and Information Technologies, 28*(7), 9113–9148. https://doi.org/10.1007/s10639-022-11555-x
- Zhao, Y., & Ko, J. (2024). Orchestrating vocational education classrooms for adaptive instruction and collaborative learning. *Cogent Education, 11*(1). https://doi.org/10.1080/2331186X.2024.2351238

**Interactive tools:** [PAIR: Measuring Fairness](https://pair.withgoogle.com/explorables/measuring-fairness/) · [PAIR: Hidden Bias](https://pair.withgoogle.com/explorables/hidden-bias/)

<small>Licence: CC BY 4.0 · Dr. Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), based on the self-learning unit S04; checked by the author.</small>
