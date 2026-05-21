---
title: "Chapter 3: Neurochemistry and Psychopharmacology"
description: "From resting potential and action potentials to neurotransmitters, hormones, and psychoactive drugs — this chapter covers the electrochemical language of the nervous system and how drugs alter it."
generated_by: "claude skill chapter-content-generator"
date: 2026-05-21
version: 0.08
---

# Chapter 3: Neurochemistry and Psychopharmacology

## Summary

This chapter examines the electrochemical basis of neural communication,
from resting potential and action potentials to synaptic transmission and
reuptake. Students learn the eight major neurotransmitters and five hormones
in AP scope, and explore how psychoactive drugs — stimulants, depressants,
opioids, and hallucinogens — alter neural function. The chapter also covers
tolerance, addiction, withdrawal, and circadian rhythms driven by melatonin.

## Concepts Covered

This chapter covers the following 35 concepts from the learning graph:

1. All-or-None Principle
2. Neural Transmission
3. Resting Potential
4. Depolarization
5. Synaptic Threshold
6. Action Potential
7. Refractory Period
8. Neurotransmitters
9. Reuptake
10. Dopamine
11. Serotonin
12. Norepinephrine
13. Glutamate
14. GABA
15. Endorphins
16. Acetylcholine
17. Substance P
18. Hormones and Behavior
19. Psychoactive Drugs
20. Adrenaline (Epinephrine)
21. Leptin
22. Ghrelin
23. Melatonin
24. Oxytocin
25. Agonists
26. Antagonists
27. Reuptake Inhibitors
28. Stimulants
29. Depressants
30. Hallucinogens
31. Opioids
32. Drug Tolerance
33. Circadian Rhythms
34. Addiction
35. Withdrawal Symptoms

## Prerequisites

This chapter builds on concepts from:

- [Chapter 1: Foundations of Psychology and Research Methods](../01-foundations-research-methods/index.md)
- [Chapter 2: Biological Bases of Behavior: Neurons and the Brain](../02-biological-bases-behavior/index.md)

---

## 3.1 Neural Transmission: The Electrical Side

!!! mascot-welcome
    <img src="../../img/mascot/welcome.png" alt="Psy the Owl welcoming you to Chapter 3" style="float:right;width:120px;margin:0 0 1em 1em;">
    **Welcome to Chapter 3 — where we learn the language neurons speak!**

    Every thought, memory, and emotion you have depends on billions of neurons firing electrochemical signals at each other dozens of times per second. In this chapter we are going to trace that process step by step — from the quiet resting state of an idle neuron, through the lightning-fast action potential, across the synapse, and all the way to the drugs and hormones that hijack or enhance those signals.

    This chapter connects biology, chemistry, and psychology in a way that appears throughout the AP exam — so building a solid mental model here pays dividends in every chapter that follows.

    *Let's think about that!* 🦉

**Neural transmission** is the process by which information moves through the nervous system as electrochemical signals. Understanding it requires thinking about neurons at two timescales: first the *electrical* events inside a single neuron, and then the *chemical* events between neurons at the synapse. This section covers the electrical side.

### Resting Potential: The Neuron on Standby

When a neuron is not firing, it is not inactive — it is actively maintaining a charged state called the **resting potential**. The inside of the neuron sits at approximately −70 millivolts (mV) relative to the outside. This negative charge exists because sodium ions (Na⁺) are kept outside the cell by protein pumps, while negatively charged proteins and potassium ions (K⁺) remain inside. The resulting electrochemical imbalance is stored potential energy — the neuron is essentially a tiny battery, primed to discharge.

The sodium-potassium pump continuously expels three Na⁺ ions for every two K⁺ ions it pulls in, maintaining the −70 mV baseline. This pumping costs energy (in the form of ATP), which is why neurons are among the most metabolically active cells in the body.

### Depolarization and the Action Potential

**Depolarization** occurs when incoming signals cause the neuron's membrane to become less negative — the inside voltage moves toward zero and beyond. This happens when ion channels open in response to chemical or electrical stimulation, allowing Na⁺ to rush into the cell down its concentration gradient. If depolarization reaches the **synaptic threshold** — typically around −55 mV — something dramatic happens: an **action potential** is triggered.

An **action potential** is an explosive, all-or-nothing electrical impulse that travels the full length of the axon. Once the threshold is crossed, Na⁺ floods in so rapidly that the membrane potential surges to about +40 mV. Almost immediately, K⁺ channels open and potassium rushes out, driving the membrane back toward its resting charge — a process called repolarization. The entire event lasts about one millisecond.

