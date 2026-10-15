<!--
author:    Dr. Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Presentation
classroom: enable

title:     P05 – Open education with AI: OER, licensing, micro-credentials (Session slides)
comment:   AI in TVET I – Slides for session 5 (self-learning, 12.11.2026): Open Educational Resources, Creative Commons licences, AI output and copyright, the European approach to micro-credentials, digital credentials, learning nuggets. Interactive: licence chooser, TASL attribution generator, ECTS calculator, micro-credential card builder.
tags:      OER, Creative Commons, Copyright, AI, Micro-credentials, Open Badges, TVET
-->

# Open Education with AI

**Session 5 · 12.11.2026 · 🔵 Self-learning** · AI in TVET I, OVGU Magdeburg

OER · licensing · AI & copyright · micro-credentials · learning nuggets

<small>Work through these slides together with the self-learning unit [S05 – OER, Licensing, Micro-credentials](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/Selflearn/S05_OER_Licensing_Microcredentials.md). **Hand-in: 18.11.2026, 23:59 (Moodle).**</small>

                --{{0}}--
Welcome to session five, the last self-learning session. Today you turn your idea into a real micro-credential draft. Along the way you will pick a licence, write correct attributions and build a credential card for your own micro-credential.

## Today's Build 🛠️

``` ascii
 OER &      ──►  Pick a     ──►  AI output   ──►  EU micro-   ──►  Nugget   ──►  HAND-IN
 the 5R          licence         & copyright      credential       plan          draft
 (15 min)        (20 min)        (15 min)         (45 min)         (30 min)      (45 min)
```

{{1}}
<section>

**After today you can …** explain OER · choose a CC licence and attribute correctly · assess AI output and declare AI use · describe a micro-credential with the EU elements · split it into stackable nuggets.

</section>

## 1. Open Educational Resources 📚

> **OER** are learning, teaching and research materials in any format that are in the public domain or published under an open licence that permits no-cost access, re-use, re-purposing, adaptation and redistribution by others (UNESCO, 2019).

{{1}}
<section>

**Why OER in TVET?** Fast-changing technologies need constantly updated material; OER can be adapted to national regulations and translated – also with AI support.

</section>

## Game: The 5R Permissions 🖐️

Drag the right "R" into each gap (Wiley).

Download a LiaScript course to keep a copy → [->[Reuse|(Retain)|Remix]]

Use the course in your class as it is → [->[(Reuse)|Revise|Redistribute]]

Adapt the examples to your trade → [->[Retain|(Revise)|Reuse]]

Merge two nuggets into one → [->[Revise|Reuse|(Remix)]]

Publish your version on GitHub → [->[Retain|(Redistribute)|Remix]]

## AI-Augmented OER 🤖📚

Gillet et al. (2024): **basic OER** (content to consume) vs. **rich OER** (learning phases, learner outputs, learning analytics, **AI support agents or chatbots**).

``` ascii
 Co-creation &  ──►  Teaching &  ──►  Adoption &  ──►  Sharing &  ─┐
 personalisation     learning         impact          discovery    │
       ▲                                                           │
       └─────────────────────── OER lifecycle ◄────────────────────┘
```

{{1}}
<section>

OER are still **scarce** in practice → think about the whole lifecycle: incentives for teachers, links to curricula, participatory design.

**Is your planned micro-credential basic or rich OER?**

- [(basic)] Basic – content to consume
- [(rich)] Rich – with learning phases, outputs, maybe an AI helper
- [(unsure)] Not sure yet

</section>

## 2. Creative Commons Licences 🅭

| Licence | Meaning | OER? |
| --- | --- | --- |
| **CC0** | No rights reserved | ✔ |
| **CC BY** | Attribution | ✔ (recommended) |
| **CC BY-SA** | Attribution + share alike | ✔ |
| **CC BY-NC** | Non-commercial only | limited |
| **CC BY-ND** | No derivatives | ✘ (no revise/remix) |

                --{{0}}--
Every Creative Commons licence except CC zero requires attribution. The additions non-commercial and no derivatives restrict what others may do, which is why they are problematic for open educational resources.

## Playground: Licence Chooser 🎛️

**Give up all rights (public domain)?** <script input="select" value="no" options="no|yes" output="cc0">@input</script>

