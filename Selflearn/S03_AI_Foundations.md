<!--
author:    Dr. Hannes Tegelbeckers
email:     hannes.tegelbeckers@ovgu.de
version:   1.2.0
language:  en
narrator:  UK English Female
mode:      Textbook

title:     S03 – AI foundations: vocabulary, models, algorithms and workflows (Self-learning unit)
comment:   AI in TVET I – Self-learning unit for session 3 (29.10.2026): data, weights, models, algorithms, learning paradigms, neural networks, AI workflows and agents; reading of the UNESCO AI Competency Framework for Students.
-->

# S03 – AI Foundations: Vocabulary, Models, Algorithms and Workflows

> **Session 3 · 29.10.2026 · 🔵 Self-learning** – I am travelling; work through this unit on your own.
>
> **Time needed:** about 3 hours (incl. reading and hands-on)
>
> **Do the exercise in Moodle by 04.11.2026, 23:59** – see the last chapter: [Open the course in Moodle](https://elearning.ovgu.de/course/view.php?id=21948)

**After this unit you will be able to …**

1. use the core vocabulary correctly: data, features, labels, algorithm, model, weights, training, inference,
2. distinguish supervised, unsupervised and reinforcement learning with TVET examples,
3. explain how a neural network learns (layers, activation, backpropagation),
4. describe an AI workflow from input data to output, including ethical checkpoints,
5. explain the difference between a simple algorithm, an AI model and an AI agent.

## 1. The Vocabulary Map

``` ascii
  DATA ──────────► ALGORITHM ──────────► MODEL ──────────► OUTPUT
 (examples,        (learning procedure,  (learned weights,  (prediction,
  features,         e.g. gradient         structure)         classification,
  labels)           descent)                                 generated text)
      │                                      ▲
      └──────────── TRAINING ────────────────┘        INFERENCE = using the model
```

| Term | Meaning | TVET example |
| --- | --- | --- |
| **Data** | Examples the system learns from | 10,000 photos of weld seams |
| **Feature** | A measurable property in the data | Seam width, porosity, colour |
| **Label** | The "correct answer" for an example | "OK" / "defect" |
| **Algorithm** | Step-by-step procedure that learns from data | Decision tree learning, gradient descent |
| **Model** | The result of training: structure + learned parameters | Trained weld-inspection classifier |
| **Weights** | Numbers inside the model that encode what it has learned | Millions of values in a neural network |
| **Training** | Adjusting the weights so that errors become smaller | Several hours on a GPU |
| **Inference** | Applying the trained model to new data | Checking a new weld seam in seconds |

**Matching exercise:** Which term fits? "The trained classifier, which can now be used on new photos."

- [( )] Algorithm
- [(X)] Model
- [( )] Label
- [( )] Feature

## 2. Weights – How Knowledge Is Stored

A model "knows" nothing in the human sense. What it has learned is stored in **weights**: numbers that determine how strongly an input influences the output.

**Simple example:** predicting whether an apprentice passes a practical exam.

``` ascii
 practice hours ──(w1 = 0.6)──┐
 theory score   ──(w2 = 0.3)──┼──►  Σ  ──► activation ──► "pass" probability
 attendance     ──(w3 = 0.1)──┘
```

**Worked example:** All inputs are scaled to values between 0 and 1. Apprentice A has practice hours = 0.8, theory score = 0.5, attendance = 1.0.

```text
weighted sum = 0.6 · 0.8 + 0.3 · 0.5 + 0.1 · 1.0
             = 0.48 + 0.15 + 0.10
             = 0.73
```

The activation function turns this sum into a probability. The weights show what the model has "learned": in this (invented) example practice hours count six times as much as attendance.

During training, the algorithm changes `w1`, `w2`, `w3` until the predictions match the real results as well as possible. If apprentices with many practice hours fail the exam more often than predicted, training lowers `w1` a little – and repeats this for thousands of examples.

**Your turn:** Apprentice B has practice hours = 0.5, theory score = 1.0, attendance = 0.5. Calculate the weighted sum.

[[0.65]]
[[?]] 0.6 · 0.5 + 0.3 · 1.0 + 0.1 · 0.5
***
0.30 + 0.30 + 0.05 = 0.65. Although B has the best theory score, the sum is lower than A's – because the model weights practice hours most.
***

**How are good weights found?** Usually with *backpropagation* (section 5) – but not only:

- **Evolution-inspired training:** *EvoLearn* combines a genetic algorithm with backpropagation. In each cycle, the best weights of several candidate models are combined (selection, crossover, mutation). For forecasting air pollution and energy consumption, the models reached their best error level earlier than with backpropagation alone (Bedi et al., 2024).
- **Smaller weights for small devices:** *Binary neural networks* store each weight in a single bit instead of a floating-point number. Models become much smaller, faster and more energy-efficient – interesting for machines and sensors in the workshop (*edge devices*). The price: they are harder to train and lose accuracy (Crulis et al., 2024).

**Why weights matter for society**

- Large language models have billions of weights. When companies publish them (**open-weight models**), anyone can run, study or fine-tune the model – good for research and independence, but the safety measures can also be removed (NTIA, 2024).
- Fine-tuning changes weights for a new purpose – e.g. a model adapted to the terminology of a trade.
- Manipulating training data (data poisoning) changes the weights and thus the behaviour of a model.

**Check:** A company adapts an open-weight LLM to the vocabulary of the electrical trades with its own training documents. What changes?

- [( )] Only the prompt – the model stays the same.
- [(X)] The weights of the model (fine-tuning).
- [( )] The training data of the original provider.

## 3. Data – Size, Quality, Representativeness

> "Garbage in, garbage out": a model can only be as good as its data.

| Quality criterion | Question | Risk if missing |
| --- | --- | --- |
| **Size** | Are there enough examples? | Model does not generalise |
| **Correctness** | Are labels right? | Model learns errors |
| **Representativeness** | Does the data reflect all relevant groups and situations? | Bias against under-represented groups |
| **Timeliness** | Is the data current? | Outdated patterns (e.g. old standards) |
| **Legality** | Was the data collected lawfully (GDPR, copyright)? | Legal and ethical problems |

**What research shows about data bias**

- **Even huge datasets are biased:** Neural networks can tell easily which large image dataset a picture comes from. The differences lie in objects, structure, colour and other visual features (Zeng et al., 2024). "Big" does not mean "representative".
- **Checking coverage:** Whether a dataset covers a group (e.g. women in a trade) can be checked systematically; pre-trained classifiers alone are *not reliable* for this – the authors combine algorithms with human crowd workers (Mousavi et al., 2024).
- **Correcting biased samples:** If a survey reached only some groups, machine learning can use a representative reference dataset to select a subsample that matches the population better (Hauptmann et al., 2023).

**Check:** A tutoring system is trained only with data from urban vocational schools. What is the main problem?

- [( )] The dataset is too large.
- [(X)] The dataset is not representative for rural learners.
- [( )] The labels are missing.

## 4. Learning Paradigms

Machine learning is not one method but a family of approaches. They differ in **what kind of data** is available and **what the system should learn**. The three main paradigms are explained on the next pages – each with an example from the workshop. The key question for choosing one is always: *Do I have examples with the correct answer (labels) – or not?*

### Supervised learning – learning with a "teacher"

The data contains labels. The model learns the relation between input and correct output – like an apprentice who practises with tasks *and* the model solutions.

- **Classification:** "defect / no defect", "spam / no spam"
- **Regression:** predicting a number, e.g. remaining lifetime of a tool

**Example:** A camera system for weld seams is trained with 10,000 photos that experienced welders have labelled "OK" or "defect". After training it classifies new seams. Its quality depends on the labels: if the experts disagreed or made mistakes, the model learns these mistakes too. Labelling is therefore expensive expert work – often the largest cost of a supervised project.

### Unsupervised learning – discovering structure

No labels. The model finds groups or patterns itself – nobody tells it what the "right" groups are.

- **Clustering:** grouping learners by learning behaviour
- **Anomaly detection:** unusual vibration patterns in a machine

**Example:** A CNC machine records vibration data every second. Nobody has labelled which values are "normal". An unsupervised model learns what typical patterns look like and reports values that do not fit – a possible sign of tool wear. Humans must then *interpret* the result: a cluster or an anomaly has no meaning until an expert explains it.

### Reinforcement learning – learning by reward

An agent acts in an environment and receives rewards or penalties – e.g. a robot learning to grip parts; also used to fine-tune LLMs with human feedback.

| | Supervised | Unsupervised | Reinforcement |
| --- | --- | --- | --- |
| Data | Labelled | Unlabelled | Interaction + reward |
| Goal | Predict | Discover structure | Learn a strategy |
| TVET example | Weld seam inspection | Grouping learners for differentiation | Robot path optimisation |

**What does research say?** One comparative study on finance, health and image data reports about 92% accuracy for supervised models (decision tree, SVM) and 66–85% for unsupervised ones (k-means, autoencoder) – but unsupervised methods were stronger at finding anomalies and patterns in *unlabelled* data (Verma et al., 2025). **Critical reading:** Are accuracy values of tasks with and without labels really comparable? The choice of paradigm depends on the task and on whether labels exist.

A beginner-friendly overview of common ML and deep-learning models (decision trees, random forests, neural networks …) and how one research field uses them is given in a scoping review on obesity research (An et al., 2022) – a good model for asking "which methods are used in *my* vocational field?".

**Check:** A vocational school wants to find groups of learners with similar error patterns in an online course – without predefined categories. Which paradigm?

- [( )] Supervised learning
- [(X)] Unsupervised learning
- [( )] Reinforcement learning

## 5. Neural Networks

Neural networks are loosely inspired by the brain. They consist of **layers** of connected "neurons".

``` ascii
 Input layer      Hidden layers        Output layer
   (x1) ───┐     (h)───(h)───┐
   (x2) ───┼───► (h)───(h)───┼───►  (y)  "defect: 0.93"
   (x3) ───┘     (h)───(h)───┘
```

1. **Layers:** The input layer takes the data, hidden layers transform it, the output layer delivers the result.
2. **Activation functions** (e.g. ReLU, sigmoid) make the network *non-linear*, so it can learn complex patterns.
3. **Loss:** After a prediction, the error is measured.
4. **Backpropagation:** The error is sent backwards through the network; each weight is adjusted a little in the direction that reduces the error (**gradient descent**).
5. **Epochs:** This is repeated many times over the whole dataset.

**Design choices matter.** Most networks use the *same* activation function in every layer. Mixing different activation functions per layer can improve generalisation, but costs training time and increases the risk of *overfitting* (Sohal & Stonehill, 2023).

Why training works at all with millions or billions of weights was long a theoretical puzzle. One explanation: the layers of a network are strongly correlated, so the space the training has to search is far smaller than the number of weights suggests (Hodas & Stinis, 2018).

**Overfitting in plain words:** A network with many weights can "memorise" the training data – like an apprentice who learns the answers of last year's exam by heart. It is perfect on the known data and fails on new tasks. That is why data is split into a **training set** and a **test set**, and the model is judged only on the test set.

**Check:** What happens during backpropagation?

- [( )] New training data is collected automatically.
- [(X)] The error is passed backwards and each weight is adjusted slightly to reduce it.
- [( )] The network removes layers that are not needed.

**Check:** A model reaches 99 % accuracy on the training data but only 60 % on new data. What is the most likely problem?

- [( )] Underfitting
- [(X)] Overfitting
- [( )] Too few weights

**Try it yourself (15 min):** Open the [TensorFlow Playground](https://playground.tensorflow.org). Train a network on the "spiral" dataset. Add hidden layers and neurons. What changes? Note your observation in your log.

**More interactive explainers:** see the list [Interactive websites for learning about AI](https://github.com/OVGU-VET-TechEd/AI_in_TVET_I_WiSe_2026_2027/blob/main/interactive-ai-learning-websites.md) (e.g. Transformer Explainer, CNN Explainer).

## 6. Train Your First Model (Hands-on)

**Tool:** [Teachable Machine](https://teachablemachine.withgoogle.com) (no code, runs in the browser)

1. Create an **image project** with two classes, e.g. "safety glasses on" / "safety glasses off" (use objects instead of faces if you prefer).
2. Record about 30 images per class with your webcam.
3. Click **Train model**.
4. Test with new images. When does it fail?
5. Add **unbalanced** data: 60 images for one class, 10 for the other. What happens?

**Reflection for your log:** What does this experiment tell you about data quality and bias?

<details>
<summary>What you will probably observe</summary>

- With balanced, varied images the model usually works well – as long as the test images look like the training images (same light, background, distance).
- With new lighting or a different background, it often fails: the model may have learned the *background* instead of the safety glasses.
- With unbalanced data (60 : 10), the model tends to predict the larger class more often, even when it is wrong.
- Transfer: The same happens with real systems. If one group (e.g. women in a trade, learners from rural schools) is under-represented in the data, the model works worse for them – this is how *data bias* arises (section 3).

</details>

## 7. AI Workflows in Education

An AI workflow describes the steps from input to usable output – including the human checks.

``` ascii
 1 Define goal ─► 2 Collect / select data ─► 3 Choose model or tool ─►
 4 Generate / predict ─► 5 Human review ─► 6 Use in teaching ─► 7 Evaluate & improve
                              ▲                                        │
                              └──────────── feedback loop ◄────────────┘
```

**Ethical checkpoints in the workflow**

| Step | Checkpoint |
| --- | --- |
| Data | Personal data? Consent? Representative? |
| Model/tool | Licence, data storage location, transparency |
| Output | Correct? Biased? Suitable for the learners? |
| Use | Who decides? Can learners contest results? |
| Evaluation | Did learning improve? Unintended effects? |

**Where does bias enter the workflow?** Medicine, where AI supports high-stakes decisions, distinguishes three sources (Hanna et al., 2025):

| Source | Examples | TVET parallel |
| --- | --- | --- |
| **Data bias** | Historical inequalities in the data, under-representation, missing or fragmented records | Historical data from male-dominated trades |
| **Development bias** | Choices in data selection, validation and model development – e.g. training only with cases from large academic hospitals | Model developed only with data from large companies or urban schools |
| **Interaction bias** | How people use the system – e.g. **automation bias**: users over-trust AI advice and accept wrong suggestions | Teachers accept AI grading suggestions without checking |

Further types listed include *temporal bias* (criteria change over time) and *feedback-loop bias* (earlier decisions shape future data).

**Why step 5 (human review) is essential:** Experts in obesity medicine rated ChatGPT diet plans about as good as standard patient materials and could rarely identify the AI plan (only 5 of 14 who believed they could). Yet they found conflicting recommendations, unaffordable suggestions and missing specifics such as portion sizes (Kim et al., 2024). The same applies to AI-generated teaching material: it can *look* professional and still be wrong or unsuitable.

**Example (TVET):** Generating a quiz for apprentices: goal (learning outcome) → own course text as data → LLM with template prompt → 10 questions → teacher checks correctness and difficulty → quiz in LiaScript → item analysis after the lesson → revise.

**Check:** A teacher accepts all grading suggestions of an AI tool without checking them, because "the AI is usually right". Which source of bias is this?

- [( )] Data bias
- [( )] Development bias
- [(X)] Interaction bias (automation bias)

## 8. Algorithms, Models and Agents

| | Simple algorithm | AI model | AI agent |
| --- | --- | --- | --- |
| Behaviour | Fixed steps written by humans | Learned from data | Pursues a goal, plans steps, uses tools |
| Adapts? | No | Through training | Uses feedback during the task |
| Example | Grade calculation formula | Classifier for weld seams | Assistant that searches sources, drafts a lesson plan and creates a quiz file |

An **AI agent** typically combines an LLM ("reasoning") with **tools** (web search, code, files), **memory** and a loop of *plan → act → observe → adjust*. The more autonomy an agent has, the more important human oversight becomes.

**Check:** What distinguishes an AI agent from a single chatbot answer?

- [( )] It always runs offline.
- [(X)] It can plan several steps and use tools to reach a goal.
- [( )] It does not use a language model.

## 9. Reading: UNESCO AI Competency Framework for Students

The framework (UNESCO, 2024a) describes what learners need to know and be able to do to use AI safely, critically and creatively. It has **four dimensions** and **three progression levels** – together 12 competencies:

| Dimension | Understand | Apply | Create |
| --- | --- | --- | --- |
| Human-centred mindset | Human agency | Human accountability | Citizenship in the era of AI |
| Ethics of AI | Embodied ethics | Safe and responsible use | Ethics by design |
| **AI techniques and applications** | AI foundations | Application skills | Creating AI tools |
| AI system design | Problem scoping | Architecture design | Iteration and feedback loops |

The levels build on each other: *Understand* means knowing basic concepts and risks; *Apply* means using AI tools purposefully for tasks; *Create* means adapting or building AI solutions. This unit (vocabulary, paradigms, neural networks, workflows) corresponds to **AI foundations** – the *Understand* level of "AI techniques and applications". The Teachable Machine experiment is a first step towards *Create*.

**For TVET** the framework is a starting point, not a curriculum: an apprentice in automotive mechatronics needs other "application skills" than a nursing trainee. Your micro-credential translates one competency into a concrete vocational context.

Read in the framework (UNESCO, 2024a):

- the overview of the four dimensions and three progression levels,
- the competency blocks for **"AI techniques and applications"**.

**Check:** An apprentice uses an AI tool to create a maintenance checklist and checks it against the manufacturer's manual. Which level of "AI techniques and applications" is this mainly?

- [( )] Understand
- [(X)] Apply
- [( )] Create

**Guiding questions**

1. Which competencies at level *Understand* would every TVET learner need?
2. Which competencies at level *Create* fit a specific vocational field?
3. Which competency could become the core of your micro-credential?

## 10. Exercise in Moodle for Session 3

**Do the exercise in Moodle by 04.11.2026, 23:59:** [Open the course in Moodle](https://elearning.ovgu.de/course/view.php?id=21948)

Enter your results in the fields below and submit each field. Moodle saves your progress. The exercise counts as done when you have completed this unit in Moodle by the deadline – no file upload is needed.

**1 · Glossary** – the 8 terms from section 1 (data, feature, label, algorithm, model, weights, training, inference) in your own words, each with an example from **your** vocational field:

[[___ ___ ___ ___ ___ ___ ___ ___]]

**2 · Hands-on** (section 6) – 5–8 sentences on your Teachable Machine experiment: classes, number of images, what worked, when the model failed, and what happened with the unbalanced data:

[[___ ___ ___ ___ ___]]

**3 · Reading** (section 9) – your answers to the three guiding questions. Question 3 is your first micro-credential idea, which we check together on 05.11.2026:

[[___ ___ ___ ___ ___ ___]]

**4 · AI tools log** – at least **3 entries** from this unit (tool, purpose, prompt, what you checked or changed):

[[___ ___ ___ ___ ___]]

Open questions are discussed at the start of the live session on 05.11.2026.

## References

- An, R., Shen, J., & Xiao, Y. (2022). Applications of artificial intelligence to obesity research: Scoping review of methodologies. *Journal of Medical Internet Research, 24*(12), e40589. https://doi.org/10.2196/40589
- Bedi, J., Anand, A., Godara, S., Bana, R. S., Faiz, M. A., Marwaha, S., & Parsad, R. (2024). Effective weight optimization strategy for precise deep learning forecasting models using EvoLearn approach. *Scientific Reports, 14*, 20139. https://doi.org/10.1038/s41598-024-69325-3
- Crulis, B., Serres, B., de Runz, C., & Venturini, G. (2024). *An experimental comparative study of backpropagation and alternatives for training binary neural networks for image classification* (arXiv:2408.04460). https://arxiv.org/abs/2408.04460
- Hanna, M. G., Pantanowitz, L., Jackson, B., Palmer, O., Visweswaran, S., Pantanowitz, J., Deebajah, M., & Rashidi, H. H. (2025). Ethical and bias considerations in artificial intelligence/machine learning. *Modern Pathology, 38*(3), 100686. https://doi.org/10.1016/j.modpat.2024.100686
- Hauptmann, T., Fellenz, S., Nathan, L., Tüscher, O., & Kramer, S. (2023). Discriminative machine learning for maximal representative subsampling. *Scientific Reports, 13*, 20925. https://doi.org/10.1038/s41598-023-48177-3
- Hodas, N. O., & Stinis, P. (2018). Doing the impossible: Why neural networks can be trained at all. *Frontiers in Psychology, 9*, 1185. https://doi.org/10.3389/fpsyg.2018.01185
- Kim, D. W., Park, J. S., Sharma, K., Velazquez, A., Li, L., Ostrominski, J. W., Tran, T., Seitter Peréz, R. H., & Shin, J.-H. (2024). Qualitative evaluation of artificial intelligence-generated weight management diet plans. *Frontiers in Nutrition, 11*, 1374834. https://doi.org/10.3389/fnut.2024.1374834
- Mousavi, M., Shahbazi, N., & Asudeh, A. (2024). Data coverage for detecting representation bias in image datasets: A crowdsourcing approach. In *Proceedings of EDBT 2024*. https://openproceedings.org/2024/conf/edbt/Data_Coverage_EDBT_CRV.pdf
- National Telecommunications and Information Administration. (2024). *Dual-use foundation models with widely available model weights*. https://www.ntia.gov/programs-and-initiatives/artificial-intelligence/open-model-weights-report/background
- Sohal, J., & Stonehill, B. (2023). *Analysis of multi-activation layers in neural network architectures* [Conference presentation]. Symposium of Student Scholars, Kennesaw State University. https://digitalcommons.kennesaw.edu/undergradsymposiumksu/spring2023/presentations/19
- UNESCO. (2024a). *AI competency framework for students*. https://doi.org/10.54675/JKJB9835
- Verma, R., Maheshwari, R., Manore, D., Rane, P. S., & Raikwar, M. (2025). Supervised vs. unsupervised learning: A comparative study in modern AI system. *Communications on Applied Nonlinear Analysis, 32*(9s), 860–872.
- Zeng, B., Yin, Y., & Liu, Z. (2024). Understanding bias in large-scale visual datasets. In *Advances in Neural Information Processing Systems 37 (NeurIPS 2024)*. https://arxiv.org/abs/2412.01876

<small>Licence: CC BY 4.0 · Dr. Hannes Tegelbeckers, OVGU Magdeburg · Created with AI support (Claude), checked and revised by the author.</small>
