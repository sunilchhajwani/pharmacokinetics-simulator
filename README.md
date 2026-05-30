# 💊 Pharmacokinetics Simulator

An interactive, single-file HTML pharmacokinetics simulator designed for clinical education. Simulate drug dosing, visualize concentration-time curves, practice dose adjustments, and learn PK concepts from beginner to advanced — all in the browser, no installation needed.

**Live Demo:** Open `Pharmacokinetics-Simulator.html` in any modern browser.

---

## ✨ Features

### 📊 Main Simulator
- **46 drugs** — Vancomycin, Gentamicin, Amikacin, Phenytoin, Digoxin, Lithium, Meropenem, Ciprofloxacin, and 38 more
- **3 dosing routes** — IV Bolus, IV Infusion, Oral with absorption
- **Real-time concentration-time chart** with therapeutic range (green band), toxic threshold (red line), steady-state marker, and MIC overlay
- **Patient-specific PK** — Cockcroft-Gault CrCl, Schwartz pediatric CrCl, IBW/ABW/TBW weight basis
- **Bayesian TDM** — Enter measured levels, back-calculate individual ke/t½/CL, get 3 dose adjustment suggestions
- **AUC-guided dosing** — Vancomycin AUC24/MIC with trapezoidal rule
- **Loading dose calculator** — Auto-calculate from target Cp × Vd / F
- **Physiological modifiers** — Pregnancy, heart failure, burns, smoking, hepatic impairment, dialysis modes
- **Drug interactions** — 280+ CYP/P-gp interaction pairs
- **Pediatric mode** — Weight-based dosing with max dose cap
- **Drug comparison** — Save and overlay two regimens on the same chart
- **PK dosing report** — Printable report with safety alerts

### 📖 Study Tab
- **Chart Reading Guide** — 8 interactive steps that annotate the chart, explaining each element in plain English (concentration curve, therapeutic range, toxic threshold, peak/trough, dose markers, steady state, half-life, full summary)
- **Clinical Practical Tips** — 16 bedside-knowledge tip cards across 6 categories (Dosing, Levels, Renal, Mistakes, Vancomycin, Aminoglycoside), each linking to the chart
- **Dose Adjustment Sandbox** — Practice real clinical dose adjustments with instant feedback (see below)
- **PK Concept Explorer** — Drag sliders for Vd, CL, F and watch the curve reshape in real-time
- **Clinical Simulations** — 8 multi-step patient scenarios with scoring (Vancomycin ICU, Gentamicin OD, Phenytoin Status, Lithium Overdose, Pediatric, Renal Decline, Drug Interactions, Aminoglycoside TDM)
- **Show the Math** — Step-by-step formula walkthroughs with actual patient values
- **PK Glossary** — 26 terms with definitions and clinical significance

### 🎯 Dose Adjustment Sandbox
The sandbox is the core practical learning tool — it presents a clinical scenario and lets you adjust the dose/interval, then evaluates your decision in real-time.

**12 Clinical Scenarios:**

| # | Scenario | Drug | Difficulty |
|---|---------|------|-----------|
| 1 | Subtherapeutic trough | Vancomycin | Easy |
| 2 | Renal impairment — extend interval | Vancomycin | Easy |
| 3 | Toxic trough, normal kidneys | Vancomycin | Easy |
| 4 | AKI developing mid-therapy | Vancomycin | Medium |
| 5 | Obese patient, wrong weight basis | Vancomycin | Medium |
| 6 | Once-daily gentamicin — subtherapeutic peak | Gentamicin | Medium |
| 7 | Aminoglycoside — low peak + high trough | Gentamicin | Medium |
| 8 | Phenytoin nonlinear kinetics | Phenytoin | Medium |
| 9 | Drug interaction — amiodarone + digoxin | Digoxin | Hard |
| 10 | CRRT patient — needs MORE drug | Vancomycin | Hard |
| 11 | Pediatric vancomycin | Vancomycin | Hard |
| 12 | Lithium + NSAID toxicity | Lithium | Hard |

**4 Learning Levels:**
- 📖 **Guided** — Step-by-step walkthrough (5 steps: Read Level → Assess Patient → Identify Problem → Choose Strategy → Adjust)
- 🤝 **Assisted** — Interactive dose/interval sliders + hints + "Why did you choose this?" reasoning questions
- 🎯 **Independent** — No hints, scored 0–3 (dangerous → acceptable → good → optimal)
- ⚡ **Timed** — 2-minute countdown challenge

**Feedback Engine** evaluates every decision on 3 axes:
- **Safety** — Are toxic levels predicted? (✓/✗)
- **Efficacy** — Is the trough in the therapeutic range? (✓/⚠/✗)
- **Approach** — Did you follow the right clinical principle? (e.g., "extend interval first in renal impairment")

**Before/After Chart Overlay** — Pink dashed line = original regimen, blue solid = your adjustment, both visible at once.

**6 Pattern Recognition Cards:**
1. Low Trough, Normal Kidneys → Increase dose
2. High Trough, Low CrCl → Extend interval first
3. High Trough, Normal Kidneys → Reduce dose or extend
4. AKI Mid-Therapy → Hold → Check → Restart adjusted
5. Aminoglycoside: Low Peak + High Trough → Increase dose AND extend interval
6. Drug Interaction Raises Levels → Reduce dose, monitor closely

**7 Achievement Badges:** 🥼 First Adjustment · 🎯 On Target · 🧠 Pattern Master · 🏥 Renal Expert · ⚡ Speed Doser · 🏆 Clinical Pharmacist · 💎 Perfect Score

### 📚 Learn Tab — 8-Chapter Learning Path
Structured curriculum from basics to clinical mastery:

1. **What is Pharmacokinetics?** — ADME, the 4 PK parameters
2. **Volume of Distribution** — Bathtub analogy, clinical implications
3. **Clearance & Half-Life** — Drain analogy, steady-state timing
4. **Routes & Loading Dose** — IV bolus vs infusion vs oral, when to load
5. **Multiple Dosing & Steady State** — Accumulation, 4–5 half-lives rule
6. **Renal Dosing** — Cockcroft-Gault, when to reduce dose vs extend interval
7. **Therapeutic Drug Monitoring** — When/how to draw levels, Bayesian dosing
8. **Capstone: Vancomycin in Renal Failure** — Complete clinical workup

Each chapter includes:
- **Concept explanations** in plain language with real-world analogies
- **"In Practice" steps** with bedside tips, common mistakes, and chart connections
- **Interactive demos** with auto-set chart parameters
- **Quiz questions** with detailed explanations
- **Progress tracking** saved to localStorage

---

## 🚀 Getting Started

1. Download or clone this repo
2. Open `Pharmacokinetics-Simulator.html` in Chrome, Firefox, Safari, or Edge
3. That's it — no server, no install, no dependencies

## 🛠 Technical Details

- **Single HTML file** — All CSS, JS, and content in one self-contained file
- **Pure vanilla JS** — No frameworks, no build tools, no CDN dependencies
- **Canvas-based charting** — All graphs drawn on HTML5 Canvas
- **localStorage persistence** — Learning progress and sandbox scores saved locally
- **Responsive layout** — Works on desktop (sidebar + chart)

## ⚠️ Disclaimer

**For educational purposes only. NOT for clinical decision-making.** All dosing decisions must be validated by a licensed clinical pharmacist or physician using institutional protocols and validated laboratory results.

## 📄 License

This project is open source. See repository for license details.