**Allow adaptations?** <script input="select" value="yes" options="yes|yes, if shared alike|no" output="ccad">@input</script>

**Allow commercial use (e.g. company training)?** <script input="select" value="yes" options="yes|no" output="cccom">@input</script>

<script modify="false" style="display:block">
const pd = "@input(`cc0`)" === "yes", ad = "@input(`ccad`)", com = "@input(`cccom`)" === "yes";
let code, url, oer, why;
if (pd) { code = "CC0 1.0"; url = "https://creativecommons.org/publicdomain/zero/1.0/"; oer = "✔ OER"; why = "No conditions at all – maximum freedom, but no attribution required."; }
else {
  let parts = ["by"];
  if (!com) parts.push("nc");
  if (ad === "no") parts.push("nd"); else if (ad !== "yes") parts.push("sa");
  code = "CC " + parts.join("-").toUpperCase() + " 4.0";
  url = "https://creativecommons.org/licenses/" + parts.join("-") + "/4.0/";
  if (parts.includes("nd")) { oer = "✘ Not OER"; why = "No derivatives: nobody may revise or remix your nugget."; }
  else if (parts.includes("nc")) { oer = "◐ Limited OER"; why = "Non-commercial: companies may not use it in paid training – a problem for TVET."; }
  else { oer = "✔ OER"; why = parts.includes("sa") ? "Adaptations must use the same licence." : "The recommended licence for OER: free use with attribution."; }
}
`HTML: <div style="border:3px solid #111;border-radius:10px;padding:12px;display:inline-block;min-width:260px"><div style="font-size:1.6em;font-weight:bold">${code}</div><div>${oer}</div><p style="margin:6px 0">${why}</p><a href="${url}" target="_blank" rel="noopener">${url}</a></div>`
</script>

