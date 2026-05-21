---
title: "Chapter 6: Memory: Encoding, Storage, and Models"
description: "A comprehensive exploration of how the human mind encodes, stores, and organizes information — covering the multi-store model, working memory, levels of processing, long-term potentiation, and proven encoding strategies including mnemonics, chunking, spacing, and the serial position effect."
generated_by: "claude skill chapter-content-generator"
date: 2026-05-21
version: 0.08
---

# Chapter 6: Memory: Encoding, Storage, and Models

## Summary

This chapter introduces the major models and systems of human memory.
Students compare the multi-store model (sensory → short-term → long-term)
with the working memory model and levels-of-processing framework. The chapter
covers how information is encoded through elaborative rehearsal, chunking,
mnemonic devices, and spacing, and distinguishes explicit from implicit memory
and episodic from semantic memory. Long-term potentiation is introduced as the
biological mechanism of memory consolidation.

## Concepts Covered

This chapter covers the following 18 concepts from the learning graph:

1. Explicit Memory
2. Implicit Memory
3. Multi-Store Memory Model
4. Episodic Memory
5. Semantic Memory
6. Prospective Memory
7. Procedural Memory
8. Sensory Memory
9. Levels of Processing
10. Short-Term Memory
11. Encoding Strategies
12. Long-Term Potentiation
13. Working Memory Model
14. Long-Term Memory
15. Mnemonic Devices
16. Chunking
17. Spacing Effect
18. Serial Position Effect

## Prerequisites

This chapter builds on concepts from:

- [Chapter 2: Biological Bases of Behavior: Neurons and the Brain](../02-biological-bases-behavior/index.md)
- [Chapter 5: Cognition and Thinking](../05-cognition-thinking/index.md)

---

## 6.1 Types of Memory: A Map of the System

!!! mascot-welcome
    <img src="../../img/mascot/welcome.png" alt="Psy the Owl welcoming you to Chapter 6" class="mascot-admonition-img">
    **Welcome to Chapter 6 — where we explore the architecture of memory!**

    Have you ever forgotten where you put your phone ten seconds after setting it down, yet still remember every word to a song you haven't heard in five years? Memory is not a single thing — it is a collection of interacting systems, each specialized for different kinds of information. Some memories are conscious and deliberate; others operate invisibly, guiding your hands on a keyboard or your feet on a bicycle without any effort at all.

    In this chapter you will discover *why* memories are formed, *how* they are stored, and — most usefully — *what strategies actually work* to make them stick. Everything here has direct applications to studying for the AP exam and every other exam you will ever take.

    *Let's think about that!* 🦉

Memory is not a single mental filing cabinet. Psychologists organize memory into distinct systems based on what kind of information is stored and how conscious access to that information is. The broadest and most important distinction is between **explicit memory** and **implicit memory**.

**Explicit memory** (also called *declarative memory*) refers to memories that can be consciously retrieved and described in words. When you recall what you had for breakfast, recite the definition of a psychology term, or remember that you need to pick up a friend from the airport tomorrow, you are using explicit memory. Explicit memory requires conscious, deliberate effort to retrieve.

**Implicit memory** refers to memories that influence behavior without conscious awareness. When you ride a bike, type on a keyboard, or feel a vague sense of familiarity about a melody you cannot name, implicit memory is at work. Implicit memories are revealed through performance rather than verbal report — you show that you remember rather than telling that you remember.

### Subtypes of Explicit Memory

Within explicit memory, psychologists distinguish three important subtypes. **Episodic memory** stores personally experienced events — specific episodes from your life anchored to a time and place. Remembering your first day of high school, the last birthday party you attended, or what you did last Saturday morning are all episodic memories. Episodic memory is sometimes called "mental time travel" because retrieving an episodic memory involves mentally re-experiencing the original event.

**Semantic memory** stores general knowledge about the world that is not tied to a specific personal experience. Knowing that Paris is the capital of France, that photosynthesis converts sunlight into glucose, or that "ubiquitous" means "found everywhere" are semantic memories. You know these facts, but you probably do not remember *when* you first learned them.

