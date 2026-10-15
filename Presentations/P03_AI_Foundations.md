<!--
author:    Dr. Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.0.0
language:  en
narrator:  UK English Female
mode:      Presentation
classroom: enable

title:     P03 – AI foundations: vocabulary, models, algorithms and workflows (Session slides)
comment:   AI in TVET I – Slides for session 3 (self-learning, 29.10.2026): data, weights, models, algorithms, learning paradigms, neural networks, AI workflows and agents, UNESCO AI Competency Framework for Students. Interactive: weights playground, gradient-descent lab, TensorFlow Playground, Teachable Machine.
tags:      AI, TVET, Machine learning, Neural networks, Bias, Agents, UNESCO
-->

# AI Foundations

**Session 3 · 29.10.2026 · 🔵 Self-learning** · AI in TVET I, OVGU Magdeburg

Vocabulary · models · algorithms · workflows

<small>Work through these slides together with the self-learning unit [S03 – AI Foundations](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/main/Selflearn/S03_AI_Foundations.md). **Hand-in: 04.11.2026, 23:59 (Moodle).**</small>

                --{{0}}--
Welcome to session three. Today you become a machine learning engineer for an afternoon. You will move weights by hand, watch a network learn, and train your own image classifier. No programming needed.

## Today's Lab Plan 🧪

| Station | What you do | Time |
| --- | --- | --- |
| 1 Vocabulary | Build the map from data to output | 15 min |
| 2 Weights | Be the training algorithm yourself | 15 min |
| 3 Data | Spot the bias | 15 min |
| 4 Paradigms | Sort tasks into learning types | 10 min |
| 5 Neural networks | Gradient descent lab + TensorFlow Playground | 30 min |
| 6 Hands-on | Train a model with Teachable Machine | 30 min |
| 7–8 Workflows & agents | From model to classroom | 20 min |
| 9 Reading | UNESCO AI CFT for Students | 45 min |

## 1. The Vocabulary Map 🗺️

``` ascii
  DATA ──────────► ALGORITHM ──────────► MODEL ──────────► OUTPUT
 (examples,        (learning procedure,  (learned weights,  (prediction,
  features,         e.g. gradient         structure)         classification,
  labels)           descent)                                 generated text)
      │                                      ▲
      └──────────── TRAINING ────────────────┘        INFERENCE = using the model
```

{{1}}
<section>

| Term | TVET example |
| --- | --- |
| **Data** | 10,000 photos of weld seams |
| **Feature** | Seam width, porosity, colour |
| **Label** | "OK" / "defect" |
| **Algorithm** | Decision tree learning, gradient descent |
| **Model** | Trained weld-inspection classifier |
| **Weights** | Millions of values in a neural network |
| **Training** | Adjusting weights so errors become smaller |
| **Inference** | Checking a new weld seam in seconds |

</section>

## Game: Fill the Vocabulary Gaps 🧩

A vocational school collects 10,000 photos of weld seams. Each photo gets a [->[feature|(label)|weight]] "OK" or "defect". Seam width and porosity are [->[(features)|labels|epochs]]. A [->[model|(algorithm)|dataset]] such as gradient descent adjusts the [->[labels|(weights)|photos]] during [->[inference|(training)|deployment]]. The result is a trained [->[(model)|feature|label]], which checks new seams in seconds – this is called [->[training|(inference)|labelling]].

                --{{0}}--
Drag the words into the gaps. If you can explain this paragraph to a colleague, you have the core vocabulary of machine learning.

## 2. Weights – How Knowledge Is Stored

A model "knows" nothing in the human sense. It stores **weights**: numbers that decide how strongly an input influences the output.

``` ascii
 practice hours ──(w1 = 0.6)──┐
 theory score   ──(w2 = 0.3)──┼──►  Σ  ──► activation ──► "pass" probability
 attendance     ──(w3 = 0.1)──┘
```

{{1}}
<section>

During training, the algorithm changes `w1`, `w2`, `w3` until predictions match reality as well as possible. **On the next slide, you are the algorithm.**

</section>

## Playground: Be the Training Algorithm 🎚️

**One apprentice:**

