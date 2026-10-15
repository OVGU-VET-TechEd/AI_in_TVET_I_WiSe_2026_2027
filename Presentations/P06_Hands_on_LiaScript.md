<!--
author:    Dr. Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Presentation
classroom: enable

title:     P06 – Hands-on LiaScript & Pitch Presentations (Session slides)
comment:   AI in TVET I – Slides for session 6 (live, 19.11.2026): LiaScript syntax live, GitHub workflow, building nuggets with AI, 10-minute pitch, panel feedback, final submission and UNESCO AI CFT reflection. Interactive: syntax arcade, link builder, pitch planner, peer rating, competency radar.
tags:      LiaScript, GitHub, OER, Pitch, Micro-credentials, UNESCO, Reflection
-->

# Hands-on LiaScript & Pitch Day

**Session 6 · 19.11.2026 · 🟢 Live** · AI in TVET I, OVGU Magdeburg

LiaScript live · GitHub workflow · nuggets with AI · **your pitches** 🎤

<small>Self-learning unit for this session: [S06 – Hands-on LiaScript](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/Selflearn/S06_Hands_on_LiaScript.md)</small>

                --{{0}}--
Welcome to our final session of AI in TVET one. First a short LiaScript power-up, then the stage is yours: every group pitches its micro-credential to our decision panel.

## How Ready Are You? 🚦

**My pitch file is …**

- [(1)] 😱 not started
- [(2)] 🛠️ half done
- [(3)] ✅ finished, but untested
- [(4)] 🚀 finished and tested via the LiaScript link

**One word for how you feel right now:**

[[___]]

## Today's Agenda 🗓️

| Time (approx.) | Block |
| --- | --- |
| 09:00 | LiaScript power-up: syntax arcade, GitHub link builder |
| 09:20 | Pitch planner & final checks |
| 09:30 | 🎤 **Pitches** – 10 min + 3 min panel questions each |
| end | Final submission, UNESCO AI CFT self-check, outlook |

## 1. What Is LiaScript? 📄➡️🎓

Markdown + superpowers: quizzes, animations, text-to-speech, videos, code – **without an LMS**. Plain text → easy to version, translate and **generate with AI**.

``` ascii
 your-nugget.md  ──►  GitHub (raw link)  ──►  liascript.github.io/course/?<raw link>
   (plain text)        (storage, versions)       (interactive course in the browser)
```

{{1}}
<section>

`mode: Presentation` → one slide at a time (pitch) · `mode: Textbook` → whole page (self-learning nuggets)

**Fun fact:** these slides *are* a LiaScript file. Every playground in this course is just text + a few lines of JavaScript.

</section>

## Syntax Arcade 1: Quizzes 🕹️

<section>

**Single choice** · `- [(X)] correct`

Which tool measures electrical voltage?

- [( )] Torque wrench
- [(X)] Multimeter
- [( )] Caliper

</section>

{{1}}
<section>

**Multiple choice** · `- [[X]] correct`

Which are personal protective equipment for welding?

- [[X]] Welding helmet
- [[ ]] Sandals
- [[X]] Leather gloves

</section>

{{2}}
<section>

**Text input** · `[[welding]]` · **Selection** · `[[a|(b)|c]]` · **Drag & drop** · `[->[a|(b)|c]]`

Joining metals by melting them together is called [[welding]].

The header line `mode: ` [[Textbook|(Presentation)|Slides]] shows one slide at a time.

LiaScript files are written in [->[HTML|(Markdown)|Word]].

</section>

                --{{0}}--
Every quiz type you saw in this seminar takes one line of text. Hover over the grey syntax labels and use them as a cheat sheet for your nuggets.

## Syntax Arcade 2: Animations & Voice 🔊

```markdown
                --{{1}}--
This text is read aloud on click 1.

{{1}}
This block appears on click 1.
```

{{1}}
<section>

👋 I appeared on the first click – and the narrator is reading the speaker note now.

</section>

                --{{1}}--