**Prospective memory** is the memory for *future intentions* — remembering to do something at a particular time or in a particular context. Remembering to take your medication at noon, to call your grandmother on her birthday, or to mention something to your teacher after class are all prospective memory tasks. Prospective memory failures ("I forgot to do it!") are among the most common everyday memory complaints.

### Subtypes of Implicit Memory

**Procedural memory** is the dominant form of implicit memory: it stores motor skills and habitual action sequences. Procedural memories are built through repetition and practice and are expressed through smooth, automatic performance. Once a motor skill is proceduralized — tying shoelaces, playing piano scales, touch-typing — you can execute it while your conscious attention is elsewhere. Interestingly, *thinking too hard* about a well-practiced skill can actually disrupt it (called **choking** or the "paralysis by analysis" effect), because conscious attention interferes with the automatic processing that procedural memory uses.

The table below summarizes all five memory types covered in this chapter:

| Memory Type | Conscious? | Examples | AP Exam Keyword |
|---|---|---|---|
| Episodic | Yes | First day of school, last vacation | "Personal experience," "time and place" |
| Semantic | Yes | Capital cities, vocabulary, facts | "General knowledge," "no context" |
| Prospective | Yes | Remember to buy milk, call a friend | "Future intention," "remembering to remember" |
| Procedural | No | Riding a bike, typing, swimming | "Motor skill," "habit," "automatic" |
| Priming / Other Implicit | No | Feeling of familiarity, conditioned responses | "Unconscious influence," "revealed by performance" |

#### Diagram: Memory Types Overview

<details markdown="1">
<summary>Interactive: Memory Type Sorter</summary>

This interactive activity presents a series of 12 memory scenarios and asks you to classify each into the correct memory type (episodic, semantic, prospective, or procedural). Scenarios are presented one at a time on a card. Four labeled bins are shown below: drag the card to the correct bin or click the bin label. Immediate feedback explains why the answer is correct or incorrect, with a brief definition of the relevant memory type. A progress bar tracks your score across all 12 scenarios. After completing the set, a summary pie chart shows your accuracy by memory type — revealing which types you find most confusing.

**Specification for MicroSim: Memory Type Sorter**

*Build as a p5.js simulation. Show a scenario card (white rounded rectangle, 400 × 180 px) near the top of the canvas. Below, render four labeled bins as colored rectangles (episodic = blue, semantic = green, prospective = orange, procedural = purple). On click of a bin label, animate the card flying to that bin. Show a green checkmark and brief explanation text for correct answers; a red X and corrective explanation for incorrect answers. After 1.5 s, advance to the next card. Track score (correct / total) in top-right corner. After all 12 cards, show a donut chart (using p5.js arc calls) breaking down accuracy by category. Include a "Retry" button.*

*File location when built: `docs/sims/memory-type-sorter/`*
*Iframe height when embedded: 520px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/memory-type-sorter/main.html"
        width="100%" height="520" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

---

## 6.2 The Multi-Store Memory Model (Atkinson-Shiffrin)

The first influential scientific model of human memory was proposed by Richard Atkinson and Richard Shiffrin in 1968. Their **Multi-Store Memory Model** (sometimes called the Modal Model) describes memory as a sequence of three distinct stores — **sensory memory**, **short-term memory**, and **long-term memory** — through which information flows in stages. Each store differs in its capacity, duration, and the form in which information is encoded.

### Sensory Memory

**Sensory memory** is the first and most fleeting stage. It holds a nearly complete snapshot of sensory experience for a very brief period — less than half a second for visual information (called *iconic memory*) and about 3–4 seconds for auditory information (called *echoic memory*). Sensory memory acts as a buffer: it holds a rich perceptual record long enough for selective attention to extract the most relevant information and pass it forward. Everything else decays immediately without further processing. George Sperling's classic 1960 experiments demonstrated that iconic memory holds far more information than people can report — participants could recall any *row* of a briefly flashed letter grid when cued immediately, showing that the full grid was briefly available even though the whole could not be reported before decay.

### Short-Term Memory