| Input | Value (0–100) | Weight |
| --- | --- | --- |
| Practice hours | <script input="range" min="0" max="100" step="5" value="70" output="x1">@input</script> | w1 = <script input="range" min="-1" max="1" step="0.1" value="0.6" output="w1">@input</script> |
| Theory score | <script input="range" min="0" max="100" step="5" value="60" output="x2">@input</script> | w2 = <script input="range" min="-1" max="1" step="0.1" value="0.3" output="w2">@input</script> |
| Attendance | <script input="range" min="0" max="100" step="5" value="90" output="x3">@input</script> | w3 = <script input="range" min="-1" max="1" step="0.1" value="0.1" output="w3">@input</script> |

<script modify="false" style="display:block">
const x = [@input(`x1`), @input(`x2`), @input(`x3`)].map(v => Number(v) / 100);
const w = [@input(`w1`), @input(`w2`), @input(`w3`)].map(Number);
const sum = x[0]*w[0] + x[1]*w[1] + x[2]*w[2];
const z = 10 * sum - 5;
const p = 1 / (1 + Math.exp(-z));
const col = p > 0.66 ? "#16a34a" : (p > 0.33 ? "#f59e0b" : "#dc2626");
`HTML: <p>Σ = ${w.map((wi,i) => wi.toFixed(1) + "·" + x[i].toFixed(2)).join(" + ")} = <b>${sum.toFixed(2)}</b> → activation (sigmoid) →</p>
<div style="background:#e5e7eb;border-radius:6px;height:26px;width:100%"><div style="background:${col};height:26px;width:${(p*100).toFixed(0)}%;border-radius:6px;color:white;font-weight:bold;padding-left:8px;line-height:26px">${(p*100).toFixed(0)} %</div></div>
<p>Predicted probability to <b>pass</b> the practical exam.</p>`
</script>

<small>Toy model for illustration (activation = sigmoid of 10·Σ − 5). Real models have thousands to billions of weights.</small>

                --{{0}}--
First change the apprentice. Then change the weights. What happens if attendance gets a negative weight? Or if theory gets all the weight? This is what training does automatically, millions of times, to reduce the error.

## How Are Good Weights Found?

{{1}}
<section>

- **Backpropagation** – the standard (station 5)
- **Evolution-inspired:** *EvoLearn* combines a genetic algorithm with backpropagation; models reached their best error level earlier (Bedi et al., 2024)
- **Tiny weights for tiny devices:** *binary neural networks* store each weight in a single bit → smaller, faster, more energy-efficient for **edge devices** in the workshop – but harder to train, less accurate (Crulis et al., 2024)

</section>

{{2}}
<section>