Hello! I am the built-in narrator. Every speaker note in your pitch can be read aloud, which is great for accessibility and for self-learning nuggets.

{{2}}
<section>

**Survey (no right answer):** `- [(1)] option` · **Text survey:** `[[___]]`

Which LiaScript feature will you use in your nuggets?

- [(quiz)] Quizzes
- [(anim)] Step-by-step animations
- [(tts)] Text-to-speech
- [(video)] Videos
- [(code)] Executable code

</section>

## Syntax Arcade 3: Run Code in a Slide 💻

LiaScript can execute code. Change the numbers and press **▶**.

```js
// Workload check for your micro-credential
const nuggets = 5;          // number of nuggets
const minutesPerNugget = 15;
const practiceHours = 20;   // tasks, project, assessment
const hours = nuggets * minutesPerNugget / 60 + practiceHours;
`${hours} h ≈ ${(hours / 30).toFixed(1)}–${(hours / 25).toFixed(1)} ECTS`
```
<script>@input</script>

{{1}}
<section>

Under the code block, one line does the magic: `<script>@input</script>`

</section>

## Syntax Arcade 4: Media & Embeds 🎬

```markdown
![Image description](https://…/image.png)
!?[Video title](https://www.youtube.com/watch?v=…)
?[Audio](https://…/file.mp3)
??[Any website](https://…)
```

{{1}}
<section>

`??[…]` embeds a whole website – like the LiaScript LiveEditor, where you can test your file right now:

??[LiaScript LiveEditor](https://liascript.github.io/LiveEditor/)

</section>

{{2}}
<section>

🖼️ Always add image credits (TASL, see S05).

</section>

## Speed Check ⚡

Which line creates a **correct single-choice** option?

- [( )] `- [[X]] option`
- [(X)] `- [(X)] option`
- [( )] `- {{X}} option`

Which line makes a block appear on the **second** click?

- [( )] `--{{2}}--`
- [(X)] `{{2}}`
- [( )] `[[2]]`

Why must you **never** indent text by 4 or more spaces?

- [( )] LiaScript deletes the text.
- [(X)] Markdown renders it as a code block.
- [( )] The narrator cannot read it.

## 2. GitHub Workflow 🐙

{{1}}
<section>

1. **Sign up** at [github.com](https://github.com) (university email)
2. **Create a repository**, e.g. `AI_in_TVET_<your-topic>` (public)
3. **Add file** → `nugget_01.md` → paste LiaScript → *Commit changes*
4. Open the file → **Raw** → copy the link
5. Open: `https://liascript.github.io/course/?<raw link>`
6. Media: folder `media/`, link images via their raw link

</section>

{{2}}
<section>

💡 Develop in the [LiveEditor](https://liascript.github.io/LiveEditor/), then copy the final version to GitHub.

</section>

## Playground: Link Builder 🔗

**GitHub user or organisation:** <script input="text" value="OVGU-VET-TechEd" output="gU" input-always-active>@input</script>

**Repository:** <script input="text" value="AI_in_TVET_I_WiSe_2026_2027" output="gR" input-always-active>@input</script>

**Branch:** <script input="text" value="main" output="gB" input-always-active>@input</script>

**File path:** <script input="text" value="Presentations/P06_Hands_on_LiaScript.md" output="gF" input-always-active>@input</script>

<script modify="false" style="display:block">
const c = s => s.trim().replace(/^\/+|\/+$/g,"").replace(/\s/g,"%20").replace(/[<>"]/g,"");
const u = c(`@input(`gU`)`), r = c(`@input(`gR`)`), b = c(`@input(`gB`)`) || "main", f = c(`@input(`gF`)`);
const raw = `https://raw.githubusercontent.com/${u}/${r}/${b}/${f}`;
const lia = `https://liascript.github.io/course/?${raw}`;
const ok = u && r && /\.md$/i.test(f);
`HTML: <p><b>Raw link:</b><br><code style="word-break:break-all">${raw}</code></p>
<p><b>LiaScript link</b> (put this in Moodle):<br><a href="${lia}" target="_blank" rel="noopener" style="word-break:break-all">${lia}</a></p>
<p>${ok ? "✅ Looks good – click to test it." : "⚠️ Check user, repository and that the file ends with <code>.md</code>."}</p>`
</script>

                --{{0}}--
Type in your own repository and file name, click the generated link and check that your pitch opens. This is the link you hand in.

## 3. Building a Nugget with AI 🤖✍️

Give the AI a **template** so the LiaScript syntax stays correct – e.g. the [course presentation template](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/AI_in_TVET_I_WiSe_2026_2027/00_Organisation/Template_LiaScript_Presentation.md) or the prompt in S06.

{{1}}
<section>

**Then revise – your job, not the AI's:**

- [ ] Facts correct? Sources added and checked?
- [ ] Learning objective really trained and assessed?
- [ ] Example authentic for the vocational field?
- [ ] Language suitable for the target group?
- [ ] Quiz distractors plausible, feedback helpful?
- [ ] Syntax renders in LiaScript (tested!)?
- [ ] Licence and AI declaration added?

📓 Document prompt, output and changes in your **AI tools log**.

</section>

## 4. Playground: Pitch Planner ⏱️

Plan your 10 minutes (in minutes):

| Slide | Content | Minutes |
| --- | --- | --- |
| 1 | Title & value proposition | <script input="range" min="0" max="3" step="0.5" value="0.5" output="p1">@input</script> |
| 2 | Skill gap (evidence) | <script input="range" min="0" max="3" step="0.5" value="1.5" output="p2">@input</script> |
| 3 | Target group & outcomes | <script input="range" min="0" max="3" step="0.5" value="1.5" output="p3">@input</script> |
| 4 | Nuggets & workload | <script input="range" min="0" max="3" step="0.5" value="1.5" output="p4">@input</script> |
| 5 | Live demo of one nugget | <script input="range" min="0" max="4" step="0.5" value="2" output="p5">@input</script> |
| 6 | Assessment & recognition | <script input="range" min="0" max="3" step="0.5" value="1" output="p6">@input</script> |
| 7 | AI integration | <script input="range" min="0" max="3" step="0.5" value="1" output="p7">@input</script> |
| 8 | Ask to the panel & references | <script input="range" min="0" max="3" step="0.5" value="1" output="p8">@input</script> |

<script modify="false" style="display:block">
const v = [@input(`p1`),@input(`p2`),@input(`p3`),@input(`p4`),@input(`p5`),@input(`p6`),@input(`p7`),@input(`p8`)].map(Number);
const total = v.reduce((a,b) => a+b, 0);
const cols = ["#1e3a8a","#2563eb","#0ea5e9","#14b8a6","#16a34a","#84cc16","#f59e0b","#ef4444"];
const bar = v.map((x,i) => x > 0 ? `<div title="Slide ${i+1}: ${x} min" style="background:${cols[i]};width:${x/Math.max(10,total)*100}%;height:28px;color:#fff;font-size:0.8em;text-align:center;line-height:28px">${i+1}</div>` : "").join("");
const msg = total > 10 ? `⏰ <b>${total} min – too long!</b> Cut ${total-10} min. The panel will stop you at 10:00.` : (total < 9 ? `🕳️ <b>${total} min</b> – you have time left. Strengthen the live demo or the evidence.` : `✅ <b>${total} min</b> – perfect timing.`);
const demo = v[4] < 1.5 ? "<br>💡 The live demo is the most convincing part – give it at least 1.5 min." : "";
`HTML: <div style="display:flex;width:100%;border:1px solid #94a3b8;border-radius:6px;overflow:hidden">${bar}</div><p>${msg}${demo}</p>`
</script>

                --{{0}}--
The default values follow the recommendation from S06. Adjust them to your pitch. If your bar turns red, you are over time.

## Pitch Criteria 🏆

| Criterion | Expectation |
| --- | --- |
| Content | Clear skill gap, measurable outcomes, UNESCO alignment |
| Persuasiveness | Convincing value proposition for the panel |
| LiaScript use | Slides, step-by-step animations, ≥ 1 interactive element |
| Delivery | Free speech, time kept, audience-oriented |
| Sources & AI | References (APA 7), image licences, AI use declared |

{{1}}
<section>

🎭 **The panel:** provost · curriculum director · industry partners. Today, **you** are the panel for the other groups.

</section>

## 🎤 Pitch Time!

**Stage rules**

1. Open your pitch via **your LiaScript link**
2. Start the classroom so the panel can vote in your poll
3. 10 minutes – the timer is strict ⏰
4. 3 minutes panel questions

{{1}}
<section>

**Panel task during each pitch:** note one strength and one question.

</section>

                --{{0}}--
Good luck to all groups. Remember: the panel wants to know why this micro-credential is needed, who it is for, and why they should trust it.

## Panel Vote 🗳️ (repeat for each group)

**Group:** <script input="text" value="Group 1" output="grp" input-always-active>@input</script>

**Would you fund this micro-credential?**

- [(1)] Yes, as presented
- [(2)] Yes, with changes
- [(3)] Not yet

**Strongest point:**

[[___]]

**Question for the group:**

[[___]]

                --{{0}}--
Use this slide for every group. Change the group name, vote, and write your strongest point and your question.

## Playground: Quick Peer Rating ⭐

Rate the last pitch from 1 to 5:

| Criterion | Rating |
| --- | --- |
| Content | <script input="range" min="1" max="5" step="1" value="4" output="r1">@input</script> |
| Persuasiveness | <script input="range" min="1" max="5" step="1" value="4" output="r2">@input</script> |
| LiaScript use | <script input="range" min="1" max="5" step="1" value="4" output="r3">@input</script> |
| Delivery | <script input="range" min="1" max="5" step="1" value="4" output="r4">@input</script> |
| Sources & AI | <script input="range" min="1" max="5" step="1" value="4" output="r5">@input</script> |

<script modify="false" style="display:block">
const n = ["Content","Persuasiveness","LiaScript use","Delivery","Sources & AI"];
const v = [@input(`r1`),@input(`r2`),@input(`r3`),@input(`r4`),@input(`r5`)].map(Number);
const avg = v.reduce((a,b) => a+b, 0) / 5;
const best = n[v.indexOf(Math.max(...v))], tip = n[v.indexOf(Math.min(...v))];
const g = `@input(`grp`)`.replace(/</g,"&lt;");
`HTML: <div style="border:2px solid #f59e0b;border-radius:12px;padding:10px;max-width:480px"><b>${g}</b><div style="font-size:1.6em">${"★".repeat(Math.round(avg))}${"☆".repeat(5-Math.round(avg))} <small>${avg.toFixed(1)}</small></div><p>👍 Strongest: <b>${best}</b><br>🔧 Work on: <b>${tip}</b></p></div>`
</script>

<small>For informal peer feedback only – grading is done by the lecturer.</small>

## 5. Final Submission: 15.01.2027 📦

- [ ] **Micro-credential** with all EU mandatory elements
- [ ] **Learning nuggets** as LiaScript files on GitHub (working links)
- [ ] **Pitch presentation** (LiaScript)
- [ ] *Optional:* **digital badge** (image + Open Badges metadata)
- [ ] **AI co-design documentation & reflection** (PDF): AI tools log + reflection paper, 1,000–1,500 words, using the **UNESCO AI Competency Framework for Teachers**
- [ ] Licences, image credits and AI declaration in every file

                --{{0}}--
Tick what you already have. Everything goes into Moodle by the fifteenth of January.

## Playground: UNESCO AI CFT – Where Are You Now? 🧭

Repeat the self-check from session 1 – the difference is great material for your **reflection paper**.

**0** = not yet · **1** = Acquire · **2** = Deepen · **3** = Create

| Dimension | Your level |
| --- | --- |
| 1 Human-centred mindset | <script input="range" min="0" max="3" step="1" value="2" output="cft1">@input</script> |
| 2 Ethics of AI | <script input="range" min="0" max="3" step="1" value="2" output="cft2">@input</script> |
| 3 AI foundations and applications | <script input="range" min="0" max="3" step="1" value="2" output="cft3">@input</script> |
| 4 AI pedagogy | <script input="range" min="0" max="3" step="1" value="1" output="cft4">@input</script> |
| 5 AI for professional development | <script input="range" min="0" max="3" step="1" value="1" output="cft5">@input</script> |

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
const poly = `<polygon points="${v.map((x,i) => pt(i, R*x/3).join(",")).join(" ")}" fill="rgba(22,163,74,0.35)" stroke="#16a34a" stroke-width="2"/>`;
const lvl = ["–","Acquire","Deepen","Create"];
const list = v.map((x,i) => `<li><b>${dims[i]}</b>: ${x === 0 ? "not yet" : lvl[x] + " → <i>" + comp[i][x-1] + "</i>"}</li>`).join("");
const next = v.indexOf(Math.min(...v));
`HTML: <div style="display:flex;flex-wrap:wrap;gap:16px;align-items:center"><svg viewBox="0 0 320 300" style="width:300px;max-width:100%">${grid}${axes}${poly}</svg><div style="flex:1;min-width:240px"><ul>${list}</ul><p>🚀 <b>Growth area for AI in TVET II:</b> ${dims[next]}${v[next] < 3 ? " – next competency: <i>" + comp[next][v[next]] + "</i>" : ""}</p></div></div>`
</script>

                --{{0}}--
Compare this radar with your screenshot from session one. In your reflection paper, pick two dimensions where you moved, and give concrete evidence from your AI tools log.

## Reflection Starter ✍️

For your reflection paper (1,000–1,500 words):

{{1}}
<section>

1. Where did AI **really** help you build your micro-credential – and where did it mislead you?
2. Which decisions did you deliberately keep **human**? (→ human-centred mindset)
3. Which ethical issue did you meet in practice? (→ ethics of AI)
4. What will you do differently as a TVET teacher? (→ AI pedagogy, professional development)

</section>

{{2}}
<section>

**One sentence you will definitely put in your reflection:**

[[___ ___]]

</section>

## Thank You & Outlook 🎉

**AI in TVET I – done!** 🎓

{{1}}
<section>

**Coming up: AI in TVET II** · from **03.12.2026** · Thursdays, 09:00–12:00 → [course website](https://ovgu-vet-teched.github.io/AI_in_TVET_II_WiSe_2026_2027/)

</section>

{{2}}
<section>

**How would you rate this seminar overall?**

- [(1)] ⭐
- [(2)] ⭐⭐
- [(3)] ⭐⭐⭐
- [(4)] ⭐⭐⭐⭐
- [(5)] ⭐⭐⭐⭐⭐

**One thing to keep, one thing to change:**

[[___ ___]]

</section>

## References

- 1EdTech. (2024). *Open Badges specification v3.0*. https://www.imsglobal.org/spec/ob/v3p0/
- Council of the European Union. (2022). *Council Recommendation on a European approach to micro-credentials for lifelong learning and employability* (2022/C 243/02). https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022H0627(02)
- LiaScript. (n.d.). *LiaScript documentation*. https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md
- UNESCO. (2024b). *AI competency framework for teachers*. https://doi.org/10.54675/ZJTE2084

**Tools:** [LiaScript LiveEditor](https://liascript.github.io/LiveEditor/) · [GitHub](https://github.com) · [Presentation template](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/AI_in_TVET_I_WiSe_2026_2027/00_Organisation/Template_LiaScript_Presentation.md)

<small>Licence: CC BY 4.0 · Dr. Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), based on the self-learning unit S06; checked by the author.</small>