Information that captures attention moves from sensory memory into **short-term memory** (STM). Short-term memory holds a small amount of information in an active, immediately accessible state for roughly 15–30 seconds without rehearsal. George Miller's famous 1956 paper ("The Magical Number Seven, Plus or Minus Two") showed that the capacity of short-term memory is approximately **7 ± 2 items** (chunks). Without active rehearsal, items fade through a process called **decay**; they can also be lost through **displacement** when new incoming items push out old ones.

**Maintenance rehearsal** — the silent or vocal repetition of information — can keep items active in STM indefinitely, but it does not reliably move information into long-term memory. **Elaborative rehearsal** — connecting new information to existing knowledge, thinking about its meaning — is far more effective for long-term retention (a point we will return to in Section 6.4).

### Long-Term Memory

Information that is sufficiently processed moves into **long-term memory** (LTM). Long-term memory has a virtually unlimited capacity and can store information for a lifetime. Unlike the other stores, LTM is thought to be permanent in principle; what we call "forgetting" typically reflects failures of *retrieval* rather than erasure of the stored trace (this is explored in Chapter 7). LTM encompasses all of the explicit and implicit memory subtypes described in Section 6.1.

The flow of information through the three stores — and the control processes (attention, rehearsal, encoding) that govern how much moves between them — is the essence of the Atkinson-Shiffrin model. The model remains one of the most tested frameworks on the AP Psychology exam.

#### Diagram: Multi-Store Memory Model (Atkinson-Shiffrin)

<details markdown="1">
<summary>Interactive: Atkinson-Shiffrin Memory Flow Diagram</summary>

This interactive diagram animates the flow of information through the three memory stores of the Atkinson-Shiffrin model. A horizontal pathway shows Sensory Memory → Short-Term Memory → Long-Term Memory as labeled nodes connected by directed arrows. A "decay" arrow drops down from both Sensory Memory and Short-Term Memory. A "rehearsal loop" curves back from STM to itself. Click any node to expand a pop-up panel showing its capacity, duration, and encoding type. Click any arrow to display the process it represents (attention, elaborative rehearsal, retrieval). A "Run Simulation" button animates a stream of colored information tokens flowing through the pathway: most tokens fall off at sensory memory (decay), a few pass into STM, and only tokens that reach the rehearsal loop eventually make it to LTM. A slider adjusts rehearsal frequency to show how it affects how many tokens reach LTM.

**Specification for MicroSim: Atkinson-Shiffrin Flow Diagram**

*Build as a p5.js simulation. Draw three rounded rectangles (nodes) in a horizontal row: "Sensory Memory" (gray), "Short-Term Memory" (blue), "Long-Term Memory" (green). Connect with right-pointing arrows. Add a downward "Decay" arrow from Sensory Memory and from STM. Add a curved "Rehearsal" arrow looping above STM back to itself. Each node is clickable: clicking opens an overlay card (semi-transparent dark rectangle) showing capacity, duration, and encoding format. A "Simulate" button spawns 20 small circular tokens that animate along the pathway. At each junction, a random subset (weighted by a slider value) continues; the rest deflect down the decay arrow and fade. Tokens that complete the rehearsal loop N times (set by a second slider) proceed to LTM and turn gold. Show a live "Encoded to LTM" counter in the corner. Include a "Reset" button.*

*File location when built: `docs/sims/multi-store-memory-model/`*
*Iframe height when embedded: 540px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/multi-store-memory-model/main.html"
        width="100%" height="540" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

!!! tip
    <img src="../../img/mascot/tip.png" alt="Psy the Owl with a tip" class="mascot-admonition-img">
    **AP Exam shorthand for the three stores:**

    - **Sensory Memory** → huge capacity, tiny duration (< 1 s visual, ~4 s auditory)
    - **Short-Term Memory** → 7 ± 2 chunks, ~15–30 s without rehearsal
    - **Long-Term Memory** → unlimited capacity, potentially permanent

    A common AP multiple-choice trap: the question describes someone repeating a phone number over and over but forgetting it the moment they dial. This is **maintenance rehearsal keeping information in STM** — it does NOT transfer to LTM. *Let's think about that!* 🦉

