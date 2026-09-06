---
type: Primer
---

# A primer on discourse graphs

The [CHI Papers Mission](missions/chi-papers.md) asks you to make a **map of the knowledge/design space** your papers are part of, using a simplified "discourse graph" — then to extend that map with your own ideas.

This page is the reference for *how*. We'll do a worked example together in class; come back here while you're building your own map.

---

## Part A — reading papers into nodes

When reading papers with a research mindset (i.e., with a mind towards contributing to new knowledge based on what is known or unknown about a problem or question of interest), it is can be useful to read and take notes on papers in terms of atomic **nodes** of knowledge (e.g., a question, a claim, an empirical result, a new design pattern) and connect them into a map of a scholarly conversation around a question or topic. This lets you see what is well-trodden or uncertain, what is unknown or left to do that is interesting, and spark new ideas for future attempts to advance collective knowledge on the question/topic (aka Research! :)).

I have found the following types of atomic knowledge nodes to be quite useful in my own research in HCI (which often clusters into empirical and design/constructive problems, in [Oulasvirta and Hornbæk's](https://dl.acm.org/doi/10.1145/2858036.2858283) language):

Broadly, I take aim at one or more research **questions**, which can be informed/answered by empirical **claims** that are supported or opposed by empirical observational **evidence**, or new design **patterns** that are instantiated in or exemplified by concrete design **artifacts** that can be evaluated.

![The five node types, drawn as two groups. Claim over Evidence is a body of evidence, the empirical contributions; Pattern over Artifact is a design space, the design and system contributions. Both groups point up at a Research Question, and both are contained in or produced by published papers or our own project.](assets/discourse-graph-node-types.png)

Let's consider each node type in more detail.
### QUE — Question

Research questions are unknowns that we want to make known, and are addressable by our experiments, prototypes, etc.

This is usually something general enough that it takes multiple experiments and results to address.

**Examples:**

- *How might we support users in recontextualizing key insights from past brainstorming meetings to support future synthesis work?*
- *Can language models assist with analogical problem reformulation?*
- *Compared to human experts, how accurately and efficiently can LLMs evaluate research reports?*
- *How might we augment scholarly sensemaking by making the full range of scholarly information more senseable?*

Questions are often useful as overall landmarks that structure an area of investigation, and other node types, like claims, or design patterns, often point at (address) questions.

### CLM — Claim

Claims are **atomic, generalized assertions** about the world that (propose to) answer research questions.

Concepts are described at a higher level of abstraction that is closer to a generalization — e.g., prefer the construct to the operationalization or observable:

| Prefer this (construct) | over this                                       |
| ----------------------- | ----------------------------------------------- |
| social media            | Facebook (operationalization)                   |
| polarization            | self-reported ideological distance (observable) |

Often these cut across papers and studies.

!!! tip "The AIDA test"

    The **AIDA scheme** from [this paper on nanopublications](https://arxiv.org/pdf/1303.2446.pdf) is a pretty good set of principles for how we try to write CLM nodes:

    - **Atomic**: a sentence describing one thought that cannot be further broken down in a practical way
    - **Independent**: a sentence that can stand on its own, without external references like "this effect" or "we"
    - **Declarative**: a complete sentence ending with a full stop that could in theory be either true or false
    - **Absolute**: a sentence describing the core of a claim ignoring the (un)certainty about its truth and ignoring how it was discovered (no "probably" or "evaluation showed that"); typically in present tense


**Example:** *Transformer language models have some analogical reasoning ability.*

### EVD — Evidence

Evidence is a **specific empirical observation from a particular study**. Claims are supported or opposed by evidence.

EVD nodes, like CLM nodes, should be **atomic** — they should describe, as far as possible, a single observation vs. a set of results.

EVD descriptions are written in the **past tense**. This convention reminds us that these are contingent observations!

EVD descriptions are **strictly contextualized**:

- **Low level.** Concepts are described at a lower level of abstraction that is **closer to the actual observation** — more at the level of operationalizations and measures compared to constructs. This is the same ladder as above, run in the opposite direction: *Facebook* rather than *social media*, *self-reported ideological distance* rather than *polarization*. Include screenshots of the specific figures/tables, as well as textual descriptions that report the result(s).
- **Methodology context.** Key methodological details are described, sufficient to understand the result and appraise its support/opposition for various claims. At minimum: **the observable** (aka *what* data was actually collected and analyzed), **participants and setting** (*who* was studied, where and when), and **procedures and analysis** (*how* data was collected and analyzed).

!!! note "Associate with context"

    Everything that is asserted about what was done/seen should be associated with a **snippet** — screenshot or quote, **with page numbers**. This includes both the **summary of the observation/result** (the key tables/figures/quotes that ground it) and the **details of the methods**. This helps a ton with future sensemaking! It can be time-consuming, so for the purposes of this mission, we want every EVD to be anchored in a screenshot of an observable, like a key figure/table or crucial quotes.


**Example** (supporting the CLM above): *~60 percent of InstructGPT-generated analogical explanations for scientific concepts were rated by crowd workers as containing a meaningful analogy, comparable to human-generated analogies.*

### PTN — Pattern

Patterns are conceptual classes such as theoretical objects, heuristics, design patterns, and system/methodological approaches, that are abstracted from a *specific* implementation. They are what make specific systems "work" or not, matched to a model of the problem.

**Examples:** Integrated crowdsourcing · Direct Manipulation · boundary objects · incremental formalization · Ephemeral UIs · transformer language model · Shared Representation · Hypertext · Computer-Supported Argumentation · Toulmin structures · abstractive summarization · extractive summarization

### ART — Artifact

Artifacts are specific concrete systems (prototypes, standards, etc.) that instantiate one or more conceptual patterns or methods.

**Examples:**

- Ideahound — instantiates *Integrated crowdsourcing*
- DynaVis — instantiates *Ephemeral UIs*

### Other node types!

You may think of more node types, too! These are just the node types that I've found particularly useful in my research in HCI, so I feel comfortable recommending them to you to try out!

For example, sometimes it's also useful to call out (named) **theories** (THE), which are broader explanatory accounts of *why* or *how* things work as they do — a set of mechanisms and relationships that generates predictions across many situations. Where a PTN is a reusable move you can point at in a system, a THE is the explanation you'd reach for to say why or how that move should work at all. These would make contributions to *conceptual* problems in HCI, in [Oulasvirta and Hornbæk's](https://dl.acm.org/doi/10.1145/2858036.2858283) language.

**Examples:** information foraging theory · the Notional Model of Sensemaking

---

## Which nodes should I be looking for?

It depends on what you're reading *for*:

| If you're reading a paper to inform...                                                                                                                                                         | ...you care about noting down                                                                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| an **empirical** question, like "Do platforms bans stop the spread of antisocial behavior online?"                                                                                             | CLMs and their supporting/opposing EVD — including claims about system efficacy, which help establish the unknown frontier                                          |
| a **design** question, like "How might we design interventions that stop the spread of antisocial behavior online while balancing tradeoffs between individual fairness and community health?" | ARTs (example systems), and their underlying core design PTNs                                                                                                       |
| a **conceptual/theoretical** question, like "Why do bans succeed in stopping the spread of antisocial behavior in some cases but not others?"                                                  | key THEories, and PTNs or concepts and the key CLM predictions they make for your setting, and/or key EVD for these CLMs (and by extension, support for the theory) |

Most CHI papers will give you several types at once. Start with whichever matches your driving interest. This also means you'll likely be *selectively* reading CHI papers based on your interest, rather than extracting or summarizing them as a whole. This is how working researchers read strategically!

In Part 1 of the mission, you share strategic, "node-oriented" notes you've taken on the papers you've selected. These then become raw ingredients for the map you'll make.

---

## Part B — Building and extending the map from (with) nodes

Once we have a sense of the nodes of knowledge for an area of research inquiry, we can use them to construct a higher-level **synthesis** (or map) of **where we are in a scholarly conversation and how we (can) contribute to / advance the conversation.**
### Mapping a scholarly conversation

Useful maps of a scholarly conversation depend on what kind of question/contribution you're after!

For example: 

**If the contribution is a system**, review the design space / history of prior art, with something like this structure — for each key **PTN**:

- key exemplar **ART**s for this PTN
- key **CLM** and **EVD** about this PTN in relation to the core problem
- and any open **QUE** you address

**If the contribution is empirical**, review prior insights and questions, with something like this structure — for each key **CLM** about some core (sub)**QUE**:

- key supporting and opposing (possibly conflicting!) **EVD**, with intuitions about strength of evidence
- and then any open **QUE** that remain

You may think of others!

This is Part 2 of the CHI papers mission!
### Finding opportunities for new contributions to the conversation

A map is often most useful because it helps you see opportunities for new contributions to the conversation! 

Here are some ways you can do this:

1. **Do xyz PTNs work for our task/context of interest? What might (new) ARTs that draw from these PTNs to work in our setting look like?**
2. **This ART seems awesome, but doesn't quite do X — how might we make it do X (e.g., drawing inspiration from CLMs or PTNs or THEs)?**
3. **Lots of people say this PTN is great, but we don't have great EVD that it actually works.**
4. **CLM A and CLM B are in major tension — what sort of decisive EVD might help us figure out a winner (or a new explanation)?**

You'll practice this in Part 3 of the CHI papers mission by proposing nodes of your own that connect to / derive from parts of your map in Part 2.

---

When you're ready to put this to work, head back to the [CHI Papers Mission](missions/chi-papers.md).