**Why weights matter for society:** open-weight models can be run, studied and fine-tuned by anyone – good for research and independence, but safety measures can also be removed (NTIA, 2024) · fine-tuning adapts weights (e.g. to a trade's terminology) · **data poisoning** manipulates them.

</section>

## 3. Data – Garbage In, Garbage Out 🗑️

| Criterion | Question | Risk if missing |
| --- | --- | --- |
| **Size** | Enough examples? | Doesn't generalise |
| **Correctness** | Labels right? | Learns errors |
| **Representativeness** | All groups and situations? | Bias |
| **Timeliness** | Current? | Outdated patterns |
| **Legality** | GDPR, copyright? | Legal & ethical problems |

{{1}}
<section>

- Networks can easily tell **which** large image dataset a picture comes from → "big" ≠ "representative" (Zeng et al., 2024)
- Checking whether a group is covered: pre-trained classifiers alone are **not reliable** – combine algorithms with human crowd workers (Mousavi et al., 2024)
- A representative reference dataset can help select a better-matching subsample (Hauptmann et al., 2023)

</section>

## Game: Spot the Data Problem 🔍

Which quality criterion is violated?

- [[Size] [Correctness] [Representativeness] [Timeliness] [Legality]]
- [ ( )       ( )             (X)             ( )         ( )  ]  Tutoring system trained only with data from urban vocational schools
- [ ( )       ( )             ( )             (X)         ( )  ]  Chatbot for electricians trained on standards that were replaced last year
- [ ( )       (X)             ( )             ( )         ( )  ]  Half of the "defect" weld photos were labelled "OK" by mistake
- [ ( )       ( )             ( )             ( )         (X)  ]  Apprentices' chat messages collected without consent
- [ (X)       ( )             ( )             ( )         ( )  ]  Only 12 example photos for a new welding technique

## 4. Learning Paradigms 🎓

| | Supervised | Unsupervised | Reinforcement |
| --- | --- | --- | --- |
| Data | Labelled | Unlabelled | Interaction + reward |
| Goal | Predict | Discover structure | Learn a strategy |
| TVET example | Weld seam inspection | Grouping learners | Robot path optimisation |

{{1}}
<section>

**Critical reading:** one study reports ~92 % accuracy for supervised vs. 66–85 % for unsupervised models – but unsupervised methods were stronger at finding anomalies in *unlabelled* data (Verma et al., 2025). *Are accuracies of tasks with and without labels really comparable?*

</section>

## Game: Which Paradigm? 🤖

- [[Supervised] [Unsupervised] [Reinforcement]]
- [    ( )           (X)             ( )     ]  Find groups of learners with similar error patterns – no categories given
- [    (X)           ( )             ( )     ]  Predict the remaining lifetime of a tool from labelled sensor data
- [    ( )           ( )             (X)     ]  A robot learns to grip parts through rewards
- [    ( )           (X)             ( )     ]  Detect unusual vibration patterns in a machine
- [    (X)           ( )             ( )     ]  Classify e-mails as "spam / no spam"
- [    ( )           ( )             (X)     ]  Fine-tuning an LLM with human feedback

## 5. Neural Networks 🧠

``` ascii
 Input layer      Hidden layers        Output layer
   (x1) ───┐     (h)───(h)───┐
   (x2) ───┼───► (h)───(h)───┼───►  (y)  "defect: 0.93"
   (x3) ───┘     (h)───(h)───┘
```

{{1}}
<section>

1. **Layers** – input, hidden, output
2. **Activation functions** (ReLU, sigmoid) – make the network non-linear
3. **Loss** – measures the error
4. **Backpropagation** – sends the error backwards; each weight moves a little downhill (**gradient descent**)
5. **Epochs** – repeat over the whole dataset

</section>

{{2}}
<section>

Mixing activation functions per layer can improve generalisation but costs time and risks **overfitting** (Sohal & Stonehill, 2023). Why training works at all: layers are strongly correlated, so the search space is far smaller than the number of weights suggests (Hodas & Stinis, 2018).

</section>

## Lab: Gradient Descent by Hand ⛰️

The model `y = w · x` should learn from data where the true rule is `y = 2 · x`. Start: **w = 0**.

Learning rate: <script input="range" min="0.005" max="0.12" step="0.005" value="0.02" output="lr">@input</script>

Epochs: <script input="range" min="1" max="40" step="1" value="10" output="ep">@input</script>

<script modify="false" style="display:block">
const lr = Number(@input(`lr`)), ep = Number(@input(`ep`));
const xs = [1,2,3,4,5], mx2 = xs.reduce((a,x) => a + x*x, 0) / xs.length;
let w = 0; const ws = [w], losses = [(w-2)*(w-2)*mx2];
for (let i = 0; i < ep; i++) { w = w - lr * 2 * (w - 2) * mx2; ws.push(w); losses.push((w-2)*(w-2)*mx2); }
const maxL = losses[0];
const W = 300, H = 140;
const pts = losses.map((l,i) => `${20 + i*(W-30)/Math.max(1,ep)},${H - 10 - Math.min(l,maxL*1.2)/(maxL*1.2)*(H-20)}`).join(" ");
const diverge = Math.abs(w - 2) > 2;
const status = diverge ? "💥 <b>Diverging!</b> The steps are so big that w jumps over the valley and further away each epoch." : (Math.abs(w-2) < 0.05 ? "✅ <b>Converged.</b> The model found the rule." : "🐢 <b>Still learning</b> – more epochs or a larger learning rate.");
`HTML: <svg viewBox="0 0 ${W} ${H}" style="width:100%;max-width:520px"><line x1="20" y1="${H-10}" x2="${W}" y2="${H-10}" stroke="currentColor"/><line x1="20" y1="5" x2="20" y2="${H-10}" stroke="currentColor"/><text x="24" y="14" font-size="10" fill="currentColor">loss</text><text x="${W-40}" y="${H-14}" font-size="10" fill="currentColor">epochs</text><polyline points="${pts}" fill="none" stroke="#dc2626" stroke-width="2"/></svg>
<p>After ${ep} epochs: <b>w = ${isFinite(w) ? w.toFixed(3) : "∞"}</b> (target 2) · loss = ${isFinite(losses[ep]) ? losses[ep].toFixed(3) : "∞"}</p><p>${status}</p>`
</script>

                --{{0}}--
Try a tiny learning rate: the model learns, but slowly. Try a large one, above about zero point zero nine: the loss explodes. Choosing such settings is part of the craft of machine learning.

## Play: TensorFlow Playground 🎮

Train a real neural network in your browser. **Mission:** solve the **spiral** dataset (bottom-right). Add layers and neurons – what changes?

??[TensorFlow Playground](https://playground.tensorflow.org)

Fewest neurons you needed for the spiral?

- [(2)] ≤ 4
- [(6)] 5–8
- [(10)] 9–12
- [(14)] more than 12 / never solved it 😅

                --{{0}}--
Note your observation in your AI tools log. Hint: try adding the sine features on the left, or use more hidden layers.

## More Explainers 🔭

??[MLU-Explain: Neural Networks (Amazon)](https://mlu-explain.github.io/neural-networks/)

{{1}}
<section>

Also great: [CNN Explainer](https://poloclub.github.io/cnn-explainer/) (how images are classified layer by layer) · [Quick, Draw!](https://quickdraw.withgoogle.com) (a network guesses your doodle) · full list: [Interactive websites for learning about AI](https://github.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/blob/main/interactive-ai-learning-websites.md)

</section>

## 6. Hands-on: Train Your First Model 📸

**Tool:** [▶ Teachable Machine](https://teachablemachine.withgoogle.com) (no code, opens in a new tab)

{{1}}
<section>

1. **Image project**, two classes: "safety glasses on" / "off" (objects instead of faces are fine)
2. ~30 images per class with your webcam
3. **Train model**
4. Test with new images – when does it fail?
5. Make it **unbalanced**: 60 images vs. 10. What happens?

</section>

{{2}}
<section>

**What happened with unbalanced data?**

- [(bias)] The model mostly predicted the bigger class
- [(same)] Nothing changed
- [(worse)] It became uncertain for both classes
- [(other)] Something else (→ log)

📸 Screenshots + 5–8 sentences of reflection → **hand-in item 2**

</section>

## 7. AI Workflows in Education 🔄

``` ascii
 1 Define goal ─► 2 Collect / select data ─► 3 Choose model or tool ─►
 4 Generate / predict ─► 5 Human review ─► 6 Use in teaching ─► 7 Evaluate & improve
                              ▲                                        │
                              └──────────── feedback loop ◄────────────┘
```

{{1}}
<section>

| Step | Ethical checkpoint |
| --- | --- |
| Data | Personal data? Consent? Representative? |
| Model/tool | Licence, storage location, transparency |
| Output | Correct? Biased? Suitable? |
| Use | Who decides? Can learners contest? |
| Evaluation | Did learning improve? Side effects? |

</section>

## Where Does Bias Enter? 🕳️

Hanna et al. (2025): **data bias** · **development bias** · **interaction bias** (e.g. automation bias)

- [[Data bias] [Development bias] [Interaction bias]]
- [    (X)            ( )                 ( )      ]  Historical data from male-dominated trades
- [    ( )            (X)                 ( )      ]  Model developed only with data from large companies
- [    ( )            ( )                 (X)      ]  Teachers accept AI grading suggestions without checking
- [    ( )            (X)                 ( )      ]  Validation only with urban schools

{{1}}
<section>

**Why step 5 matters:** experts rated ChatGPT diet plans about as good as standard materials and rarely identified the AI plan – yet found conflicting, unaffordable or unspecific advice (Kim et al., 2024). AI teaching material can **look** professional and still be wrong.

</section>

## 8. Algorithm, Model or Agent? 🦾

| | Simple algorithm | AI model | AI agent |
| --- | --- | --- | --- |
| Behaviour | Fixed steps by humans | Learned from data | Pursues a goal, plans, uses tools |
| Adapts? | No | Through training | Feedback during the task |
| Example | Grade formula | Weld-seam classifier | Searches sources, drafts lesson plan, creates quiz file |

{{1}}
<section>

``` ascii
        ┌──────── PLAN ────────┐
        │                      ▼
     ADJUST                   ACT  ──► tools: web search, code, files
        ▲                      │
        └────── OBSERVE ◄──────┘        + memory
```

The more autonomy, the more **human oversight** is needed.

</section>

**Check:** What distinguishes an AI agent from a single chatbot answer?

- [( )] It always runs offline.
- [(X)] It can plan several steps and use tools to reach a goal.
- [( )] It does not use a language model.

## 9. Reading: UNESCO AI CFT for Students 📖

Four dimensions × three levels **Understand – Apply – Create** (UNESCO, 2024a)

| | Understand | Apply | Create |
| --- | --- | --- | --- |
| Human-centred mindset | ● | ● | ● |
| Ethics of AI | ● | ● | ● |
| **AI techniques and applications** ← read these blocks | ● | ● | ● |
| AI system design | ● | ● | ● |

{{1}}
<section>

**Guiding questions** (→ hand-in item 3)

1. Which *Understand* competencies does **every** TVET learner need?
2. Which *Create* competencies fit **your** vocational field?
3. Which competency could become the **core of your micro-credential**? 💡

**My first micro-credential idea in one line:**

[[___]]

</section>

## Hand-in for Session 3 📤

**Deadline: 04.11.2026, 23:59 · Moodle · one PDF**

1. **Glossary:** the 8 terms in your own words + example from **your** field
2. **Hands-on:** Teachable Machine screenshots + 5–8 sentences (incl. unbalanced data)
3. **Reading:** answers to the three guiding questions (max. 1 page) – Q3 = your idea, checked live on **05.11.2026**
4. **AI tools log:** updated

{{1}}
<section>

**Which lab station was the most fun?**

- [(weights)] Weights playground
- [(gd)] Gradient descent lab
- [(tfp)] TensorFlow Playground
- [(tm)] Teachable Machine

</section>

## References

- Bedi, J., Anand, A., Godara, S., Bana, R. S., Faiz, M. A., Marwaha, S., & Parsad, R. (2024). Effective weight optimization strategy for precise deep learning forecasting models using EvoLearn approach. *Scientific Reports, 14*, 20139. https://doi.org/10.1038/s41598-024-69325-3
- Crulis, B., Serres, B., de Runz, C., & Venturini, G. (2024). *An experimental comparative study of backpropagation and alternatives for training binary neural networks for image classification* (arXiv:2408.04460). https://arxiv.org/abs/2408.04460
- Hanna, M. G., Pantanowitz, L., Jackson, B., et al. (2025). Ethical and bias considerations in artificial intelligence/machine learning. *Modern Pathology, 38*(3), 100686. https://doi.org/10.1016/j.modpat.2024.100686
- Hauptmann, T., Fellenz, S., Nathan, L., Tüscher, O., & Kramer, S. (2023). Discriminative machine learning for maximal representative subsampling. *Scientific Reports, 13*, 20925. https://doi.org/10.1038/s41598-023-48177-3
- Hodas, N. O., & Stinis, P. (2018). Doing the impossible: Why neural networks can be trained at all. *Frontiers in Psychology, 9*, 1185. https://doi.org/10.3389/fpsyg.2018.01185
- Kim, D. W., Park, J. S., Sharma, K., et al. (2024). Qualitative evaluation of artificial intelligence-generated weight management diet plans. *Frontiers in Nutrition, 11*, 1374834. https://doi.org/10.3389/fnut.2024.1374834
- Mousavi, M., Shahbazi, N., & Asudeh, A. (2024). Data coverage for detecting representation bias in image datasets: A crowdsourcing approach. In *Proceedings of EDBT 2024*.
- National Telecommunications and Information Administration. (2024). *Dual-use foundation models with widely available model weights*. https://www.ntia.gov/programs-and-initiatives/artificial-intelligence/open-model-weights-report/background
- Sohal, J., & Stonehill, B. (2023). *Analysis of multi-activation layers in neural network architectures* [Conference presentation]. Kennesaw State University.
- UNESCO. (2024a). *AI competency framework for students*. https://doi.org/10.54675/JKJB9835
- Verma, R., Maheshwari, R., Manore, D., Rane, P. S., & Raikwar, M. (2025). Supervised vs. unsupervised learning: A comparative study in modern AI system. *Communications on Applied Nonlinear Analysis, 32*(9s), 860–872.
- Zeng, B., Yin, Y., & Liu, Z. (2024). Understanding bias in large-scale visual datasets. In *NeurIPS 2024*. https://arxiv.org/abs/2412.01876

**Interactive tools:** [TensorFlow Playground](https://playground.tensorflow.org) · [Teachable Machine](https://teachablemachine.withgoogle.com) · [MLU-Explain](https://mlu-explain.github.io) · [CNN Explainer](https://poloclub.github.io/cnn-explainer/) · [Quick, Draw!](https://quickdraw.withgoogle.com)

<small>Licence: CC BY 4.0 · Dr. Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), based on the self-learning unit S03; checked by the author.</small>
