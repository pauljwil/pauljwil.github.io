---
layout: single
title: Work Samples
permalink: /work-samples/
author_profile: true
toc: true
toc_sticky: true
---

This page showcases a collection of my technical writing and software development projects, demonstrating my skills and expertise in both disciplines. These samples provide insights into my ability to communicate complex technical concepts effectively and demonstrate proficiency in various programming languages and tools.

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

### Release notes

[Mirantis Secure Registry 2.9.1 Release Notes](https://web.archive.org/web/20231110152837/https%3A%2F%2Fdocs.mirantis.com%2Fmsr%2F2.9%2Frelease-notes%2F2-9-1.html)

Authored release notes encompassing product enhancements, issue resolutions, and security updates. Collaborated with ticket owners in Jira to create initial drafts for each release note, ensuring accurate and comprehensive coverage. Coordinated with a technical writer and the engineering team lead to review and edit the collection of release notes, incorporating their feedback and suggestions. Iteratively refined the drafts based on the review process until the release notes received final approval.

## Software Development

In addition to my expertise as a technical writer, this page showcases my experience as a software developer, specializing in Go and Python. While the majority of my development work has been in private GitHub repositories, the featured projects offer a glimpse into the skills I have acquired while working as a developer. These projects serve as concrete examples of my coding abilities and demonstrate my technical proficiency in the software development field.

### Fullstack

[Recipes Online](https://github.com/pauljwil/recipes-online)

Used React, Go, and MongoDB to create a fullstack web application for storing recipes that showcases my skills in web development, backend server programming, and database management.
This application allows users to get, add, update, and delete recipes using a web interface. As the sole developer working on this project, I conceptualized, designed, and implemented
both the frontend and backend components.

### Go

[Docker Registry Exporter](https://github.com/pauljwil/docker-registry-exporter)

Developed a Prometheus exporter specifically designed for Docker registries, enabling the exposure of essential metrics such as repository and tag counts. This exporter serves as a valuable tool for monitoring and collecting key information from Docker registries, facilitating better visibility and analysis of repository and tag data.

[RethinkDB Exporter](https://github.com/pauljwil/rethinkdb-prometheus-exporter)

Created a fork of an existing RethinkDB exporter, expanding its functionality by incorporating additional metrics for the `current_issues` table and table sizes. Additionally, implemented comprehensive unit testing to ensure the reliability and accuracy of the exporter. This enhanced version of the exporter provides improved monitoring and analysis of RethinkDB deployments.

### Python

[Replacer CLI](https://github.com/pauljwil/replacer-cli)

Developed a command-line interface (CLI) application that enables users to search for and replace text within multiple files in a given directory. This application provides a convenient and efficient way to perform bulk text replacements, saving time and effort when working with large sets of files.
