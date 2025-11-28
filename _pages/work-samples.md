---
layout: single
title: Work Samples
permalink: /work-samples/
author_profile: true
toc: true
toc_sticky: true
---

This page highlights my work in content operations, technical writing, and software development. The samples demonstrate my ability to solve complex problems, architect scalable documentation solutions, and communicate technical concepts to diverse audiences. You’ll also find examples of my proficiency in Go, Python, and other tools used to deliver impactful results across multiple domains.

## Content Operations

The following case studies highlight my work as a DITA Information Architect. These examples showcase how I design and implement scalable documentation systems, drive process automation, and solve complex challenges in content management.

### Content migration to DITA CCMS

* **Overview:** Migrated 30,000+ topics from legacy documentation sites into a DITA-based CCMS, unifying product content and versioning.
* **Role:** Led migration strategy, built automation scripts, and designed scalable processes.
* **Challenges:** Complex legacy structures, diverse versioning, and minimizing manual cleanup.
* **Solution:** Automated content conversion and DITA map creation with Python and XSLT; built a version diff tool to upload only changed topics between versions and resource ID-based linking for cross-deliverable links; accelerated delivery with AI-assisted coding.
* **Impact:** Reduced manual workload, improved content reuse, and enabled reliable cross-product navigation.
* **Learn more:** [Lessons Learned in an AI-Assisted Content Migration](https://blogs.cisco.com/innovation/lessons-from-an-ai-assisted-content-migration) on the Cisco Innovation blog.

### Heretto Sitemap Governance

* **Overview:** Improved sitemap integrity for DITA CCMS documentation by leading governance and process alignment initiatives.
* **Role:** Led policy creation, stakeholder alignment, and process improvements.
* **Challenges:** Drift between master and production sitemaps, inconsistent merging practices, and risk of content misalignment.
* **Solution:** Cleaned up and synchronized sitemaps, introduced conditional processing to safely merge references, and authored a sitemap governance policy to standardize practices.
* **Impact:** Increased release predictability, reduced rework, and ensured long-term platform stability.

## Technical Writing

The documentation samples provided here are tailored to the needs of DevOps Engineers, Cloud Architects, Site Reliability Engineers, System Administrators, Software Developers, and other professionals in similar roles. These resources are designed to effectively communicate technical concepts, procedures, and best practices to this target audience.

### Procedural

[Configure a canary deployment](https://web.archive.org/web/20231110150936/https%3A%2F%2Fdocs.mirantis.com%2Fmke%2F3.6%2Fops%2Fdeploy-apps-k8s%2Fnginx-ingress%2Fconfigure-canary-deployment.html)

This is one of several topics in a section on configuring Mirantis Kubernetes Engine (MKE) to use NGINX Ingress Controller. I collaborated closely with the feature developer, who provided me with the necessary information to draft the articles. Together, we refined the content, ensuring its comprehensiveness. After undergoing technical writer and developer review, the content was published and has remained largely unchanged since that time.

[Configure Prometheus to scrape MSR metrics](https://web.archive.org/web/20231110150634/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F3.1%2Fops%2Fmonitor-msr%2Fcollect-msr-metrics%2Fconfigure-prometheus.html)

Serving as the primary software developer in the creation of this feature, I acted as my own SME in the documentation process. I documented the configuration procedure through a combination of referencing my development notes and working with other developers to ensure that the documentation would work across orchestration platforms. The final draft went through both developer and technical writer reviews.

### Conceptual

[MSR product overview](https://web.archive.org/web/20231110153612/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F3.1%2Foverview.html)

Already in publication when I started at Mirantis, I reworked this page over the years to survey evolving feature offerings and an expanding set of platforms on which the software could run. Updates to this overview received SME, engineering manager, and technical writer reviews prior to publication.

### Reference

[Mirantis Secure Registry 3.0 system requirements](https://web.archive.org/web/20231110151437/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F3.0%2Fcommon%2Fmsr-system-reqs.html)

This documentation outlines the essential system resource requirements and recommended allotments for running MSR 3.0. I first received the necessary information from the development team, which I organized and presented in draft form. To ensure accuracy and clarity, the draft underwent thorough editing and approval processes led by another writer and the development team. Subsequently, valuable feedback from customers and the support team was collected, and I incorporated their input into the current version of the documentation.

### API

[Mirantis Kubernetes Engine 3.6.2 API documentation](https://web.archive.org/web/20231110151635/https://docs.mirantis.com/mke/3.6/api-ref/mke-api-3-6-2.html)

Revitalized the API documentation by migrating from Swagger to Redoc to enhance the overall presentation. Created an OpenAPI specification from the Golang codebase for each release and integrated it into the Sphinx-based documentation site.

[Sidescale API documentation](../sidescale-api)

Developed comprehensive API documentation for a cloud services platform utilizing the Apache CloudStack API. Created a user-friendly site using the Slate static site generator and GitHub Pages. Implemented a custom Javascript script to convert the API documentation from JSON to Markdown, ensuring a smooth and accurate transition between the data format and the markup language.

### Troubleshooting

[Filesystem storage back ends](https://web.archive.org/web/20231110151937/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F3.0%2Fmigration-tool%2Ftroubleshoot-migration%2Ffilesystem-storage-back-ends.html)

With extensive involvement in testing the Mirantis Migration Tool (MMT), I collaborated with another writer to create a comprehensive troubleshooting section for the MMT documentation, from which this page is drawn. Working closely with developers and the QA team, we documented detailed troubleshooting steps for different problem scenarios encountered during MMT testing. As users reported issues with the tool, we continuously expanded and enhanced the troubleshooting section to address emerging challenges. Taking the lead in drafting the additional content, I ensured its accuracy and clarity, which was further refined through reviews by a technical writer and SMEs.

### Release Notes

[Mirantis Secure Registry 2.9.1 release rotes](https://web.archive.org/web/20231110152837/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F2.9%2Frelease-notes%2F2-9-1.html)

Authored release notes encompassing product enhancements, issue resolutions, and security updates. Collaborated with ticket owners in Jira to create initial drafts for each release note, ensuring accurate and comprehensive coverage. Coordinated with a technical writer and the engineering team lead to review and edit the collection of release notes, incorporating their feedback and suggestions. Iteratively refined the drafts based on the review process until the release notes received final approval.

## Software Development

In addition to my expertise in content operations and technical communication, this page showcases my experience as a software developer, specializing in Go and Python. While the majority of my development work has been in private GitHub repositories, the featured projects offer a glimpse into the skills I have acquired while working as a developer. These projects serve as concrete examples of my coding abilities and demonstrate my technical proficiency in the software development field.

### Go

[Docker Registry Exporter](https://github.com/pauljwil/docker-registry-exporter)

Developed a Prometheus exporter specifically designed for Docker registries, enabling the exposure of essential metrics such as repository and tag counts. This exporter serves as a valuable tool for monitoring and collecting key information from Docker registries, facilitating better visibility and analysis of repository and tag data.

[RethinkDB Exporter](https://github.com/pauljwil/rethinkdb-prometheus-exporter)

Created a fork of an existing RethinkDB exporter, expanding its functionality by incorporating additional metrics for the `current_issues` table and table sizes. Additionally, implemented comprehensive unit testing to ensure the reliability and accuracy of the exporter. This enhanced version of the exporter provides improved monitoring and analysis of RethinkDB deployments.

### Python

[Replacer CLI](https://github.com/pauljwil/replacer-cli)

Developed a command-line interface (CLI) application that enables users to search for and replace text within multiple files in a given directory. This application provides a convenient and efficient way to perform bulk text replacements, saving time and effort when working with large sets of files.