---

## 6.3 The Working Memory Model (Baddeley and Hitch)

The Atkinson-Shiffrin model treated short-term memory as a single passive storage buffer. In 1974, Alan Baddeley and Graham Hitch proposed a richer replacement: the **Working Memory Model**. Rather than a simple holding pen, working memory is a dynamic, multi-component system that actively manipulates information while using it — the "mental workspace" where thinking, reasoning, comprehension, and problem-solving actually happen.

The Baddeley-Hitch model has four components.

The **central executive** is the most important component. It is an attentional control system — not a storage device itself but the director that allocates attention, coordinates the other components, switches between tasks, and links working memory to long-term memory. The central executive is associated with the prefrontal cortex. When you are solving a math problem in your head while simultaneously remembering the intermediate steps, your central executive is orchestrating both processes.

The **phonological loop** handles verbal and auditory information. It consists of two parts: a *phonological store* (a brief verbal trace that fades in about 2 seconds) and an *articulatory rehearsal process* (the "inner voice" that refreshes the trace by silently repeating it). The phonological loop is why you can hold a phone number in mind by repeating it mentally. It is also central to language comprehension: as you read a sentence, the phonological loop holds earlier words active while you process later ones.

The **visuospatial sketchpad** handles visual and spatial information — the "inner eye." It is responsible for maintaining and manipulating mental images, navigating space, and tracking the positions of objects. Architects mentally rotating floor plans, chess players visualizing future board positions, and you imagining the layout of your bedroom are all using the visuospatial sketchpad.

The **episodic buffer** (added by Baddeley in 2000) is a limited-capacity temporary store that integrates information from the phonological loop, the visuospatial sketchpad, and long-term memory into coherent, multi-dimensional episodes. It is the "glue" that binds verbal, visual, and stored knowledge into a unified experience. The episodic buffer explains why you can combine a melody (phonological loop), a mental image of a concert venue (visuospatial sketchpad), and autobiographical memories (LTM) into a single rich recollection.

The table below compares the components of working memory:

| Component | Type of Information | Storage? | Key Function |
|---|---|---|---|
| Central Executive | Attentional control | No | Directs attention; coordinates other components |
| Phonological Loop | Verbal / auditory | Yes (~2 s) | Inner voice; language comprehension |
| Visuospatial Sketchpad | Visual / spatial | Yes | Mental imagery; spatial navigation |
| Episodic Buffer | Multimodal | Yes (limited) | Integrates information from all sources |

#### Diagram: Working Memory Model (Baddeley)

<details markdown="1">
<summary>Interactive: Working Memory Model Explorer</summary>

This interactive diagram lets you explore each component of Baddeley's working memory model and see how they interact. The canvas shows the four components as labeled shapes: the central executive as a large central circle, flanked by the phonological loop (left), the visuospatial sketchpad (right), and the episodic buffer (bottom). Bidirectional arrows connect the central executive to each component; a downward arrow connects the episodic buffer to a Long-Term Memory node below. Clicking any component highlights it and opens a sidebar panel with its name, function, capacity, duration, and a real-world example. A "Task Simulator" lets you select a cognitive task (e.g., "Mental arithmetic," "Reading a novel," "Navigating a new city") and animates which components are active — highlighted in color — during that task, with a brief explanation of why each component is engaged.

**Specification for MicroSim: Working Memory Model Explorer**

*Build as a p5.js simulation. Draw a large circle (central executive, yellow) in the center of the canvas. Draw three satellite shapes: phonological loop (blue rounded rectangle, left), visuospatial sketchpad (purple rounded rectangle, right), episodic buffer (green rounded rectangle, bottom). Draw a Long-Term Memory node (gray rectangle) below the episodic buffer. Connect all satellites to the central executive with bi-directional arrows; connect the episodic buffer to LTM with a bi-directional arrow. On hover, each component brightens. On click, render an info panel on the right side of the canvas (semi-transparent dark background, white text) with: Name, Function (2–3 sentences), Capacity/Duration, Example. Below the diagram, add a dropdown menu: "Select a cognitive task" with 5 options. On selection, animate the relevant components with a pulsing glow and display explanation text in the info panel. Include a "Clear" button.*

