# Portfolio Build Prompts (github.io)

A ready-to-use, ordered set of prompts to build an **industry-first, research-aware** personal
portfolio website and host it free on GitHub Pages.

**How to use this file**
1. Open your AI coding assistant (Cursor, GitHub Copilot Chat, etc.) inside an empty project folder.
2. Paste the prompts **in order** (Prompt 1 first). Wait for each to finish before pasting the next.
3. Replace every `[PLACEHOLDER]` with your real info (see the list below).

---

## Before you start — fill in these placeholders

Wherever a prompt says one of these, swap in your real value:

| Placeholder | What to put |
|---|---|
| `[NAME]` | Your full name |
| `[GITHUB_USERNAME]` | Your exact GitHub username (case-sensitive) |
| `[EMAIL]` | Your contact email |
| `[LINKEDIN_URL]` | Your LinkedIn profile URL |
| `[SCHOLAR_URL]` | Google Scholar URL (skip if you don't have one) |
| `[DEGREE_AND_SCHOOL]` | e.g. "M.S. in Computer Engineering, University of X (2024–2026)" |
| `[LOCATION]` | e.g. "San Francisco, CA" |
| `[AUV_ORG]` / `[AUV_TITLE]` / `[AUV_DATES]` | The lab/company, your role, and dates for the underwater-vehicle work |
| `[PHOTO]` | A square headshot saved as `assets/profile.jpg` |
| `[RESUME_PDF]` | Your resume saved as `assets/resume.pdf` |

> **Accuracy note:** Anything you can't confirm (org names, dates, degree, publications) is left as a
> placeholder on purpose. Fill it with real values — don't ship placeholder text, and don't invent facts.

---

## Prompt 1 — Scaffold + design system

```
Build me a personal portfolio website as a single static site using only plain HTML, CSS, and
JavaScript — no framework, no build step — so it can be hosted directly on GitHub Pages at
https://[GITHUB_USERNAME].github.io.

Create this structure:
- index.html
- css/style.css
- js/main.js
- assets/           (for my photo and resume PDF)
- .nojekyll         (empty file, so GitHub Pages serves assets as-is)
- README.md         (short: what this is + how to run/deploy locally)

Design requirements:
- Clean, modern, professional look aimed at ML/AI and software engineering RECRUITERS.
- Fully responsive (looks great on mobile and desktop).
- Sticky top navigation with smooth-scroll to sections; a dark/light theme toggle that
  remembers the choice in localStorage.
- Subtle scroll-reveal animations; accessible color contrast; Google Fonts (a clean sans-serif).
- One primary accent color used consistently for buttons, links, and highlights.

I am [NAME], an ML/AI engineer looking for industry roles. Set up the page with these sections in
this exact order (I'll fill each one in follow-up prompts):
Hero, About, Experience, Projects, Skills, Research, Interests, Contact.

For now, scaffold all sections with placeholder content and wire up the nav, theme toggle, and
smooth scrolling. Keep the code well-organized and commented at the section level only.
```

---

## Prompt 2 — Hero + About

```
Fill in the Hero and About sections.

HERO:
- My name: [NAME]
- One-line title: "Machine Learning / AI Engineer"
- A short, punchy tagline (industry-focused): I build and ship AI systems — on-device models,
  LLM agents, and perception for autonomous systems — that work in the real world.
- Put my email [EMAIL] directly under my name.
- Buttons: "View Projects" (scrolls to Projects) and "Download Resume" (links to assets/resume.pdf).
- Social links with icons: GitHub (https://github.com/[GITHUB_USERNAME]), LinkedIn ([LINKEDIN_URL]),
  and Google Scholar ([SCHOLAR_URL] — omit if empty). Show my headshot from assets/profile.jpg,
  and fall back to my initials if the image is missing.

ABOUT (2–3 short paragraphs, professional and concrete, no fluffy filler):
- I'm an ML/AI engineer ([DEGREE_AND_SCHOOL]) who builds practical AI systems end to end — from
  data pipelines and model fine-tuning to efficient on-device deployment.
- My work spans on-device/edge AI, LLM agents and retrieval, autonomous-systems navigation and
  perception, and applied healthcare ML. I care about models that are efficient, reliable, and
  actually deployable, not just accurate on a benchmark.
- Based in [LOCATION]. Currently seeking full-time industry roles in ML/AI engineering.
```

---

## Prompt 3 — Experience

```
Fill in the Experience section as a clean, scannable timeline. Two entries, most recent first.
Bold the key technologies and keep the metrics prominent.

ENTRY 1 — Autonomous Underwater Vehicle Research
Organization: [AUV_ORG]
Role: [AUV_TITLE]
Dates: [AUV_DATES]
Bullets:
- Boosted mission endurance by up to 45% and exceeded performance targets in 55%+ of test scenarios.
- Developed and benchmarked a hybrid A* + Artificial Potential Field (APF) navigation system with
  real-time sensor fusion (sonar, IMU, depth sensors).
- Evaluated across 200+ randomized environments, achieving statistically significant path-planning
  improvements (p < 0.001) and generating data-driven mission-optimization and operating-depth
  recommendations.

ENTRY 2 — The Smart Bridge (Tamil Nadu, India)
Role: Applied Data Science Intern
Dates: May 2023 – July 2023
Bullets:
- Developed a clinical AI system for early Chronic Kidney Disease (CKD) detection using ensemble
  machine learning and automated data pipelines, achieving 97% accuracy across held-out datasets
  and 50+ patient cases.
- Built scalable healthcare data and analytics infrastructure, transforming fragmented multi-source
  patient records into audit-ready ML datasets and interactive risk-intelligence dashboards, enabling
  rapid population-level screening and data-driven clinical interventions.
```

---

## Prompt 4 — Projects

```
Fill in the Projects section as a responsive grid of cards. Each card: a short tech-tag line, a
title, a 1–2 sentence description, key metrics highlighted, the tech stack, dates, and a
placeholder link labeled "GitHub / demo" (I'll add real URLs later). Lead with impact and metrics.

PROJECT 1 — SnapOn: Offline On-Device Visual Memory Assistant
Tech: Android, Kotlin, PyTorch, ExecuTorch, SmolVLM, Whisper
Dates: June 2026 – July 2026
Description: A fully offline AI assistant for the Samsung Galaxy S25 Ultra (Snapdragon 8 Elite) —
point the camera, ask questions by voice, and save answers as semantically searchable memories,
with zero cloud calls or data leaving the device. Quantized SmolVLM-500M (vision-language) and
Whisper tiny.en (speech-to-text) to INT8 via ExecuTorch/XNNPACK, added on-device TTS and a
SQLite-backed retrieval layer for cross-session recall; prototyped as a Flask/PyTorch desktop demo,
then ported to a native Android app with CameraX and direct on-device inference.

PROJECT 2 — NVIDIA Nemotron Reasoning Benchmark
Tech: LoRA, Reinforcement Learning, Fine-tuning
Dates: March 2026 – June 2026
Description: Fine-tuning Nemotron-3-Nano-30B with LoRA adapters on a novel NVIDIA reasoning
benchmark — exploring synthetic data generation, advanced prompting, and RL-based training pipelines
to improve multi-step logical reasoning while staying efficient on constrained hardware via
parameter-efficient fine-tuning.

PROJECT 3 — Novabot: AI-Powered Email & Calendar Assistant
Tech: Python, LLMs, LangChain, Gmail API, Google Calendar API
Dates: January 2026 – April 2026
Description: An LLM-based personal assistant that unifies multiple email accounts and calendars into
one conversational interface — semantic search, inbox prioritization, meeting extraction, scheduling
automation, and natural-language Q&A — cutting the context-switching overhead of managing fragmented
inboxes.

PROJECT 4 — Terrain Mapping from LiDAR: Hybrid 3D/2D Deep Learning
Tech: Python, PyTorch, KPConv, U-Net, SemanticKITTI
Dates: January 2026 – April 2026
Description: Built 2D U-Net, 3D KPConv, and hybrid LiDAR semantic-segmentation models on
SemanticKITTI — 98.7% pixel accuracy, 0.761 mIoU, and ~30 ms inference for real-time autonomous
driving. A 2D–3D feature-fusion design (KPConv + U-Net with spatial projection) improved Obstacle
IoU by 51% (0.585 → 0.885) and Traversable-Terrain IoU by 18% (0.776 → 0.917) via class balancing
and multimodal feature learning.
```

---

## Prompt 5 — Skills

```
Fill in the Skills section as grouped "chip"/tag lists (one row of chips per group, with a group
heading). Use exactly these groups and items:

- Languages: Python, C++, Java, SQL, MATLAB, Bash
- AI/ML: Machine Learning, Deep Learning, Generative AI, Large Language Models (LLMs),
  Vision-Language Models (VLMs), Retrieval-Augmented Generation (RAG), LoRA, NLP, Computer Vision,
  Reinforcement Learning, Multi-Agent AI
- Frameworks & Libraries: PyTorch, TensorFlow, Scikit-Learn, Hugging Face, LangChain, LangGraph,
  vLLM, FAISS, LlamaIndex, OpenCV, NumPy, Pandas, Streamlit, Flask, FastAPI
- Data & MLOps: Data Pipelines, ETL, Feature Engineering, Information Retrieval, Semantic Search,
  Vector Databases, Model Training, Fine-Tuning, Inference Optimization, Model Deployment,
  Experiment Tracking
- Systems & Cloud: AWS (EC2, S3), Docker, Linux/UNIX, Git, REST APIs, CI/CD, Data Structures &
  Algorithms, Object-Oriented Programming, System Design, Distributed Systems, Autonomous Systems,
  Sensor Fusion, Path Planning

Make the chips visually consistent with the site's accent color and hover states.
```

---

## Prompt 6 — Research

```
Fill in the Research section. Keep it compact and clearly SECONDARY to the industry work above — a
brief "Research" block that signals depth without dominating the page. Two short summaries:

1. Autonomous Navigation for Underwater Vehicles — Designed and benchmarked a hybrid A* + Artificial
   Potential Field navigation system with multi-sensor fusion (sonar, IMU, depth), demonstrating
   statistically significant path-planning gains (p < 0.001) across 200+ randomized environments and
   up to 45% improvement in mission endurance.

2. Applied Clinical Machine Learning — Built an ensemble-ML system for early Chronic Kidney Disease
   detection reaching 97% accuracy, together with the healthcare data infrastructure needed to turn
   fragmented patient records into audit-ready ML datasets for population-level screening.

Add a placeholder line "Publications & preprints: [add links here]" that I can fill in or delete.
Do not invent any publications, venues, or citations.
```

---

## Prompt 7 — Interests

```
Fill in the Interests section so my profile feels holistic — not just a list of job skills. Present
it as a small set of cards or tags with a one-line note each.

Technical interests:
- On-device / edge AI and model efficiency (quantization, on-device inference)
- LLM agents, RAG, and applied generative AI
- Autonomous systems: robotics, navigation, sensor fusion, path planning
- Multimodal perception (vision-language models, LiDAR, computer vision)
- Applied healthcare AI and real-world ML deployment

Also include a short, friendly "Beyond work" line with 3–4 personal interests — leave it as
[ADD_PERSONAL_INTERESTS] for me to fill in (e.g., hobbies, sports, travel, volunteering, music), so
the section shows I'm a well-rounded person, not just an engineer.
```

---

## Prompt 8 — Contact + footer

```
Fill in the Contact section and footer.

CONTACT: a short, warm line inviting recruiters and collaborators to reach out, followed by a row of
cards/buttons, each with the service's icon in its real brand colors:
- Email: [EMAIL]
- GitHub: https://github.com/[GITHUB_USERNAME]
- LinkedIn: [LINKEDIN_URL]
- Google Scholar: [SCHOLAR_URL]  (omit this card if I don't have one)

FOOTER: "© <current year> [NAME]" with the year auto-updating in JavaScript, plus a "Back to top" link.
```

---

## Prompt 9 — Deploy to GitHub Pages

```
Help me deploy this to GitHub Pages so it's live at https://[GITHUB_USERNAME].github.io.

Give me the exact steps and terminal commands to:
1. Create a new PUBLIC GitHub repository named exactly [GITHUB_USERNAME].github.io (empty — no README).
2. Initialize git here, commit everything, and push to that repo's main branch.
3. Enable GitHub Pages (Settings → Pages → Deploy from a branch → main / root).
4. Verify the site is live and tell me how long it usually takes to appear.

Also add a .gitignore for macOS/editor junk (.DS_Store, .vscode/, .idea/), and remind me to put my
photo (assets/profile.jpg) and resume (assets/resume.pdf) in the assets folder before pushing.
```

---

## Optional polish prompts (use as needed)

```
Do a final polish pass: check mobile responsiveness at 375px width, verify the dark/light toggle on
every section, ensure all links open correctly (external links in a new tab), tighten spacing so 3–4
project cards are visible at a glance, and fix any accessibility issues (alt text, color contrast,
focus states).
```

```
Add subtle metric "stat" callouts to the top project cards (e.g., "97% accuracy", "0.761 mIoU",
"INT8 on-device") so recruiters catch the impact within seconds.
```
