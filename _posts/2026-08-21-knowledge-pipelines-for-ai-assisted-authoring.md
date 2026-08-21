---
title: "Building knowledge pipelines for AI-assisted authoring"
---

As AI becomes part of everyday authoring work, increasingly capable models and agent tooling are only part of what makes these systems genuinely useful. Just as important is how effectively organizational knowledge can be made available to AI agents. This challenge extends well beyond documentation teams, but content professionals are particularly well positioned to help solve it. We've spent years creating, organizing, and governing knowledge, which is exactly the groundwork needed to build the pipelines that connect authoritative organizational knowledge with AI-enabled workflows.

I work on a Content Engineering team, helping support the tooling and architecture behind a team of enterprise software technical writers. Like many knowledge workers, our writers are figuring out how to use AI to maximize their impact. From where I sit, two of the biggest obstacles are integrating AI agents with core authoring tools, and making the right organizational knowledge available to agents efficiently while keeping it current.

This post focuses on the second problem.

## When organizational knowledge is disconnected from AI

For our writers to use AI effectively, their agents need reliable access to the knowledge that governs how we create documentation:

* Our style guide
* Our Heretto CCMS authoring guidance in Confluence
* The DITA 1.3 specification (we author the majority of our docs in DITA XML)

Without supporting infrastructure, writers devised workarounds for solving this, but they often didn't scale. They downloaded the DITA specification and asked their agent to parse it on demand. They built skills that referenced the entire style guide. They copied and pasted Confluence pages into chats when they needed guidance.

These approaches can work, but they're inefficient. They also create a maintenance problem: any downloaded or embedded documentation becomes stale as soon as the source changes.

## From personal tool to shared infrastructure

I first ran into this problem personally. When I moved into my current role, I was learning content reuse strategy alongside DITA Open Toolkit plugin development. I leaned into AI, but quickly discovered that model training data wasn't particularly strong on DITA or its surrounding ecosystem.

Around November 2025, as coding agents became much more capable, I spent a weekend building a RAG (retrieval-augmented generation) system that indexed the DITA specification and the DITA Open Toolkit documentation. Instead of relying on training data or parsing large documents from scratch, my AI tools could retrieve the information they needed.

The results were immediately useful. Complex questions about DITA became much easier to work through, and I spent less time hunting through documentation. What began as a solution to my own problem turned out to be a useful architectural pattern for the broader authoring team.

The resulting system eventually grew into what I'm calling a knowledge pipeline: infrastructure that continuously connects authoritative organizational knowledge to AI agents.

## Building the pipeline

At its center is a RAG system that indexes the DITA specification, our style guide, and our Heretto CCMS authoring guidance in Confluence. A CI pipeline regularly pulls the latest content from our living documentation sources, transforms it, and updates the search index. Since the DITA specification is stable, it only needed to be indexed once.

We expose this knowledge through an MCP (Model Context Protocol) server, allowing local AI agents to retrieve relevant information as they work. Retrieval results cite the source and page, giving writers a way to trace guidance back to the authoritative content behind it.

Alongside retrieval, we built a deterministic validation service that reports invalid DITA XML and style guide violations over an HTTP endpoint. Not every authoring decision is best handled through semantic retrieval. Some require consistent, deterministic validation.

We also developed a small set of reusable skills. Two teach agents how to use the knowledge pipeline itself, including retrieval and validation. The other two automate a workflow our writers repeatedly requested: aligning Markdown drafts with our style guide and converting them into valid DITA. Applying DITA markup can be challenging, particularly for outside contributors. Combining style guide alignment with automated DITA conversion improves consistency, shortens delivery time, and lowers the barrier to contribution.

## From retrieval to reusable workflows

Once the pipeline was in place, it became useful in two complementary ways: as an interactive reference system for writers and as infrastructure that powers reusable AI workflows.

**The first use case is interactive retrieval.**

Rather than manually searching specialized reference documentation, writers can ask questions directly against authoritative sources. In our environment, that includes questions such as:

* How do I create a relationship table?
* Which elements and attributes are allowed here?
* Can you show me an example based on the specification?
* How does reuse affect this structure?

The value is that the answers are grounded in current source material and traceable to their origin, allowing writers to verify guidance and spend less time searching through reference documentation.

**The second use case is embedding the same knowledge into reusable workflows.**

For example, a skill that creates new topic stubs retrieves our current authoring guidance from Confluence, including conventions for naming, identifiers, reuse, and content structure. Because that guidance is retrieved at runtime rather than embedded in the skill itself, updates to our documentation are reflected automatically without rebuilding the workflow.

That distinction has turned out to be an important architectural advantage. The same knowledge pipeline that helps a writer answer a question also helps AI workflows stay aligned with current organizational guidance. Rather than encoding knowledge into prompts or individual skills, we keep it in authoritative sources and make it available wherever it's needed.

We're still in the early stages, but we've already seen writers and external contributors use the Markdown-to-DITA workflow to reduce manual authoring effort, while the same underlying pipeline provides reliable guidance across a growing set of AI-assisted authoring tasks.

## Not every kind of knowledge should be retrieved

One of the more interesting lessons has been that not every knowledge source belongs in a RAG system.

Our usage dictionary, for example, hasn't been a particularly good fit.

There are two main reasons:

* The agent first has to identify candidate words or phrases before it knows which dictionary entries should be checked.
* Semantic search naturally retrieves conceptually related content, which can rank similar sections ahead of the exact entries needed for a style decision.

For terminology enforcement, we've found deterministic validation to be much more effective than retrieval. In our case, that validation is implemented with XSLT, although tools such as Vale solve a similar class of problems.

More broadly, we've learned that different kinds of knowledge call for different ways of bringing them into an AI-assisted workflow. Some information is best retrieved as context when it's needed. Other information is better enforced through deterministic checkpoints.

## Expanding the pipeline

We're still exploring where to take the system next. The initiative I'm most excited about is a topic example gallery.

Rather than only retrieving specifications and authoring guidance, the system will also retrieve high-quality examples of task, concept, and reference topics, along with more specialized patterns such as tutorials, API endpoints, compatibility matrices, release notes, and other recurring content types.

Today, our Markdown-to-DITA workflow can generate valid markup, but it doesn't yet have a rich library of examples to draw from. By making those examples available through the same knowledge pipeline, we can help agents produce more consistent DITA semantics and stronger content structure from the start.

Others in the field are working through the same design questions. In [Designing an AI Workflow's Repo](https://sreyad.medium.com/designing-an-ai-workflows-repo-14e746e068dd), Sreya argues for pairing good examples with anti-patterns that show why a given pattern fails, a distinction worth accounting for as a gallery like this grows.

## Beyond authoring

What we've built so far is a modest piece of a much larger picture. Retrieval and validation solve some immediate problems, but broader knowledge pipelines will also intersect with how knowledge is authored, governed, structured, updated, and integrated into workflows. That can include metadata and its governance, knowledge graphs, authoring integrations, and cross-functional processes, alongside the retrieval and validation mechanisms we've started with.

Documentation teams are a natural place to develop these ideas because we're already responsible for creating and maintaining structured content. We spend our time thinking about how knowledge is created, organized, reused, governed, and kept current. Those concerns increasingly matter beyond documentation and authoring teams.

As models and agent tooling continue to evolve, a central part of our work will be building the pipelines that connect them to authoritative, current organizational knowledge.
