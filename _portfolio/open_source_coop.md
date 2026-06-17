---
title: "Building Open-Source On-Premise Infrastructure for a for a Multi-Faceted Worker-Owned Cooperative"
excerpt: "Open-Source Puzzle Piecing"
collection: portfolio
---

**Network Infrastructure:** I secured and modernized the organization's network by designing and implementing structured cabling and segmented wired and wireless access. To reduce attack surface and improve traffic management, I introduced VLANs and deployed a pfSense-based firewall solution. I extended secure connectivity to remote offices by configuring site-to-site VPNs using OpenVPN and Tomato firmware-based routers, replacing unreliable and unsecured remote access with a stable, encrypted architecture. I documented the network architecture using Dia, maintaining up-to-date diagrams to support troubleshooting, planning, and infrastructure visibility.

*Virtualized Server Environment:* To consolidate hardware and centralize service delivery, I deployed and administered an on-premises virtualized server environment using KVM/libvirt. This platform hosted directory services, file and print services, monitoring systems, backup infrastructure, web applications, and other business-critical workloads — replacing a fragmented collection of physical machines with a manageable, resilient infrastructure.

*Monitoring and Resilience:* I implemented proactive network and device monitoring using SNMP and Nagios, giving the organization real-time visibility into system health, performance trends, and potential failures before they became outages. To support structured incident tracking and response, I deployed and administered Request Tracker, providing a centralized workflow for managing and documenting support requests and issues. To strengthen data protection and recovery capabilities, I deployed and maintained a centralized backup system using Bacula. Together these systems supported long-term capacity planning, hardware lifecycle management, and annual budgeting decisions based on actual utilization data.

I also maintained PCI compliance for payment processing systems, ensuring secure handling of sensitive financial data and adherence to applicable security standards.

*Platform Migration — Windows to Linux:* To improve security, reliability, and operational efficiency while eliminating software licensing costs, I led a full organizational migration from Windows to Linux-based systems. As part of this effort, I implemented Linux Terminal Server Project (LTSP) infrastructure to centralize desktop management, and deployed X2Go-based remote access to support secure off-site and remote work — years before remote work became a mainstream necessity.

*Identity and Access Management:* Building on the new Linux platform, I implemented a centralized IAM solution using OpenLDAP through Zentyal, integrating Samba and Kerberos to deliver enterprise-style Single Sign-On (SSO). Users could authenticate once to their Linux workstations and access HR systems, business productivity tools, and shared file and print services without maintaining separate credentials. This architecture centralized authentication and authorization, simplified account provisioning and deprovisioning, reduced password-related support requests, and enforced consistent access controls and policy across the organization. I extended this further by integrating OAuth-based authentication for Google Workspace, bringing cloud-based collaboration tools under the same centralized access management umbrella.

I also deployed and managed GNU Mailman mailing list systems to support structured communication across internal teams and external customers.

*Web and Cloud Presence:* I designed, deployed, and managed the organization's WordPress website, supporting e-commerce functionality, event promotion, and public-facing communication. The site was hosted on AWS EC2 on a LAMP stack (Linux, Apache, MySQL, PHP), providing a secure, reliable, and scalable platform for online services and organizational outreach.

*Open-Source ERP:* One project I was unable to complete before my departure was the implementation of an open-source ERP system. After researching several options — including Compiere, ADempiere, and OpenERP — I settled on OpenBravo as the best fit for the organization's needs. The groundwork was laid, but the project was never finished. It remains a reminder that not every initiative reaches completion.
