---
layout: single
title: Case Studies
permalink: /case-studies/
author_profile: true
toc: true
toc_sticky: true
---

The case studies below represent enterprise work completed at Cisco/Splunk. Because they involve internal systems and proprietary code, I focus on the problems, architecture, design decisions, and outcomes rather than source code.

## AI authoring platform

**Overview:** Built an internal platform that centralizes documentation authoring knowledge and makes it available to AI coding agents, pairing a searchable knowledge base with a deterministic DITA validation service so agents work in accordance with team standards.

**Role:** Built the platform, including retrieval, validation, agent skills, and a content synchronization pipeline. A developer on my team provided the infrastructure it runs on.

**Challenges:** Writers had no scalable way to give their agents the knowledge that governs how documentation is created, so they parsed the DITA specification on demand or pasted it into chats, and every such copy went stale as soon as its source changed. Model training data was also weak on DITA. Terminology enforcement, meanwhile, suited deterministic checks better than semantic retrieval, which ranked related content ahead of the exact entries a style decision required.

**Solution:** A retrieval service, exposed to local writing agents through an MCP server, indexes the DITA 1.3 specification, the *Splunk Style Guide*, and our Heretto authoring guidance in Confluence. CI refreshes the index from those living sources, and results cite source and page so guidance stays traceable. A DITA Open Toolkit service reports invalid DITA XML and style guide violations deterministically over an HTTP endpoint. Agent skills sit on top, including one that converts Markdown into valid DITA ready for upload to the CCMS. Because the skills retrieve guidance at runtime rather than embedding it, documentation updates propagate without rebuilding the workflows.

**Impact:** Serves an enterprise documentation team along with a growing number of external contributors, who use the Markdown-to-DITA workflow to reduce manual authoring effort and lower the barrier to contributing DITA content. The same pipeline keeps guidance current across an expanding set of AI-assisted authoring tasks.

**Learn more:** [Building knowledge pipelines for AI-assisted authoring](/knowledge-pipelines-for-ai-assisted-authoring/).

## Documentation platform automation

**Overview:** Built a CI-driven automation platform for our DITA CCMS, maintaining a nightly mirror of a multi-gigabyte content set and extending it with reporting, metadata write-back, PDF refreshes, and Markdown generation for AI consumption.

**Role:** Own this project as sole architect and developer across its five pipeline stages.

**Challenges:** Running CI against more than 400,000 topic files spread across hundreds of version branches, including a metadata manifest whose nightly commit grew repository history by hundreds of megabytes a night. Long-running jobs, from a 90-minute download to multi-hour builds, make late failure expensive: the pipeline needs continuous tuning, and a stage that breaks has to stop the run rather than pass bad output downstream.

**Solution:** The platform runs as five sequential stages, each committing state before handing off to the next, so no stage ever works from stale input. Making that survivable at scale meant moving the nightly manifest out of version history into an expiring build artifact, tuning git transfer settings for the download size, adding a prerequisite gate that catches a missing dependency in seconds rather than hours into a build, and guarding each stage so it fails loudly instead of publishing degraded content.

**Impact:** Reporting gives information architects the coverage data driving metadata cleanup, resource IDs give every documentation page a copiable permalink, and PDFs stay current through a monthly refresh cycle, with new version releases generated automatically as they ship. The platform has become our main source of leverage for building on top of our CCMS.

## Content migration to DITA CCMS

**Overview:** Consolidated three legacy documentation sites into a single DITA-based CCMS, unifying product content across hundreds of versions.

**Role:** Led the migration of two of the three sites, built the automation, and coordinated the move itself: sequencing which guides converted when, then working with writers to get content uploaded, reviewed, and branched for versioning.

**Challenges:** The two sites had very different architectures, one versioned and one not, and the legacy content included outliers that followed no consistent pattern. ID handling, case-sensitivity conflicts, cross-publication links, and legacy site redirects had to be reconciled across systems, on a tight timeline resourced almost entirely by internal team members.

**Solution:** Built a suite of Python tools: navigation tree crawler, HTML fetcher, DITA converter, topic splitter, map creator, and a version diff handler that uploaded only the topics that changed between versions. The suite began as a single existing migration script, customized to the content at hand and then extended feature by feature. Each stage recorded its output, so writers reviewing a new version only had to check the topics the diff handler had uploaded, and any later question about a topic's origin could be answered from that record. AI-assisted development is what made a custom tool suite of this scope feasible for a team this size on this timeline.

**Impact:** Delivered faster than would have been possible without AI assistance, and significantly reduced manual post-migration cleanup while improving content reuse and enabling reliable cross-product navigation.

**Learn more:** [Lessons Learned in an AI-Assisted Content Migration](https://blogs.cisco.com/innovation/lessons-from-an-ai-assisted-content-migration) on the Cisco Innovation blog.

## Documentation samples

Earlier documentation work at Mirantis, written for Kubernetes administrators, SREs, and developers. These pages are hosted on the Internet Archive and can take up to 10 seconds to load.

**Procedural:** [Configure Prometheus to scrape MSR metrics](https://web.archive.org/web/20231110150634/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F3.1%2Fops%2Fmonitor-msr%2Fcollect-msr-metrics%2Fconfigure-prometheus.html)

Authored the documentation for a Prometheus monitoring feature that I also implemented as a software developer, acting as my own subject matter expert and verifying the procedure across orchestration platforms.

**API reference:** [Mirantis Kubernetes Engine 3.6.2 API documentation](https://web.archive.org/web/20231110151635/https://docs.mirantis.com/mke/3.6/api-ref/mke-api-3-6-2.html)

Revitalized the API documentation by migrating from Swagger to Redoc and generating an OpenAPI specification directly from the Go codebase for each release. Integrated the generated specification into the Sphinx documentation site to improve navigation and maintainability.

**Procedural:** [Configure a canary deployment](https://web.archive.org/web/20231110150936/https%3A%2F%2Fdocs.mirantis.com%2Fmke%2F3.6%2Fops%2Fdeploy-apps-k8s%2Fnginx-ingress%2Fconfigure-canary-deployment.html)

Documented end-to-end configuration of NGINX Ingress canary deployments in Mirantis Kubernetes Engine, working closely with the feature developer to produce production-ready guidance for Kubernetes administrators.

**Conceptual:** [MSR product overview](https://web.archive.org/web/20231110153612/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F3.1%2Foverview.html)

Reworked this conceptual overview across multiple releases, explaining Mirantis Secure Registry's architecture, capabilities, and deployment scenarios for technical decision-makers.