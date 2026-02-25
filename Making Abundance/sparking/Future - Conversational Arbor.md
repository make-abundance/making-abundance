---
status: design
area: sparking
---

# Future — Conversational Arbor

> [!info] This is a design
> A roadmap for how navigation through the vault evolves. The current filesystem approach is intentionally simple — it's the foundation for what comes next.

## Current: Filesystem Navigation

Wikilinks and "From here" sections. The reader navigates by clicking through documents, guided by contextual links at the bottom of each piece. The graph view shows the vault's structure at a glance: green for sparking, blue for engine room, amber for open questions.

This works for the current audience — a small, fully-aligned circle doing the thinking together. It's simple, transparent, and requires no infrastructure beyond Obsidian.

**What it does well:**
- Zero setup cost
- Every link is visible and inspectable
- The graph view reveals the shape of the thinking
- New documents slot in naturally

**What it can't do:**
- Respond to where a newcomer is — everyone gets the same links
- Adapt the sequence based on what someone has already read or felt
- Surface the right open question for the right person at the right time

## Next: SI Agent as Navigator

An SI that can route newcomers through the material based on their responses. Not a chatbot that answers questions about the content — an arbor that helps people find their own path through it.

The agent would:
- Start with a version of what `Abundance is Here Now.md` does in text — evoke the contraction, offer paths
- Listen to how the person responds and route accordingly (someone who says "I feel that" goes toward The Pointing-Out Piece; someone who says "prove it" goes toward The Argument Clarified)
- Track what's been read and offer the natural next step
- Surface open questions when someone's engagement suggests they might have something to contribute

The frontmatter system supports this: `status` tells the agent what's solid vs. exploratory, `area` routes between sparking and engine room, `sequence-step` orders the sparking flow.

**Key design constraint:** The SI agent is an arbor, not a funnel. It opens paths — it doesn't drive toward a predetermined destination. If someone wants to start with the engine room, the agent helps them do that well, not redirects them to start with feelings.

## Later: RAG-Supported Conversation

A conversational interface with retrieval-augmented generation over the full vault. The SI doesn't just route — it can synthesize, connect ideas across documents, and engage in genuine dialogue about the material.

This enables:
- A newcomer asking "What would this look like in my company?" and getting an answer that weaves together The Arbor, Kindness in Practice, and Operational Defenses
- A contributor asking "What's the most important open question right now?" and getting a curated answer based on the vault's current state
- A Campfire facilitator asking "What should I know before running this with a group of engineers?" and getting preparation drawn from multiple sources

**The frontmatter becomes essential here.** The RAG system needs to know:
- What's decided vs. exploratory (so it doesn't present open questions as settled truth)
- What area a document belongs to (so it can weight responses appropriately)
- Where things sit in the sequence (so it can respect the designed order while remaining flexible)

## The Through-Line

At every stage, the navigation is an arbor: structure that reveals paths rather than directing traffic. The filesystem links, the SI agent, and the RAG conversation all follow the same principle — open growing space for the reader, don't close it.

The evolution is in capability, not in philosophy. More paths to light, not a different kind of light.
