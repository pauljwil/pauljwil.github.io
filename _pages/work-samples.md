---
layout: single
title: Work Samples
permalink: /work-samples/
author_profile: true
---

This page showcases a collection of my technical writing and software development projects. These samples provide insights into my skills and expertise in both disciplines, highlighting my ability to communicate complex technical concepts effectively and demonstrate proficiency in various programming languages and tools.

## Technical Writing

The documentation samples provided here are tailored to the needs of DevOps Engineers, Cloud Architects, Site Reliability Engineers, System Administrators, Software Developers, and other professionals in similar roles. These resources are designed to effectively communicate technical concepts, procedures, and best practices to this target audience,.

### Deployment Procedures

[Mirantis Secure Registry 3.0.x installation instructions](https://docs.mirantis.com/msr/3.0/install/install-online.html)

This documentation was developed through an iterative process. Initially, I received information from a subject matter expert (SME), which I organized and drafted. However, the initial version lacked guidance on setting up the Kubernetes environment for the MSR cluster. Responding to customer feedback, I personally experienced the challenges of setting up a Kubernetes environment and documented my observations. I collaborated with a team member to incorporate this information into the documentation. As customer demands evolved, they requested additional verification steps to ensure the operational status of prerequisite components. I addressed this feedback by including verification instructions and troubleshooting commands for handling failed components.

### Operations Guide

[Use Helm charts with Mirantis Secure Registry](https://docs.mirantis.com/msr/3.0/ops/use-helm-charts.html)

This portfolio piece showcases a diverse range of documentation types, including conceptual, procedural, and reference materials. Initially, I received the raw content from the developer responsible for the feature. I then restructured and transformed the content into draft form. Another technical writer then provided valuable edits, which I incorporated into the document. I refined and revised the draft until it received approval from both the documentation and development teams.

### Reference Material

[Mirantis Secure Registry 3.0 system requirements](https://docs.mirantis.com/msr/3.0/common/msr-system-reqs.html)

This documentation outlines the essential system resource requirements and recommended allotments for running MSR 3.0. I first received the necessary information from the development team, which I organized and presented in draft form. To ensure accuracy and clarity, the draft underwent thorough editing and approval processes led by another writer and the development team. Subsequently, valuable feedback from customers and the support team was collected, and I incorporated their input into the current version of the documentation.

### API Documentation

[Mirantis Kubernetes Engine 3.6.2 API documentation](https://docs.mirantis.com/mke/3.6/api-ref/mke-api-3-6-2.html)

Revitalized the API documentation by migrating from Swagger to Redoc to enhance the overall presentation. Created an OpenAPI specification from the Golang codebase for each release and integrated it into the Sphinx-based documentation site.

[Sidescale API documentation](../sidescale-api)

Developed comprehensive API documentation for a cloud services platform utilizing the Apache CloudStack API. Created a user-friendly site using the Slate static site generator and GitHub Pages. Implemented a custom Javascript script to convert the API documentation from JSON to Markdown, ensuring a smooth and accurate transition between the data format and the markup language.

## Troubleshooting Articles

[Troubleshoot migration with Mirantis Migration Tool](https://docs.mirantis.com/msr/3.0/migration-tool/troubleshoot-migration.html)

With extensive involvement in testing the Mirantis Migration Tool (MMT), I collaborated with another writer to create a comprehensive troubleshooting section for the MMT documentation. Working closely with developers and the QA team, we documented detailed troubleshooting steps for different problem scenarios encountered during MMT testing. As users reported issues with the tool, we continuously expanded and enhanced the troubleshooting section to address emerging challenges. Taking the lead in drafting the additional content, I ensured its accuracy and clarity, which was further refined through reviews by a technical writer and SMEs.

### Release Notes

[Mirantis Kubernetes Engine 3.5 Release Notes](https://docs.mirantis.com/mke/3.5/release-notes.html)

Authored release notes for multiple patch releases, encompassing product enhancements, issue resolutions, security updates, known issues, and middleware versioning details. Collaborated with ticket owners in Jira to create initial drafts for each release note, ensuring accurate and comprehensive coverage. Coordinated with a technical writer and the engineering team lead to review and edit the collection of release notes, incorporating their feedback and suggestions. Iteratively refined the drafts based on the review process until the release notes received final approval.

### QuickStart Guide

[Install Mirantis Container Runtime on Ubuntu](https://docs.mirantis.com/mcr/20.10/qs-ubuntu.html)

Delivers a streamlined installation guide for Mirantis Container Runtime (MCR), enabling users to quickly set up and run MCR in less than an hour. Optimized the comprehensive installation instructions to include only the essential steps required for installing MCR in a test environment. Collaborated with a technical writer and SME to review and refine the draft. Iteratively revised the guide based on their feedback until it received their final approvals.

## Software Development

In addition to my expertise as a technical writer, this page showcases my experience as a software developer, specializing in Go and Python. While the majority of my development work has been in private GitHub repositories, the featured projects offer a glimpse into the skills I have acquired while working as a developer. These projects serve as concrete examples of my coding abilities and demonstrate my technical proficiency in the software development field.

### Go

[Docker Registry Exporter](https://github.com/pauljwil/docker-registry-exporter)

Developed a Prometheus exporter specifically designed for Docker registries, enabling the exposure of essential metrics such as repository and tag counts. This exporter serves as a valuable tool for monitoring and collecting key information from Docker registries, facilitating better visibility and analysis of repository and tag data.

[RethinkDB Exporter](https://github.com/pauljwil/rethinkdb-prometheus-exporter)

Created a fork of an existing RethinkDB exporter, expanding its functionality by incorporating additional metrics for the `current_issues` table and table sizes. Additionally, implemented comprehensive unit testing to ensure the reliability and accuracy of the exporter. This enhanced version of the exporter provides improved monitoring and analysis of RethinkDB deployments.

### Python

[Replacer CLI](https://github.com/pauljwil/replacer-cli)

Developed a command-line interface (CLI) application that enables users to search for and replace text within multiple files in a given directory. This application provides a convenient and efficient way to perform bulk text replacements, saving time and effort when working with large sets of files.
