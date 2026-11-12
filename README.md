# Patient Flow Simulator

Test changes to your emergency pathway before you make them in the hospital.

### ▶ [Open the Patient Flow Simulator](https://storehouse-dev38.github.io/PatientFlow/)

Free to use in your browser. There's nothing to install and no sign-in, and no patient data is needed. Everything you enter stays on your own computer.

![The Patient Flow Simulator](docs/img/pathway-overview.png)

---

## What it's for

Hospitals constantly propose changes to the emergency and non-elective pathway: more AMU beds, a bigger SDEC, earlier discharges, better weekend discharge, reducing delayed discharges. It's rarely clear in advance which will actually help, or whether a change will just move the queue somewhere else.

The simulator lets you try these changes on a model of your hospital and see the knock-on effects across the whole pathway, from ambulance handover through ED, assessment and the wards to discharge.

It has two tools, one on each tab:

| Tab | Use it to answer |
|---|---|
| **Whole pathway** | Where is our bottleneck? What would a change do to ED 4-hour and 12-hour performance, ambulance handover, escalation beds, occupancy and length of stay? |
| **SDEC design** | Should our SDEC streams share one unit or stay separate? Where should it go, how big should it be, and what hours should it open? Would sharing space hurt our smaller pathways? |

---

## Getting started

### Whole pathway

1. **Choose a starting point.** Pick the preset closest to your hospital (large acute, medium or small district general) and whether you want wards grouped by division or by specialty.
2. **Make it match your hospital.** Enter your daily arrivals, bed numbers, lengths of stay and delayed-discharge figures. Click any unit on the bed board to edit it.
3. **Run the model** and compare the results with your real performance. Adjust until they're close; this is what makes the comparisons trustworthy.
4. **Pin as baseline.**
5. **Change one thing** — add beds, move the discharge curve earlier, cut delays — and **re-run**. Every result shows the change against your baseline.

![Pathway flow map](docs/img/pathway-flow-map.png)

### SDEC design

1. **Set up your streams** (medical, surgical, older persons, gynae, or your own) with their daily demand, spaces and staff.
2. **Choose the layout, location and hours** you want to test.
3. **Run the model.** It automatically compares separate and shared units on the same patients, tests a range of sizes and closing times, and checks what a busy day in one stream does to the others.

![Who gains and who loses from sharing space](docs/img/sdec-bleed-check.png)

---

## Reading the results

After each run, the **"What this run is telling you"** panel explains the results in plain English: what's limiting flow, why, and what to look at next.

**Key measures — whole pathway**

| Measure | What it means |
|---|---|
| ED 4-hour / 12-hour | % of patients leaving ED within 4 hours, and % taking over 12 hours |
| Ambulance handover | % of ambulance arrivals waiting over an hour to be handed over |
| Escalation | Escalation beds in use on average and at peak |
| NCTR census | Patients in beds with no criteria to reside |
| Admitted LOS | Average ward stay |
| Bottleneck ranking | Which unit is holding up flow, and by how much |

**Key measures — SDEC design**

| Measure | What it means |
|---|---|
| Seen in SDEC | Patients seen per day, out of those who were suitable |
| Lost to ED / AMU | Suitable patients who went elsewhere because SDEC was closed, full or too far away |
| Wait to be seen | Time from reaching SDEC to being seen by a clinician |
| Bleed check | For each stream: does sharing space help or hurt it? |
| Bed-days saved | Admissions avoided, converted to beds |

![SDEC demand, capacity and size](docs/img/sdec-charts.png)

---

## Tips for reliable answers

- **Compare, don't forecast.** The simulator is built to compare options. "Option A is better than option B" is much more reliable than "ED will hit 71%".
- **Change one thing at a time** against a pinned baseline, so you know what caused the difference.
- **Try a few random seeds.** Change the seed in Run settings and re-run. If the answer holds, it's robust.
- **Single changes often disappoint.** Adding beds in one place usually moves the queue rather than removing it. Try combinations, such as more AMU beds together with fewer discharge delays.
- **Check the working.** On the SDEC tab, "Show the working" sets out the rules, checks the sums, and lists sample patient journeys you can sense-check with clinical colleagues.

---

## Saving and sharing scenarios

- **Save current setup** keeps a scenario in your browser so it's there next time. It's only on that browser and device, so clearing your browser data removes it.
- **Export config** gives you the full setup as text you can email or send by Teams. Your colleague pastes it into **Import config** to see exactly what you saw.

---

## Your data

- The simulator runs entirely in your browser. Nothing you enter is sent anywhere or stored on any server.
- It needs no patient data: only numbers such as daily arrivals, bed counts and average lengths of stay.
- There is no tracking and there are no cookies.

---

## Good to know

The simulator is a simplified model of a hospital, designed to compare options rather than predict exact figures. It does not include elective activity, seasonal variation or staffing levels on the wards. In SDEC, test and result times are fixed and don't lengthen when the unit is busy.

Use it to explore options, test ideas and explain why a change will or won't help. For major investment decisions, confirm your preferred option with detailed analysis using your own patient-level data.

For analysts and reviewers, the [technical specification](docs/TECHNICAL-SPEC.md) sets out every rule, assumption and check.

---

© EFG Apps. All rights reserved.