The **All-or-None Principle** states that once the threshold is reached, the action potential fires at full strength — there is no such thing as a "weak" action potential. If the threshold is not reached, nothing happens. This is analogous to a gun trigger: you can apply gentle pressure indefinitely, but only when you pass the threshold does the gun fire, always with the same force. The *intensity* of a stimulus is coded not by the size of each action potential but by the *frequency* — how many per second.

### The Refractory Period

Immediately after an action potential, the neuron enters the **refractory period** — a brief interval (roughly 1–3 milliseconds) during which it cannot fire again. During the *absolute refractory period* (the first ~1 ms), no stimulus, no matter how strong, can trigger another action potential; sodium channels are temporarily inactivated. During the subsequent *relative refractory period*, a stronger-than-usual stimulus can trigger firing, but normal-strength signals cannot. The refractory period sets an upper limit on firing frequency (typically 200–500 action potentials per second) and ensures the signal travels in one direction only — back along the path it came from cannot re-fire because those sections are still refractory.

#### Diagram: Action Potential — Voltage Over Time

<details markdown="1">
<summary>Interactive: Action Potential MicroSim</summary>

This interactive simulation lets you explore how an action potential unfolds across time. Use the stimulus slider to set input strength, then watch the membrane voltage graph animate in real time, with Na⁺ and K⁺ ion flows illustrated as arrows on a neuron cross-section. Threshold, depolarization peak, repolarization, and the refractory period are each highlighted in distinct colors.

**Specification for MicroSim: Action Potential Visualizer**

*Build as a p5.js animation with two panels: (left) a cross-section of the axon membrane showing Na⁺/K⁺ channels opening and closing with animated ion movement; (right) a voltage-vs-time graph that plots in real time as the animation plays. Controls: "Stimulus Strength" slider (0–100%), "Play / Pause" button, "Reset" button. When stimulus < threshold, graph flatlines and a tooltip reads "Below threshold — no action potential." When stimulus ≥ threshold, the full action potential curve animates. Phase labels appear on the curve: Resting (−70 mV), Threshold (−55 mV), Depolarization peak (+40 mV), Repolarization, Hyperpolarization, Refractory Period. Color code: resting = blue, depolarization = orange, repolarization = green, refractory = gray.*

*File location when built: `docs/sims/action-potential/`*
*Iframe height when embedded: 560px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/action-potential/main.html"
        width="100%" height="560" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

---

## 3.2 Synaptic Transmission: The Chemical Side

Neurons do not physically touch each other. Between the axon terminal of one neuron (the **presynaptic** neuron) and the dendrite or cell body of the next (the **postsynaptic** neuron) lies a microscopic gap called the **synaptic cleft**. Communication across this gap is chemical, not electrical.

**Neurotransmitters** are chemical messengers synthesized and stored in tiny vesicles inside the axon terminal. When an action potential reaches the terminal, it triggers the vesicles to fuse with the membrane and release neurotransmitters into the synaptic cleft — a process called exocytosis. Neurotransmitter molecules then drift across the cleft and bind to specialized **receptor sites** on the postsynaptic membrane. A receptor site is a protein shaped to accept only specific neurotransmitters — a molecular lock-and-key system. Binding either excites or inhibits the postsynaptic neuron depending on the receptor type.

After binding, neurotransmitters are cleared from the cleft in three ways: (1) **enzymatic degradation** — enzymes break them down; (2) **diffusion** — they drift away; or (3) **reuptake** — the presynaptic neuron reabsorbs them through transporter proteins for recycling. **Reuptake** is particularly important because many psychoactive drugs (especially antidepressants) work by blocking transporter proteins and thereby prolonging the neurotransmitter's time in the cleft.

#### Diagram: Synaptic Cleft and Neurotransmitter Release

<details markdown="1">
<summary>Interactive: Synaptic Anatomy Infographic Overlay</summary>

This interactive infographic overlay labels the key structures of the synapse. Click any callout marker to reveal the structure's name, definition, and functional role. Use the "Explore" mode to browse all labels freely, or switch to "Quiz" mode to test your recall by placing labels on the correct structures.

**Specification for Interactive Infographic Overlay: Synaptic Cleft**

