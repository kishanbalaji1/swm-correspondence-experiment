# Spatial Working Memory & Correspondence Experiment

**Flombaum Lab — Johns Hopkins University**

An online replication and extension of Bae, Wilson & Flombaum (2016), *"Correspondence Computations and Token Identity in Spatial Working Memory."*

---

## What this is

Participants encode the locations of colored squares, wait through a blank delay, then judge whether a single probe square moved left or right from its original position. The key methodological addition is that Consistent/Inconsistent (C/I) trial classification is **built into the design from the start** and counterbalanced, rather than applied post-hoc as in the original paper.

---

## Repository structure

```
swm-correspondence-experiment/
├── index.html        ← the full experiment (jsPsych 7)
├── README.md         ← this file
```

---

## How to run locally

Just open `index.html` in a browser. No server needed for local testing.

## How to deploy (GitHub Pages)

1. Go to your repository on GitHub
2. Settings → Pages → Source: `main` branch, `/ (root)`
3. Your experiment will be live at `https://kishanbalaji1.github.io/swm-correspondence-experiment/`

---

## Key parameters (in `index.html` → `PARAMS`)

| Parameter | Value | Note |
|---|---|---|
| Memory loads | 1–6 | Same as original paper |
| Displacements | 4–24px (6 levels) | Adjust after piloting |
| Trials per cell | 16 | Increased from 12 for online power |
| Encoding duration | 2000ms | Same as original |
| Blank delay | 900ms | Same as original |
| Response | F (left) / J (right) | No timeout |

---

## SONA integration

1. Create your study on SONA
2. Set the study URL to: `https://kishanbalaji1.github.io/swm-correspondence-experiment/?survey_code=%SURVEY_CODE%`
3. SONA automatically replaces `%SURVEY_CODE%` with each participant's code
4. Update `PARAMS.sonaRedirectURL` in `index.html` with your actual SONA completion URL

---

## Data output

Data downloads automatically as a `.csv` at the end of each session. Key columns:

- `participant_id` — SONA participant ID
- `load` — memory load (1–6)
- `displacement` — probe displacement in px
- `ci_type` — `consistent` or `inconsistent`
- `correct_direction` — `left` or `right`
- `response_direction` — participant's response
- `correct` — `true` or `false`
- `rt` — reaction time in ms

---

## References

Bae, G.-Y., Wilson, C., & Flombaum, J. I. (2016). Correspondence computations and token identity in spatial working memory. *Psychological Review* (submitted).
