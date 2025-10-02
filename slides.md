---
theme: seriph
fonts:
  sans: 'Zilla Slab'
  weights: '300'
transition: 'fade-out'
disabled: true
---

---
layout: center
class: text-center
---

# RainForest Project Report 
Your Name – MSc Project Management

---
layout: center
---

# Introduction

---
layout: image
image: gantt.png
backgroundSize: contain
---

---
layout: image
image: critical_path.png
backgroundSize: contain
---

---
layout: image
image: bac.png
backgroundSize: contain
---

---

# Timeline compare

| ID | Task                   | Baseline by Day 20 | Actual at Week 4 | Variance vs Baseline | Comment |
| -: | ---------------------- | ------------------ | ---------------- | -------------------- | ------- |
|  1 | Solution Specification | Finished           | Finished         | On time              | —       |
|  2 | Product Browser UI     | Finished           | Finished         | On time              | —       |
|  3 | Customer Order UI      | Finished           | 80%              | ≈ 1 day late         | —       |
|  4 | Customer Payment UI    | Finished           | Finished         | On time              | —       |
|  5 | Admin UI               | Finished           | 40%              | ≈ 2–3 days late      | —       |
| 13 | dBase Modifications    | Finished           | 25%              | ≈ 4–5 days late      | —       |

---

# Budget compare

| Metric                       | Meaning                                                 | Formula                                | Week-4 example (t=20)              |
| ---------------------------- | ------------------------------------------------------- | -------------------------------------- | ---------------------------------- |
| Daily planned rate `r`       | Planned € “earned” per day for a task                   | `r = BAC_task / D`                     | Task 2: `r = 2280 / 8 = 285 €/day` |
| **PV per task** `PV_task(t)` | Planned € for that task earned by day `t`               | `PV_task(t) = r × L(t)`                | Task 2: `285 × 8 = €2,280`         |
| **Total PV** `PV(t)`         | Planned € earned by day `t` (all tasks)                 | `PV(t) = Σ PV_task(t)`                 | **PV(20) = €11,221**               |
| **EV per task** `EV_task(t)` | Value of work actually finished on that task by day `t` | `EV_task(t) = BAC_task × %complete(t)` | Task 3: `1520 × 0.80 = €1,216`     |
| **Total EV** `EV(t)`         | Value of all work finished by day `t`                   | `EV(t) = Σ EV_task(t)`                 | **EV(20) = €6,524**                |

---
layout: center
---

# Conclusion