*Build using the shared diagram.js library (interactive-infographic-overlay approach). Base image: a clean scientific illustration of a synapse cross-section showing presynaptic terminal, synaptic vesicles, synaptic cleft, postsynaptic membrane, receptor sites, neurotransmitter molecules, reuptake transporter, and mitochondria. Callout markers for: (1) Axon Terminal / Presynaptic Neuron, (2) Synaptic Vesicle, (3) Neurotransmitter Molecules, (4) Synaptic Cleft, (5) Receptor Site (postsynaptic), (6) Postsynaptic Membrane, (7) Reuptake Transporter, (8) Mitochondria. Each marker opens a panel with the term, a 2-sentence definition, and a clinical/pharmacological relevance note. Include Explore and Quiz modes.*

*File location when built: `docs/sims/synaptic-cleft-infographic/`*
*Iframe height when embedded: 580px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/synaptic-cleft-infographic/main.html"
        width="100%" height="580" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

### Signal Transduction at Receptor Sites

Once a neurotransmitter binds to a postsynaptic receptor, the signal must be converted into an intracellular response — a process called **signal transduction**. Some receptors (ionotropic receptors) directly open ion channels, producing fast responses in milliseconds. Others (metabotropic receptors, commonly **G-protein coupled receptors** or GPCRs) trigger a slower intracellular cascade involving second messengers like cyclic AMP (cAMP). GPCRs are significant because they are the target of many hormones and psychoactive drugs.

The interactive diagram below shows the GPCR/cAMP signaling pathway in detail. As you explore it, notice how the signal is amplified at each step — one neurotransmitter molecule can activate multiple G-proteins, each activating multiple enzyme molecules, each producing dozens of cAMP molecules. This amplification makes chemical signaling both powerful and sensitive to disruption.

<iframe src="../../sims/signal-transduction-pathway/main.html" height="590" width="100%" scrolling="no"></iframe>

!!! mascot-tip
    <img src="../../img/mascot/tip.png" alt="Psy the Owl with a tip" style="float:right;width:100px;margin:0 0 1em 1em;">
    **Keeping "pre" and "post" straight:**

    Think of the synapse like a conversation. The *presynaptic* neuron is the *speaker* — it releases neurotransmitters. The *postsynaptic* neuron is the *listener* — it receives them. Reuptake is the speaker "taking back their words." Receptor sites are the listener's "ears."

    On the AP exam, questions about drugs almost always hinge on whether a substance acts at the pre- or postsynaptic side, and whether it mimics or blocks the neurotransmitter. *Let's think about that!* 🦉

---

## 3.3 The Eight AP Neurotransmitters

The AP Psychology curriculum emphasizes eight neurotransmitters. Before exploring them interactively, read through the table below to build a baseline understanding of each one's primary role, brain regions involved, and what happens when its activity is disrupted.

A **neurotransmitter** is any chemical messenger released by a neuron that influences another neuron, muscle cell, or gland. The same neurotransmitter can be excitatory in one synapse and inhibitory in another, depending on the type of receptor it binds.

| Neurotransmitter | Primary Role | Too Much | Too Little |
|---|---|---|---|
| **Dopamine** | Movement, reward, motivation, attention | Schizophrenia (positive symptoms) | Parkinson's disease, depression |
| **Serotonin** | Mood, sleep, appetite, impulse control | Serotonin syndrome (rare, toxic) | Depression, anxiety, OCD |
| **Norepinephrine** | Arousal, alertness, fight-or-flight, attention | Anxiety, hypertension | Depression, ADHD |
| **Glutamate** | Primary excitatory signal; learning and memory | Seizures, excitotoxicity (neuron death) | Cognitive slowing |
| **GABA** | Primary inhibitory signal; reduces anxiety | Sedation, loss of coordination | Anxiety, seizures |
| **Endorphins** | Pain relief, pleasure, euphoria after exercise | Mild euphoria | Increased pain sensitivity |
| **Acetylcholine** | Muscle activation, attention, memory, REM sleep | Muscle spasms (cholinergic crisis) | Alzheimer's disease, memory loss |
| **Substance P** | Pain transmission; mood and stress | Increased pain sensitivity, stress | Reduced pain signal (rare) |

### Dopamine

**Dopamine** is often called the "reward molecule," but its role is more precisely described as mediating *anticipation* and *motivation* — the wanting system more than the liking system. The mesolimbic dopamine pathway (from the ventral tegmental area to the nucleus accumbens) is the brain's primary reward circuit. Every pleasurable activity — eating, sex, social approval — triggers dopamine release here, reinforcing the behavior. **Norepinephrine** (also called noradrenaline) is chemically related to dopamine (one step further along the same synthesis pathway) and drives the brain's arousal and alertness systems, particularly during stress and physical danger.