<small>The official tool: [Creative Commons License Chooser](https://creativecommons.org/chooser/)</small>

                --{{0}}--
Try all combinations. Which one do you want for your nuggets, if learners and teachers should adapt them freely and also use them in company training?

## Check Your Licence Knowledge ✅

**You want learners and teachers to adapt your nuggets freely, also for company training.**

- [( )] CC BY-NC-ND
- [(X)] CC BY
- [( )] All rights reserved

**You combine a CC BY-SA image with your own text. Under which licence must you publish the adapted image?**

- [( )] Any licence
- [(X)] CC BY-SA (share alike)
- [( )] CC0

## Playground: TASL Attribution Generator 🏷️

Every re-used work needs **T**itle · **A**uthor · **S**ource · **L**icence.

**Title:** <script input="text" value="Weld seam inspection" output="tT" input-always-active>@input</script>

**Author:** <script input="text" value="Jane Doe" output="tA" input-always-active>@input</script>

**Source (URL):** <script input="text" value="https://example.org/photo" output="tS" input-always-active>@input</script>

**Licence:** <script input="select" value="CC BY 4.0" options="CC0 1.0|CC BY 4.0|CC BY-SA 4.0|CC BY-NC 4.0|CC BY-ND 4.0|CC BY-NC-SA 4.0" output="tL">@input</script>

<script modify="false" style="display:block">
const e = s => s.replace(/</g,"&lt;");
const T = e(`@input(`tT`)`), A = e(`@input(`tA`)`), S = e(`@input(`tS`)`), L = "@input(`tL`)";
const slug = L === "CC0 1.0" ? "publicdomain/zero/1.0" : "licenses/" + L.replace("CC ","").replace(" 4.0","").toLowerCase() + "/4.0";
const lurl = "https://creativecommons.org/" + slug + "/";
const missing = [["Title",T],["Author",A],["Source",S]].filter(([,v]) => v.trim() === "").map(([k]) => k);
`HTML: <div style="font-family:monospace;border-left:6px solid #16a34a;padding:8px 12px">"${T}" by ${A}, ${S}, ${L} (${lurl})</div>
<p><b>LiaScript / Markdown:</b></p><div style="font-family:monospace;font-size:0.85em;border-left:6px solid #2563eb;padding:8px 12px">"${T}" by ${A}, [Source](${S}), [${L}](${lurl})</div>
<p>${missing.length ? "⚠️ Missing: " + missing.join(", ") : "✅ TASL complete"}</p>`
</script>

<small>Find openly licensed images: [Openverse](https://openverse.org) · [Wikimedia Commons](https://commons.wikimedia.org)</small>

## 3. AI Output and Copyright ©️🤖

{{1}}
<section>

**What we know (status 2026)**

- Copyright protects **human** creative work – purely AI-generated content without sufficient human contribution is generally **not protected** in the EU and US (see U.S. Copyright Office, 2025)
- **Your** selection, arrangement and revision of AI output can be protected
- Tool **terms of use** regulate what you may do with output – read them
- AI output can unintentionally reproduce protected material – check before publishing
- EU AI Act, Art. 50: synthetic content must be identifiable as AI-generated

</section>

{{2}}
<section>

**Declare your AI use** in every OER:

```text
Created with AI support (Claude, ChatGPT). All content was checked,
revised and selected by the author. Licence: CC BY 4.0.
```

</section>

## Dilemma: The Comic-Style Illustration 🎨

You generated an illustration with an image AI **in the style of a well-known comic artist**. Would you publish it in your OER?

- [(yes)] Yes – style is not protected
- [(no)] No – too close to the artist's work and reputation
- [(depends)] Depends – I would check terms of use and similarity first
- [(change)] I would generate a different style instead

**Your reasoning (→ AI tools log):**

[[___ ___]]

                --{{0}}--
There is no simple answer. Think about copyright, but also about fairness towards the artist, and about what you model for your learners.

## 4. The European Approach to Micro-credentials 🇪🇺

> A **micro-credential** is the record of the learning outcomes that a learner has acquired following a small volume of learning. These learning outcomes have been assessed against transparent and clearly defined standards (European Commission, 2021; Council of the European Union, 2022).

{{1}}
<section>

- **Owned by the learner**, shareable, portable (e.g. Europass digital wallet)
- Standalone or **stacked** – but the **receiving organisation** decides on stacking and recognition

</section>

{{2}}
<section>

🌐 **UNESCO expert consensus** (47 experts; Oliver, 2022): focused achievement · assessment against clear standards · trusted provider · standalone value · quality assurance. **Open problems:** competing definitions, QA outside regulated education, **little evidence so far that micro-credentials work**, risk of diverting funds from formal education → *complement, don't replace* full qualifications.

</section>

## Game: Mandatory or Not? 📋

Which of these are **mandatory** elements of the EU standard?

- [[X]] Learning outcomes
- [[X]] Type of assessment
- [[ ]] Price of the course
- [[X]] Notional workload (ECTS where possible)
- [[ ]] Name of the AI tool used
- [[X]] Awarding body
- [[X]] Type of quality assurance
- [[ ]] Number of nuggets

{{1}}
<section>

**All mandatory elements:** learner identification · title · country/region · awarding body · date of issuing · learning outcomes · notional workload · level (EQF, if applicable) · type of assessment · form of participation · type of quality assurance

**Ten principles:** quality · transparency · relevance · valid assessment · learning pathways · recognition · portable · learner-centred · authentic · information and guidance

</section>

## Playground: Workload → ECTS ⏱️

Total learning hours of your micro-credential (all nuggets + assessment):

<script input="range" min="5" max="150" step="5" value="30" output="hrs">@input</script> hours

<script modify="false" style="display:block">
const h = Number(@input(`hrs`));
const lo = h / 30, hi = h / 25;
const nug = Math.round(h * 60 / 15);
`HTML: <p style="font-size:1.3em">≈ <b>${lo.toFixed(1)} – ${hi.toFixed(1)} ECTS</b></p><p>(1 ECTS ≈ 25–30 hours of learning, as in the S05 example)</p><p>🧩 For comparison: that is the time of about <b>${nug}</b> nuggets of 15 minutes – so most of the workload must come from practice tasks, projects and assessment, not from reading nuggets.</p>`
</script>

                --{{0}}--
Move the slider to your planned workload. Many first drafts promise one ECTS but contain only two hours of content. Plan the practice tasks and the assessment into the workload.

## Playground: Your Micro-credential Card 🎫

**Title:** <script input="text" value="AI-supported fault diagnosis in automotive electrics" output="mT" input-always-active>@input</script>

**Awarding body / country:** <script input="text" value="OVGU Magdeburg · Germany, Saxony-Anhalt" output="mB" input-always-active>@input</script>

**Learning outcome:** <script input="text" value="Learners can evaluate an AI diagnosis suggestion against measurement data" output="mO" input-always-active>@input</script>

**EQF level:** <script input="select" value="4" options="1|2|3|4|5|6|7|8|not applicable" output="mE">@input</script>

**Assessment:** <script input="text" value="Practical task + reflection" output="mA" input-always-active>@input</script>

**Participation:** <script input="select" value="online, self-paced" options="online, self-paced|on-site|blended" output="mP">@input</script>

**Quality assurance:** <script input="text" value="Internal review by the university" output="mQ" input-always-active>@input</script>

<script modify="false" style="display:block">
const e = s => s.replace(/</g,"&lt;");
const T = e(`@input(`mT`)`), B = e(`@input(`mB`)`), O = e(`@input(`mO`)`), E = "@input(`mE`)", A = e(`@input(`mA`)`), P = "@input(`mP`)", Q = e(`@input(`mQ`)`);
const h = Number(@input(`hrs`));
const ok = x => x.trim().length > 2 ? 1 : 0;
const filled = ok(T) + 2 * ok(B) + ok(O) + ok(A) + ok(Q) + 3;
`HTML: <div style="max-width:560px;border-radius:16px;padding:16px;color:#fff;background:linear-gradient(135deg,#1e3a8a,#0f766e);box-shadow:0 4px 14px rgba(0,0,0,0.25)">
<div style="display:flex;justify-content:space-between;font-size:0.75em;letter-spacing:2px"><span>EUROPEAN MICRO-CREDENTIAL · DRAFT</span><span>EQF ${E}</span></div>
<h3 style="margin:8px 0;color:#fff">${T}</h3>
<div style="font-size:0.9em">🏛️ ${B}</div>
<div style="margin-top:8px;font-size:0.95em">✅ ${O}</div>
<div style="display:flex;flex-wrap:wrap;gap:12px;margin-top:10px;font-size:0.85em"><span>⏱️ ${h} h ≈ ${(h/30).toFixed(1)}–${(h/25).toFixed(1)} ECTS</span><span>📝 ${A}</span><span>💻 ${P}</span><span>🔎 ${Q}</span></div>
<div style="margin-top:8px;font-size:0.75em;opacity:0.85">Learner: «name» · Issued: «date»</div></div>
<p>EU mandatory elements covered in this card: <b>${filled} / 11</b> (learner name and date are added at issuing)</p>`
</script>

                --{{0}}--
Fill in your own micro-credential. The workload comes from the ECTS slider on the previous slide. Take a screenshot: it is a great start for your hand-in and for your pitch.

## Digital Credentials 🏅

Paper can be forged – digital credentials can be **verified, shared, stored** and carry more information (Delgado Kloos et al., 2025).

{{1}}
<section>

| Format | What it is |
| --- | --- |
| **Open Badges 3.0** | Badge with embedded metadata ([spec](https://www.imsglobal.org/spec/ob/v3p0/) · [openbadges.org](https://openbadges.org)) |
| **European Learning Model (ELM)** | EU data model behind [European Digital Credentials](https://europass.europa.eu/en/stakeholders/european-digital-credentials) |

Both are based on **W3C Verifiable Credentials** → this is where your **optional badge** (assessment component 3) fits in.

</section>

{{2}}
<section>

**Will you design a badge?**

- [(yes)] Yes 🏅
- [(maybe)] Maybe
- [(no)] No, I focus on the core components

</section>

## 5. Learning Nuggets 🧩

**One nugget = one objective = 5–15 minutes**

``` ascii
 Micro-credential (e.g. 1 ECTS)
 ├── Nugget 1  Acquire:  basic concept              + quiz
 ├── Nugget 2  Acquire:  example from the workplace + quiz
 ├── Nugget 3  Deepen:   apply in a case           + task
 ├── Nugget 4  Deepen:   evaluate AI output        + task
 └── Nugget 5  Create:   own product / transfer    + assessment
```

{{1}}
<section>

**Design principles:** one objective with an action verb (Bloom) · authentic workplace example · at least one interactive element · short summary + link to next nugget · open licence + AI declaration

</section>

## How AI Helps – and Where You Decide 🤝

{{1}}
<section>

| AI can … | You decide … |
| --- | --- |
| suggest a nugget structure from your outcomes | the learning objectives |
| draft texts and quizzes | whether facts are correct |
| generate case variants | if cases are authentic |
| translate | the didactic quality |

</section>

{{2}}
<section>

**Two research examples**

- **AI for the first draft:** ChatGPT, DeepSeek, NotebookLM … gave a useful *first draft* of a micro-credential design – refined iteratively with instructors (Delgado Kloos et al., 2025)
- **AI for the skill gap:** NLP on job descriptions in the urban renewable energy sector → skill clusters → co-designed basket of **74 stackable micro-credentials** (De Rosa et al., 2024) – *a model for justifying your skill gap in the pitch*

</section>

## Plan Your Nuggets 🗂️

List your 3–6 nuggets (one line each: level · objective · interactive element):

[[___ ___ ___ ___ ___]]

**Which level is your last nugget?**

- [(acquire)] Acquire
- [(deepen)] Deepen
- [(create)] Create

                --{{0}}--
Write your nugget plan here as a first draft, then copy it into your hand-in document. A good micro-credential climbs from acquire to create.

## Hand-in for Session 5 📤

**Deadline: 18.11.2026, 23:59 · Moodle**

{{1}}
<section>

1. **Micro-credential draft** – all EU mandatory elements (use your card!)
2. **Nugget plan** – 3–6 nuggets: objective · interactive element · level
3. **First nugget draft** – LiaScript `.md` or GitHub link (does not need to be finished)
4. **AI tools log** – updated

</section>

{{2}}
<section>

🎤 **19.11.2026:** you pitch your micro-credential (10 min + 3 min questions). The S06 unit and the [presentation template](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/AI_in_TVET_I_WiSe_2026_2027/00_Organisation/Template_LiaScript_Presentation.md) help you build it.

</section>

## References

- Council of the European Union. (2022). *Council Recommendation of 16 June 2022 on a European approach to micro-credentials for lifelong learning and employability* (2022/C 243/02). https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022H0627(02)
- Creative Commons. (n.d.). *About CC licenses*. https://creativecommons.org/share-your-work/cclicenses/
- De Rosa, M., Glumac, O., Bianco, V., & Pallonetto, F. (2024). A micro-credential approach for life-long learning in the urban renewable energy sector. *Renewable Energy, 228*, 120660. https://doi.org/10.1016/j.renene.2024.120660
- Delgado Kloos, C., Alario-Hoyos, C., & Kemcha, R. (2025). How challenges become opportunities: Micro-credentials and artificial intelligence. In *2025 IEEE EDUCON*. https://doi.org/10.1109/EDUCON62633.2025.11016509
- European Commission. (2021). *A European approach to micro-credentials* [Factsheet]. Publications Office of the European Union.
- European Union. (2024). *Regulation (EU) 2024/1689 (Artificial Intelligence Act)*. https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- Gillet, D., Notari, M., Spaenlehauer, B., & Reidy, T. (2024). Implementation framework and strategies for AI-augmented open educational resources (OER). In *2024 ITHET*. https://doi.org/10.1109/ITHET61869.2024.10837633
- Oliver, B. (2022). *Towards a common definition of micro-credentials*. UNESCO. https://unesdoc.unesco.org/ark:/48223/pf0000381668
- UNESCO. (2019). *Recommendation on Open Educational Resources (OER)*. https://www.unesco.org/en/legal-affairs/recommendation-open-educational-resources-oer
- U.S. Copyright Office. (2025). *Copyright and artificial intelligence, Part 2: Copyrightability*. https://www.copyright.gov/ai/
- Wiley, D. (n.d.). *Defining the "open" in open content and open educational resources*. https://opencontent.org/definition/

**Interactive tools:** [CC License Chooser](https://creativecommons.org/chooser/) · [Openverse](https://openverse.org) · [Open Badges](https://openbadges.org) · [European Digital Credentials](https://europass.europa.eu/en/stakeholders/european-digital-credentials)

<small>Licence: CC BY 4.0 · Dr. Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), based on the self-learning unit S05; checked by the author.</small>