*File location when built: `docs/sims/working-memory-model/`*
*Iframe height when embedded: 560px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/working-memory-model/main.html"
        width="100%" height="560" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

---

## 6.4 Levels of Processing and the Biology of Memory

### Levels of Processing (Craik and Lockhart)

In 1972, Fergus Craik and Robert Lockhart proposed a fundamentally different way of thinking about memory formation. Rather than emphasizing which *store* information enters, they argued that what matters most is the *depth* at which information is processed — the **Levels of Processing** framework.

**Shallow processing** involves analyzing the surface features of a stimulus: its physical appearance, sound, or visual form. Reading a word and noting whether it is printed in capital letters is shallow (structural) processing. Deciding whether a word rhymes with another is slightly deeper (phonemic) processing. Both leave relatively weak, easily forgotten memory traces.

**Deep processing** — specifically, **semantic processing** — involves analyzing the *meaning* of information: relating it to what you already know, generating examples, asking how it connects to your own experience, or evaluating whether it makes sense. Deeply processed information produces a richer, more durable memory trace because it is integrated into the existing network of knowledge in long-term memory. This is the mechanism behind **elaborative rehearsal**: when you connect a new term to a concept you already understand, you are processing at a deep level.

The **self-reference effect** extends this principle: information processed in terms of its relevance to *yourself* is remembered especially well. If you ask "Does this word describe me?" rather than "Does this word mean something positive?", recall later is significantly better. The self is a richly organized schema in long-term memory, and anchoring new information to it creates multiple retrieval pathways.

### Long-Term Potentiation: The Biology of Memory