### Serotonin

**Serotonin** is synthesized primarily in the raphe nuclei of the brainstem and projects widely throughout the brain and spinal cord. It is best known for its role in mood regulation — chronically low serotonin activity is associated with depression, anxiety disorders, and obsessive-compulsive disorder. Serotonin also regulates sleep onset, appetite, and social behavior. About 90% of the body's serotonin is actually found in the gastrointestinal tract, where it regulates intestinal movements — a fact that explains why many serotonin-targeting antidepressants cause gastrointestinal side effects.

### Glutamate and GABA

**Glutamate** is the brain's main *excitatory* neurotransmitter — it increases the likelihood that the postsynaptic neuron will fire. It is involved in virtually every fast excitatory synapse in the brain and is essential for **long-term potentiation (LTP)**, the synaptic strengthening thought to underlie learning and memory. In contrast, **GABA** (gamma-aminobutyric acid) is the main *inhibitory* neurotransmitter. It reduces neuronal excitability throughout the nervous system. Think of glutamate as pressing the accelerator and GABA as applying the brakes — the brain needs both in careful balance. When GABA activity is too low, neurons fire uncontrollably, producing anxiety and potentially seizures. Alcohol, benzodiazepines (like Valium), and barbiturates all work by enhancing GABA activity.

### Endorphins, Acetylcholine, and Substance P

**Endorphins** (endogenous morphine) are neuropeptides released by the pituitary gland and neurons in response to pain and intense exercise. They bind to the same opioid receptors as morphine and heroin, producing analgesia (pain relief) and euphoria. The "runner's high" experienced after sustained aerobic exercise reflects endorphin release. **Acetylcholine (ACh)** was the first neurotransmitter discovered. It is the primary messenger at all neuromuscular junctions — every voluntary muscle contraction depends on ACh. In the CNS, ACh is critical for attention, memory consolidation, and REM sleep. Alzheimer's disease involves significant loss of cholinergic neurons in the basal forebrain. **Substance P** is a neuropeptide that transmits pain signals from peripheral pain receptors to the spinal cord and brain. It also plays a role in mood regulation and stress responses; elevated Substance P activity is associated with depression and inflammatory conditions.

#### Diagram: Neurotransmitter Function Explorer

<details markdown="1">
<summary>Interactive: Neurotransmitter Matching Activity</summary>

This interactive activity presents a card-matching game for all eight AP neurotransmitters. In "Learn" mode, clicking a neurotransmitter card reveals its role, associated brain region, deficiency disorder, and excess disorder. In "Match" mode, drag each neurotransmitter name to its correct function description. In "Quiz" mode, scenario cards describe a symptom (e.g., "a patient develops tremors and has difficulty initiating movement") and you must identify the likely neurotransmitter imbalance.

**Specification for MicroSim: Neurotransmitter Function Explorer**

*Build as a p5.js card-flip activity. Eight cards, each with a neurotransmitter name on front and a 3-field info panel on back: (1) Primary Function, (2) Deficiency → Disorder, (3) Excess → Disorder. Three modes switchable by tab: Learn (free flip), Match (drag name to function), Quiz (scenario → identify neurotransmitter). In Quiz mode, 10 randomized scenarios drawn from a JSON array. Score displayed at end with "Try Again" option. Color-code cards by category: monoamines (Dopamine, Serotonin, Norepinephrine) in warm orange; amino acids (Glutamate, GABA) in blue; neuropeptides (Endorphins, Substance P) in green; cholinergic (Acetylcholine) in purple.*

*File location when built: `docs/sims/neurotransmitter-explorer/`*
*Iframe height when embedded: 600px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/neurotransmitter-explorer/main.html"
        width="100%" height="600" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

!!! mascot-warning
    <img src="../../img/mascot/warning.png" alt="Psy the Owl with a warning" style="float:right;width:100px;margin:0 0 1em 1em;">
    **Common AP exam mistake: "Dopamine = happiness"**

    Students often write that dopamine *causes* happiness or pleasure. Research is more precise: dopamine drives *wanting and seeking* — anticipation and motivation — not the experience of pleasure itself. Pleasurable feelings involve multiple systems including opioid and serotonin pathways. On free-response questions, saying dopamine mediates "reward-seeking behavior" or "motivation" is more accurate and earns more credit than saying it "makes you happy."

