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
Badr ELKARFI – MSc Cybersecurity manager

<!-- 

hello My name is badr elkarfi, and today I’ll present my analysis of the RainForest project — the Customer Order Management System for ACME Distribution. I’ll walk you through the original plan, what actually happened by Week 4, why the deviations occurred, and what we can do to get the project back on track 

-->

---
layout: center
---

# Introduction

<!-- 

Before diving into the numbers, I want to share five principles that guided my analysis.
First, realistic planning — we must account for real-world constraints like HR availability and learning curves.
Second, Earned Value Management — it’s the only way to objectively measure if we’re on track.
Third, proactive risk management — because changes, like client feedback, are inevitable.
Fourth, skill-based resourcing — a Skill Level 4 developer isn’t just ‘less experienced’ — they’re 20% less productive, and that impacts timelines.
And finally, continuous client communication — because waiting until the end to show the product guarantees rework. 

-->

---
layout: image
image: gantt.png
backgroundSize: contain
---

<!--

Adjusted hours = Estimated hours × (5 / skill level)
Capacity/week = 40h × availability.
Duration (weeks) = Adjusted ÷ Capacity; 1w = 5d.
“≈” means rounded up to whole days for planning.

-->

---
layout: image
image: critical_path.png
backgroundSize: contain
---

<!--


If any task on it is late, the whole project is late
How long each task takes:
Who waits for whom
arliest start/finish pass:
Pick the chain that finishes last: that’s the critical path.

-->

---
layout: image
image: bac.png
backgroundSize: contain
---

<!--

Convert effort to hours (if in days): 1 day = 8 h.
Adjust for productivity (skill level) Adjusted hours = Estimated hours × (5 / skill level)
Cost per task: Adjusted hours × hourly rate
BAC = sum of all task costs

-->

---

# Timeline compare

| ID | Task                   | Baseline by Day 20 | Actual at Week 4 | Variance vs Baseline | 
| -: | ---------------------- | ------------------ | ---------------- | -------------------- | 
|  1 | Solution Specification | Finished           | Finished         | On time              | 
|  2 | Product Browser UI     | Finished           | Finished         | On time              | 
|  3 | Customer Order UI      | Finished           | 80%              | ≈ 1 day late         | 
|  4 | Customer Payment UI    | Finished           | Finished         | On time              | 
|  5 | Admin UI               | Finished           | 40%              | ≈ 2–3 days late      | 
| 13 | dBase Modifications    | Finished           | 25%              | ≈ 4–5 days late      |


<!--

schedule; critical path unchanged (1→2→3→7→8→12)

-->

---


# Budget compare

| Metric                       | Meaning                                                 | Formula                                | Week-4 example (t=20)              |
| ---------------------------- | ------------------------------------------------------- | -------------------------------------- | ---------------------------------- |
| Daily planned rate `r`       | Planned € “earned” per day for a task                   | `r = BAC_task / D`                     | Task 2: `r = 2280 / 8 = 285 €/day` |
| **PV per task** `PV_task(t)` | Planned € for that task earned by day `t`               | `PV_task(t) = r × L(t)`                | Task 2: `285 × 8 = €2,280`         |
| **Total PV** `PV(t)`         | Planned € earned by day `t` (all tasks)                 | `PV(t) = Σ PV_task(t)`                 | **PV(20) = €11,221**               |
| **EV per task** `EV_task(t)` | Value of work actually finished on that task by day `t` | `EV_task(t) = BAC_task × %complete(t)` | Task 3: `1520 × 0.80 = €1,216`     |
| **Total EV** `EV(t)`         | Value of all work finished by day `t`                   | `EV(t) = Σ EV_task(t)`                 | **EV(20) = €6,524**                |

<!--

earned ~58% of planned progress

-->


---
layout: center
---

# Conclusion

<!--

and to conclude, The single most important thing I learned: Project success depends on adapting to real performance data  not sticking to an unrealistic plan

-->