Every psychological account of memory has a biological underpinning. The leading biological mechanism for how memories are formed at the synaptic level is called **long-term potentiation (LTP)**. LTP is a persistent strengthening of a synapse — the connection between two neurons — that results from repeated, high-frequency stimulation. When neurons "fire together, wire together" (a principle articulated by Donald Hebb and now called **Hebb's rule**), the synapse between them becomes more efficient: the postsynaptic neuron becomes more responsive to future input from the same presynaptic neuron.

LTP was first demonstrated in the hippocampus, a brain structure critically important for consolidating new explicit memories. Glutamate receptors called **NMDA receptors** act as coincidence detectors: they only activate when the presynaptic neuron fires *and* the postsynaptic neuron is already partially depolarized — meaning LTP is a learning rule that strengthens connections only when two neurons are simultaneously active. Over repeated activation, LTP triggers molecular changes — including growth of new dendritic spines and synthesis of new proteins — that make the synaptic connection more efficient and durable. This synaptic-level change is the physical substrate of a memory trace, called an **engram**.

Understanding LTP explains several important memory phenomena: why spaced practice is more effective than massed practice (each spaced trial re-activates the synapse from a rested state, triggering stronger LTP), why sleep aids memory consolidation (hippocampal "replay" during slow-wave sleep appears to consolidate LTP-dependent memories), and why stress hormones can both enhance (for emotionally significant events) and impair (for chronic stress) memory formation.

!!! note
    <img src="../../img/mascot/thinking.png" alt="Psy the Owl thinking" class="mascot-admonition-img">
    **Connecting biology to behavior:**

    Long-term potentiation is the biological mechanism that explains *why* deep processing works. When you process information semantically, you activate a broader network of existing synapses alongside the new material. The co-activation of many synapses at once is precisely the condition that triggers LTP most strongly — so the "why" of the levels-of-processing effect turns out to be a story about synaptic coincidence detection.

    *Let's think about that!* 🦉

---

## 6.5 Encoding Strategies: Making Memories Stick

Knowing that deep processing and repeated activation strengthen memories leads directly to practical **encoding strategies** — deliberate techniques for improving how well information is encoded. This section covers four of the most important and AP-relevant strategies: mnemonic devices, chunking, the spacing effect, and the serial position effect.

### Mnemonic Devices

**Mnemonic devices** are systematic encoding strategies that use structured associations to make information more memorable. The word "mnemonic" comes from Mnemosyne, the Greek goddess of memory. Mnemonics work by linking difficult-to-remember material to something that is already easy to recall — a rhyme, a vivid image, a narrative, or an organized structure.

Common types of mnemonic devices include:

- **Acronyms**: Using the first letter of each item to form a memorable word or phrase. ROYGBIV encodes the colors of the visible spectrum (Red, Orange, Yellow, Green, Blue, Indigo, Violet).
- **Method of loci** (memory palace): Mentally placing items to be remembered at distinct locations along a familiar route (e.g., your walk to school). Retrieval involves mentally "walking" the route and "seeing" each item. This technique, used by ancient Greek orators, exploits the brain's powerful spatial memory systems and is one of the most effective mnemonic strategies ever studied.
- **Peg-word system**: Associating numbers with rhyming words ("one is a bun, two is a shoe...") and then forming vivid images linking each peg word to the item to be remembered.
- **Rhymes and songs**: Embedding information in a rhythmic or melodic structure (e.g., the ABC song, "Thirty days hath September").
- **Keyword method**: Creating a sound-alike word (the "keyword") that links the sound of a foreign word to an image of its meaning. To remember that the Spanish word *pato* means "duck," imagine a duck being poked with a *pat* on the head.

Mnemonic devices are particularly effective for memorizing lists, sequences, and vocabulary. They work by creating multiple retrieval cues — the structured association provides an additional pathway to the target information beyond its bare content.

### Chunking

**Chunking** is the process of grouping individual items of information into larger, meaningful units — "chunks" — that can be held in short-term memory as single items. Because short-term memory holds roughly 7 ± 2 *chunks* (not 7 ± 2 individual items), chunking dramatically increases the effective capacity of working memory.

The classic example is a phone number. The string 1-7-0-3-5-5-5-1-2-3-4 is 11 individual digits — well beyond the 7 ± 2 limit. But grouping it as 1 (703) 555-1234 reduces it to three chunks (country code, area code, local number), making it easily manageable. Expert chess players chunk board positions into meaningful patterns — not individual piece locations but recognized formations — which is why they can reconstruct a mid-game board from memory far better than novices.

Chunking also explains why prior knowledge improves memory. When you already know a domain well, new information in that domain is rich with meaningful patterns that can be chunked with existing knowledge — greatly increasing how much you can hold in working memory and how readily new material is encoded into long-term memory.

### The Spacing Effect

The **spacing effect** (also called the *distributed practice* effect) is one of the most robust and well-replicated findings in all of cognitive psychology: information learned in multiple, spaced study sessions is retained far better than the same total amount of study time concentrated in a single session (**massed practice** or "cramming").

Distributed practice outperforms massed practice for several reasons. Spaced repetitions allow initial forgetting to occur, and the *effort* of retrieving weakened memories actually strengthens them more than re-encoding already-active memories (a related principle called the **testing effect** or retrieval practice effect). Each spaced session also re-activates and extends LTP at the relevant synapses from a fully rested state, producing stronger potentiation than repeated activation in rapid succession. Finally, spaced study creates memories with *more varied context cues* — different times, mental states, and environmental details — providing more retrieval pathways.

The practical implication is unambiguous: start studying early, study in shorter sessions spread across days or weeks, and test yourself between sessions. Cramming may support performance on an exam the next morning but produces rapid forgetting afterward.

### The Serial Position Effect

The **serial position effect** refers to the finding that when people study and then recall a list of items, they tend to remember items from the *beginning* and *end* of the list better than items from the *middle*. This produces a characteristic U-shaped curve when recall accuracy is plotted against list position.

The enhanced recall of early items is called the **primacy effect**: early items receive more rehearsal (they have been repeated while subsequent items are processed), allowing them to be transferred to long-term memory. The enhanced recall of recent items is called the **recency effect**: items at the end of the list are still in short-term (working) memory at the time of recall and can be reported before they decay.

The middle of the list suffers from both ends: early enough that working memory has cleared by recall time, but late enough that the items received less rehearsal than the early ones. The serial position curve has important implications for how information is presented in learning (put the most critical content at the beginning or end, not the middle) and for understanding how memory systems interact.

#### Diagram: Encoding Strategies MicroSim

<details markdown="1">
<summary>Interactive: Encoding Strategies Lab</summary>

This interactive laboratory lets you experience and compare four encoding strategies: mnemonic devices, chunking, spacing, and the serial position effect. Four tabs are available at the top of the simulation.

**Mnemonics tab**: A list of 8 vocabulary terms and definitions is displayed. You choose a mnemonic strategy (acronym, keyword method, or method of loci) and apply it to the list. After a short distractor task (a 30-second counting activity), you are tested on recall. Your score is displayed alongside a comparison to rote repetition.

**Chunking tab**: A string of 12 random digits appears for 5 seconds. You attempt to recall it without chunking, then a new string appears and you are shown how to chunk it (e.g., into groups of 3–4). Your recall accuracy is compared across both conditions.

**Spacing tab**: A set of 10 flashcard-style facts is presented. You choose either a "Massed" schedule (all 10 reviewed three times in a row) or a "Spaced" schedule (all 10 reviewed, then a short delay, then reviewed again, then another delay, then reviewed again). A simulated quiz follows. A graph shows predicted long-term retention for each schedule.

**Serial Position tab**: A list of 12 words scrolls by one at a time (1 second each). After a 10-second distractor, you type all the words you remember. Your responses are scored by list position and plotted as a bar graph, revealing the U-shaped serial position curve. Labels for "Primacy Effect" and "Recency Effect" annotate the graph.

**Specification for MicroSim: Encoding Strategies Lab**

*Build as a p5.js simulation with four clickable tabs at top. Mnemonics tab: display 8 word-definition pairs. Three radio buttons select mnemonic type. A "Study" phase (30 s timer) is followed by a distractor (count down from 50 by 3s, displayed on screen). Then a recall phase: fill-in-the-blank text inputs. Score displayed as percentage. Chunking tab: generate random 12-digit string; show for 5 s; accept typed recall; score and show chunked version; repeat with chunked string; compare accuracy in a bar chart. Spacing tab: draw a 2 × N grid of "flashcards" (small rectangles). In massed mode, cycle through all cards 3 times back-to-back; in spaced mode, cycle once, then show a timer bar representing a "delay," then cycle again twice with delays. After final review, show a quiz (10 multiple-choice questions). Plot predicted retention at 1 day / 1 week / 1 month as a grouped bar chart for massed vs. spaced. Serial position tab: animate words appearing one at a time (1 s each, centered on canvas, large font). After 10-s countdown distractor, show 12 text input fields. Score each input vs. original position. Plot a bar chart of accuracy by position (1–12), with red zones labeled "Primacy" (positions 1–3) and "Recency" (positions 10–12).*

*File location when built: `docs/sims/encoding-strategies-lab/`*
*Iframe height when embedded: 600px*

*[MicroSim to be generated — embed once built:]*

```
<iframe src="../../sims/encoding-strategies-lab/main.html"
        width="100%" height="600" scrolling="no"
        style="border:none;border-radius:8px;">
</iframe>
```

</details>

---

## 6.6 Bringing It All Together: Memory as an Integrated System

The models and strategies covered in this chapter are not isolated facts — they describe a single integrated system. Sensory memory feeds short-term/working memory through selective attention. Working memory's central executive routes information to long-term memory through elaborative rehearsal and deep processing. The depth at which encoding occurs determines the richness of the resulting trace, and long-term potentiation provides the synaptic-level mechanism that physically instantiates that trace. Encoding strategies — chunking, mnemonics, distributed practice — are effective precisely because they engage these biological and cognitive mechanisms more powerfully than passive repetition.

Understanding this system also illuminates individual differences in memory. Expert performers in any domain (chess, music, medicine) do not have fundamentally different memory systems — they have built vastly richer knowledge structures in long-term memory that allow them to chunk aggressively, process deeply, and retrieve efficiently. This is encouraging news: memory performance is largely a skill that improves with the right strategies and deliberate practice.

The table below summarizes the key models and their core claims:

| Model / Framework | Proposed By | Core Claim | Key Variables |
|---|---|---|---|
| Multi-Store Model | Atkinson & Shiffrin (1968) | Three sequential stores | Rehearsal transfers info from STM to LTM |
| Working Memory Model | Baddeley & Hitch (1974) | STM is a multi-component active workspace | Central executive coordinates four components |
| Levels of Processing | Craik & Lockhart (1972) | Depth of processing determines retention | Semantic > phonemic > structural |
| Long-Term Potentiation | Bliss & Lømo (1973) | Repeated co-activation strengthens synapses | NMDA receptor, Hebb's rule, engram |

!!! mascot-celebrate
    <img src="../../img/mascot/celebration.png" alt="Psy the Owl celebrating" class="mascot-admonition-img">
    **Excellent work — you have built a complete model of memory!**

    You now understand memory not as one thing but as an intricate, multi-layered system: sensory buffers feeding a dynamic workspace, governed by attention and rehearsal, with deep encoding etching durable traces through synaptic strengthening. You know *why* spacing works, *why* mnemonics work, and *why* the middle of a list is a forgetting danger zone.

    Most importantly, every strategy in this chapter is something you can apply starting today — to this course and every other one. The science of memory is also the science of studying, and you now have the evidence-based toolkit.

    In Chapter 7 we turn to the darker side: forgetting, retrieval failures, interference, and the surprising malleability of memory. *Let's think about that!* 🦉

---

## Chapter Review

### Key Terms

- **Explicit memory** — Conscious, declarative memory; includes episodic, semantic, and prospective memory
- **Implicit memory** — Unconscious memory; includes procedural memory and priming
- **Episodic memory** — Memory for personally experienced events anchored in time and place
- **Semantic memory** — Memory for general world knowledge not tied to personal experience
- **Prospective memory** — Memory for future intentions ("remembering to remember")
- **Procedural memory** — Implicit memory for motor skills and habitual action sequences
- **Sensory memory** — Brief, high-capacity perceptual buffer (iconic < 0.5 s; echoic ~4 s)
- **Short-term memory** — Active, limited-capacity store (7 ± 2 chunks; ~15–30 s without rehearsal)
- **Long-Term Memory** — Unlimited-capacity, potentially permanent storage system
- **Multi-Store Memory Model** — Atkinson-Shiffrin three-stage model: sensory → STM → LTM
- **Working Memory Model** — Baddeley-Hitch active workspace with central executive, phonological loop, visuospatial sketchpad, and episodic buffer
- **Levels of Processing** — Craik & Lockhart framework; depth of processing (shallow to deep/semantic) determines retention strength
- **Long-Term Potentiation (LTP)** — Persistent synaptic strengthening following repeated co-activation; the biological basis of memory formation
- **Encoding Strategies** — Deliberate techniques for improving memory encoding
- **Mnemonic Devices** — Structured associations (acronyms, method of loci, keyword method) that improve recall
- **Chunking** — Grouping items into meaningful units to expand effective working memory capacity
- **Spacing Effect** — Distributed practice across time produces better long-term retention than massed (crammed) practice
- **Serial Position Effect** — U-shaped recall curve; primacy effect (early items) + recency effect (recent items)

### AP Exam Focus Points

The following distinctions are frequently tested on the AP Psychology exam:

- Explicit vs. implicit memory: conscious retrieval vs. performance-based expression
- Episodic vs. semantic memory: personal experience vs. general knowledge
- Maintenance rehearsal (keeps info in STM) vs. elaborative rehearsal (transfers to LTM)
- Shallow processing (structural/phonemic) vs. deep processing (semantic) — deep processing produces stronger retention
- Primacy effect (first items → LTM via rehearsal) vs. recency effect (last items → still in STM)
- Spacing effect: why distributed practice beats cramming for *long-term* retention
- LTP as the biological mechanism: "neurons that fire together, wire together" (Hebb's rule)