---

## 3.4 Hormones and Behavior

The nervous system does not act alone. The **endocrine system** — a network of glands that secrete chemical messengers called **hormones** into the bloodstream — profoundly influences behavior, mood, motivation, and physiology. Unlike neurotransmitters, which act within milliseconds at a synapse, **hormones and behavior** are linked through slower but longer-lasting chemical signals that travel system-wide.

The AP curriculum highlights five hormones with direct behavioral relevance. Each is secreted by a different gland and targets different behaviors.

### Adrenaline (Epinephrine)

**Adrenaline** (the common name) and **epinephrine** (the pharmacological name) refer to the same molecule — secreted by the adrenal medulla (the inner part of the adrenal glands, which sit atop the kidneys) in response to stress, danger, or intense exercise. Adrenaline prepares the body for fight-or-flight: it accelerates heart rate, increases blood pressure, dilates airways, mobilizes blood sugar, and sharpens alertness. It also functions as a neurotransmitter in the brain (where it is called norepinephrine/noradrenaline, its chemical precursor). Because the adrenal glands are part of the endocrine system, adrenaline effects persist for minutes — longer than a single nerve signal — which is why the physical sensations of fear (racing heart, sweaty palms) linger after a sudden scare has passed.

### Leptin and Ghrelin: The Hunger Hormones

**Leptin** and **ghrelin** are complementary hormones that regulate hunger and body weight. **Leptin** is secreted by fat (adipose) tissue and signals the hypothalamus that the body has sufficient energy stores — it suppresses appetite and promotes energy expenditure. Higher body fat generally means higher leptin levels. However, in obesity, the hypothalamus can become **leptin resistant**, failing to respond normally to the hormone's satiety signal. **Ghrelin** is secreted primarily by the stomach when it is empty and acts as a hunger trigger. Ghrelin levels rise before meals and fall after eating. Interestingly, ghrelin also rises in response to sleep deprivation, which helps explain why people tend to eat more when they are sleep-deprived.

### Melatonin

**Melatonin** is a hormone secreted by the pineal gland (a pea-sized structure deep in the brain) in response to darkness. It signals the body to prepare for sleep, acting as a chemical clock that synchronizes the sleep-wake cycle. Melatonin levels rise in the evening, peak in the middle of the night, and fall by morning in response to light exposure. Blue-spectrum light (from screens and LEDs) suppresses melatonin secretion most effectively, which is why screen use before bedtime delays sleep onset. Melatonin's role in **circadian rhythms** is discussed in depth in Section 3.7.

### Oxytocin

**Oxytocin** is often called the "bonding hormone" or "love hormone" because of its role in social attachment, trust, and affiliation. It is released from the posterior pituitary gland during physical touch, childbirth, breastfeeding, and positive social interactions. Oxytocin strengthens pair bonds in monogamous species, promotes maternal behavior, and reduces anxiety. Research has also linked oxytocin to in-group favoritism — it promotes trust within groups while potentially amplifying distrust of out-group members. This nuanced finding cautions against oversimplifying oxytocin as purely a "love" chemical.

#### Diagram: Hormones and Behavior Matching Activity

<details markdown="1">
<summary>Interactive: Hormones and Behavior Matching MicroSim</summary>

This interactive activity presents the five AP hormones alongside their source glands and behavioral effects. Use the matching game to connect each hormone with its gland of origin, primary behavior it influences, and what happens when levels are abnormally high or low. A body-map panel lets you click on gland locations to reveal which hormones are secreted there.

**Specification for MicroSim: Hormones and Behavior Matcher**

*Build as a two-panel p5.js activity. Left panel: a simple body silhouette with clickable hotspots on: (1) adrenal glands — epinephrine, (2) stomach — ghrelin, (3) adipose tissue — leptin, (4) pineal gland — melatonin, (5) pituitary gland — oxytocin. Clicking a hotspot highlights it and populates the right panel with: hormone name, gland, trigger condition, behavioral effect, and a "too high / too low" summary. Below the body map, a matching activity presents 10 drag-and-drop pairs: hormone → behavioral effect. Shuffle button randomizes order. Score shown at end with retry option.*

*File location when built: `docs/sims/hormones-behavior-matcher/`*
*Iframe height when embedded: 620px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/hormones-behavior-matcher/main.html"
        width="100%" height="620" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

---

## 3.5 Psychoactive Drugs: Mechanisms of Action

**Psychoactive drugs** are substances that cross the blood-brain barrier and alter perception, mood, consciousness, cognition, or behavior by modifying neurotransmitter activity. Understanding how drugs work requires three key concepts: agonists, antagonists, and reuptake inhibitors.

An **agonist** is a drug (or other substance) that mimics or enhances the effects of a neurotransmitter by binding to its receptor and activating it. Morphine is a dopamine and opioid receptor agonist; nicotine is an acetylcholine receptor agonist. An **antagonist** blocks a receptor without activating it, effectively preventing the natural neurotransmitter from binding. Naloxone (Narcan), which reverses opioid overdoses, is an opioid receptor antagonist. Antipsychotic medications typically work as dopamine antagonists, reducing the dopamine overactivity associated with schizophrenia's positive symptoms.

**Reuptake inhibitors** work at the presynaptic terminal rather than at the receptor itself: they block the transporter protein that normally pulls the neurotransmitter back out of the synapse, leaving more of the chemical available to bind postsynaptic receptors. **Selective serotonin reuptake inhibitors (SSRIs)** like fluoxetine (Prozac) are the most prescribed antidepressants and work by this mechanism. Cocaine is a reuptake inhibitor for dopamine, serotonin, and norepinephrine — its euphoric effects result from flooding reward circuits with dopamine that cannot be removed.

### Categories of Psychoactive Drugs

Four broad categories of psychoactive drugs appear on the AP exam. The table below summarizes their mechanisms and examples before the interactive simulator lets you explore each in depth.

| Category | Primary Mechanism | Examples | Key Neurotransmitter Effects |
|---|---|---|---|
| **Stimulants** | Increase CNS activity | Cocaine, amphetamines, caffeine, nicotine | ↑ Dopamine, norepinephrine (cocaine: reuptake inhibition; amphetamines: force release + reuptake inhibition) |
| **Depressants** | Decrease CNS activity | Alcohol, benzodiazepines, barbiturates | ↑ GABA activity; ↓ glutamate activity |
| **Hallucinogens** | Distort sensory processing | LSD, psilocybin, mescaline, PCP, ketamine | Serotonin receptor agonism (LSD, psilocybin); glutamate receptor blockade (PCP, ketamine) |
| **Opioids** | Bind opioid receptors | Morphine, heroin, codeine, oxycodone | Mimic endorphins; ↑ dopamine (reward); ↓ pain signals via Substance P suppression |

**Stimulants** elevate mood, increase energy, suppress appetite, and heighten alertness by amplifying dopamine and norepinephrine signaling. Cocaine's euphoric rush comes from rapid dopamine accumulation in the nucleus accumbens; the crash that follows reflects dopamine depletion as the brain struggles to compensate. Amphetamines (including prescription ADHD medications at therapeutic doses) both block reuptake and actively push dopamine out of vesicles into the synapse.

**Depressants** slow CNS activity, producing relaxation, sedation, reduced anxiety, and at high doses, unconsciousness. Alcohol — the most widely used depressant — enhances GABA (the brain's main inhibitory signal) and suppresses glutamate (the main excitatory signal). This is why alcohol reduces inhibition, impairs coordination, and at toxic doses can stop breathing. Benzodiazepines (prescribed for anxiety and sleep) work by the same GABA-enhancing mechanism.

**Hallucinogens** alter perception and cognition in ways that can produce vivid sensory distortions, synesthesia (mixing of senses), and profound changes in the sense of self and reality. Classic hallucinogens like LSD and psilocybin are serotonin receptor agonists, particularly at the 5-HT2A receptor subtype found densely in the prefrontal cortex. Dissociative hallucinogens like PCP and ketamine work differently — they block NMDA glutamate receptors, disrupting normal information integration.

**Opioids** are among the most medically valuable and most addictive substance classes. They bind mu, kappa, and delta opioid receptors — the same receptors activated by the brain's own endorphins. The result is powerful analgesia, euphoria, slowed breathing, and reduced Substance P transmission (blunting pain signals). The euphoria comes from indirect dopamine release in the reward system. However, respiratory depression — slowed or stopped breathing — is the mechanism of opioid overdose death.

#### Diagram: Drug Mechanism Simulator

<details markdown="1">
<summary>Interactive: Drug Mechanism Explorer</summary>

This interactive simulator lets you "apply" different drugs to a virtual synapse and observe how each one changes neurotransmitter levels, receptor activation, and postsynaptic response in real time. Select a drug category, choose a specific drug, and watch an animated synapse show the agonist/antagonist/reuptake inhibitor effect with color-coded neurotransmitter molecules.

**Specification for MicroSim: Drug Mechanism Simulator**

*Build as a p5.js interactive synapse simulation. Left panel: animated synapse cross-section (same visual style as synaptic cleft infographic) with neurotransmitter molecules visible in vesicles and cleft. Right panel: drug selector with four category tabs (Stimulants, Depressants, Hallucinogens, Opioids) and a dropdown of specific drugs within each category. Selecting a drug triggers: (1) an animation showing the drug molecules (in red) arriving at the synapse, (2) a highlight of where they act (transporter, receptor, vesicle), (3) a real-time bar graph showing relative NT levels in the cleft, (4) a behavioral effects summary card. A "Baseline" button resets to normal synapse. Include a "What would a doctor use this for?" info card for each drug with clinical context. Color-code by mechanism: agonists = green, antagonists = red, reuptake inhibitors = orange.*

*File location when built: `docs/sims/drug-mechanism-simulator/`*
*Iframe height when embedded: 640px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/drug-mechanism-simulator/main.html"
        width="100%" height="640" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

!!! mascot-encouraging
    <img src="../../img/mascot/encouraging.png" alt="Psy the Owl encouraging you" style="float:right;width:100px;margin:0 0 1em 1em;">
    **This section gets personal for many students.**

    Psychoactive drugs, addiction, and withdrawal are topics that may feel close to home — perhaps because of your own experiences, or those of people you care about. That is completely normal. Psychology approaches these topics without judgment, as phenomena that can be understood scientifically. Understanding *why* addiction happens doesn't excuse it, but it does explain it — and explanation is the first step toward compassion and effective help.

    You've got this. *Let's think about that!* 🦉

---

## 3.6 Tolerance, Addiction, and Withdrawal

Repeated drug use does not produce the same effect indefinitely. The brain adapts — and those adaptations can trap people in a cycle that is genuinely difficult to escape.

**Drug tolerance** is the reduction in a drug's effect that occurs with repeated use, requiring progressively larger doses to achieve the same response. Tolerance develops because the brain compensates for the drug's presence: it may downregulate (reduce the number of) receptor sites, reduce neurotransmitter synthesis, or increase the rate of drug metabolism. Tolerance explains why a heroin user who has been clean for months and then relapses is at high risk of fatal overdose — their tolerance has declined during abstinence, but they may use the same dose they were accustomed to, which now overwhelms their system.

**Addiction** (clinically termed *substance use disorder*) is a chronic, relapsing condition characterized by compulsive drug seeking and use despite harmful consequences. The DSM-5 defines it by a cluster of criteria including loss of control over use, failed attempts to quit, continued use despite problems, and physical dependence. Addiction is not simply a matter of willpower. Prolonged drug exposure physically remodels the reward circuits of the brain — particularly the nucleus accumbens and prefrontal cortex — reducing the natural pleasurability of everyday activities and strengthening the motivational pull toward the drug. The prefrontal cortex, which governs impulse control and future planning, is specifically impaired, making the rational decision to stop considerably harder than it appears from the outside.

**Withdrawal symptoms** are the physical and psychological effects that emerge when a dependent person stops or dramatically reduces drug use. They occur because the brain, having adapted to the drug's presence, is now running on a calibration that was set *with* the drug. Without it, the system is thrown off balance in the opposite direction of the drug's effects. Opioid withdrawal produces intense muscle pain, nausea, sweating, and agitation — the rebound from pain suppression. Alcohol withdrawal (in severe dependent cases) can produce tremors, hallucinations, and life-threatening seizures — the rebound from GABA enhancement and glutamate suppression. Stimulant withdrawal produces profound fatigue, depression, and increased appetite. The severity and duration of withdrawal symptoms depends on the drug, the dose, the duration of use, and individual neurobiology.

The cycle of **tolerance → dependence → withdrawal** forms the neurobiological trap of addiction. Understanding this cycle does not minimize personal responsibility, but it does explain why willpower alone is rarely sufficient and why evidence-based treatments — including medications like methadone, naltrexone, and buprenorphine for opioid use disorder — are essential.

---

## 3.7 Circadian Rhythms

Your biology runs on a roughly 24-hour internal clock — a timing system so fundamental that it operates even in isolated cells and influences almost every physiological process in the body. **Circadian rhythms** (from the Latin *circa diem*, "about a day") are biological cycles of approximately 24 hours that regulate sleep-wake patterns, body temperature, cortisol secretion, digestion, immune function, and cell division.

The master clock is located in the **suprachiasmatic nucleus (SCN)**, a small pair of clusters in the hypothalamus that receive direct light input from the retinas via the retinohypothalamic tract. The SCN synchronizes the body's peripheral clocks — present in virtually every organ — to the external light-dark cycle through hormonal and neural signals.

**Melatonin** is the primary hormonal output of this system. As described in Section 3.4, the pineal gland begins secreting melatonin in the evening when the SCN signals darkness. Rising melatonin levels lower core body temperature and initiate physiological sleep preparation. Light — especially blue-spectrum light from digital screens, LED lighting, and fluorescent bulbs — suppresses melatonin secretion by signaling the SCN that it is still daytime. This is the neuroscientific explanation for why screen exposure in the hour before bedtime measurably delays sleep onset and reduces sleep quality.

**Circadian disruption** occurs when behavioral or environmental schedules conflict with the internal clock. Shift work, transatlantic jet lag, irregular sleep schedules, and excessive evening light exposure all disrupt circadian rhythms. Chronic circadian disruption is associated with increased risk of metabolic disorders, cardiovascular disease, mood disorders, and impaired immune function — evidence that the body's clocks do much more than regulate sleep.

For adolescents specifically, there is a well-documented biological shift in circadian phase during puberty: the clock shifts approximately 2 hours later, making it genuinely harder for teenagers to fall asleep before 11 p.m. and to wake before 8 a.m. This is not laziness — it is neurobiology. Research consistently shows that school start times aligned with adolescent chronobiology (i.e., later start times) improve academic performance, mental health, and even reduced car accident rates among teen drivers.

#### Diagram: Circadian Rhythm and Melatonin Across 24 Hours

<details markdown="1">
<summary>Interactive: Circadian Rhythm Visualizer</summary>

This interactive chart shows melatonin levels, core body temperature, alertness, and cortisol across a 24-hour day. Drag the "light/dark" slider to shift the light-dark cycle (simulating jet lag or shift work) and observe how each biological variable tracks — or fails to track — the new schedule. A teen mode toggle applies the adolescent phase delay. A screen-use toggle shows the suppressive effect of evening blue light on melatonin onset.

**Specification for MicroSim: Circadian Rhythm Visualizer**

*Build as a Chart.js or p5.js interactive plot. X-axis: 24-hour clock (0:00–24:00). Y-axis: relative level (0–100%). Four overlapping line curves, each toggleable via checkbox: Melatonin (indigo), Cortisol (orange), Core Body Temperature (red), Alertness (green). Default: standard adult cycle. Controls: (1) "Light-Dark Cycle Offset" slider: drag to simulate jet lag (shifts all curves ±6 hours). (2) "Teen Phase Delay" toggle: shifts melatonin and alertness curves 2 hours later. (3) "Evening Screen Use" toggle: delays melatonin onset by 1 hour and reduces its peak by 30%. Tooltip on hover shows exact values. A colored time-of-day band along the x-axis shows wake (light yellow) and sleep (dark blue) periods. Include a "Reset to default" button.*

*File location when built: `docs/sims/circadian-rhythm-visualizer/`*
*Iframe height when embedded: 520px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/circadian-rhythm-visualizer/main.html"
        width="100%" height="520" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

!!! mascot-celebration
    <img src="../../img/mascot/celebration.png" alt="Psy the Owl celebrating" style="float:right;width:120px;margin:0 0 1em 1em;">
    **You made it through one of the most concept-dense chapters in AP Psychology — excellent work!**

    You now speak the language of the nervous system: from the quiet −70 mV resting potential all the way to the global effects of hormones and the neurobiological trap of addiction. That is a remarkable amount of territory.

    Here is the big picture to carry forward: **behavior is chemistry, but chemistry is not destiny.** Neurotransmitters and hormones create powerful biological tendencies, and drugs can hijack those systems — but the prefrontal cortex, which this chapter showed is essential for resisting those pulls, is also the seat of the deliberate choices you make every day.

    Before the exam, make sure you can: (1) draw and label an action potential curve, (2) name the function of all 8 neurotransmitters and 5 hormones, (3) explain agonist vs. antagonist vs. reuptake inhibitor with drug examples, and (4) connect melatonin to circadian rhythm disruption.

    *Let's think about that!* 🦉
