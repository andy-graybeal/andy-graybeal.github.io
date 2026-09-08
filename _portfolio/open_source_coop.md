---
title: "Open-Source Infrastructure, Network Security, and Digital Operations"
excerpt: "Design and administration of segmented networks, pfSense firewalls, encrypted VPNs, Linux systems, centralized IAM, virtualization, monitoring, and backups."
collection: portfolio
---

# Open-Source Infrastructure and Network Security at Worker-Owned Restaurant Corporation

From 2004 through 2013, I served as co-owner and the sole systems and network administrator for Worker-Owned Restaurant Corporation in Athens, Ohio. IT was not a full-time position; I divided my time between technology responsibilities and restaurant operations, including work as a prep cook. I designed and administered an open-source environment that supported approximately 90 people across a restaurant, bakery, bar, nightclub, manufacturing facility, catering operation, and festival and farmers market activities. The environment included approximately 20 centrally managed workstations, segmented networks, firewall and VPN administration, Linux desktop management, virtualized servers, centralized authentication, monitoring, and automated backups.

## Network Design and Firewall Administration

The network I inherited used CAT5 runs assembled from multiple joined cable segments rather than continuous end-to-end runs. It also relied on an unmanaged hub. The organization experienced recurring network errors, and the existing equipment provided no practical way to separate traffic or manage the network centrally.

I redesigned the physical and logical network with structured cabling and a managed switch that I could configure and monitor. I introduced VLANs to segment network traffic, while firewall rules controlled which systems and services were reachable. The wireless design provided separate networks for patrons and workers rather than placing both groups on the same network.

I initially administered the firewall directly with OpenBSD/PF and later migrated firewall operations to pfSense. The web interface made routine rule management and troubleshooting easier while retaining PF as the underlying firewall technology. I used Nmap to verify that systems exposed only the intended services and ports.

For remote offices I configured encrypted site-to-site connectivity with OpenVPN and Tomato-based routers.

I documented the network in Dia and updated the diagrams as the environment changed.

## Windows to Linux Migration

I led the organization’s transition from Windows to Linux.  Linux Terminal Server Project infrastructure centralized workstation administration for approximately 20 workstations used by 90 people. This improved consistency and reduced desktop software licensing costs.

As part of the Linux platform’s lifecycle, I upgraded the Ubuntu environment from version 8.04 to 10.04.

I also maintained a pool of approximately 10 IBM/Lenovo ThinkPad T-series laptops running Linux for staff to take home. Staff used X2Go from these laptops to connect remotely to the organization’s systems.

Seven computers remained on Windows because of application requirements: two ran QuickBooks, while five supported the organization’s legacy point-of-sale system. I used Cygwin to integrate these systems with Linux-based administrative and backup workflows and wrote Bash scripts to detect system or application failures. I also installed Icinga agents to monitor their health.

## Implementation and User Adoption

I introduced changes incrementally while keeping the organization’s active systems available. User training was part of the implementation process, particularly when moving staff from Windows to Linux, migrating productivity work from Microsoft Office to LibreOffice, providing remote access through X2Go, and later migrating services to Google Workspace. The office-suite transition also required converting hundreds of the organization’s existing documents and spreadsheets into formats that could be maintained in LibreOffice.

Many of the organization’s administrative and operational workflows originally relied on pen-and-paper records or spreadsheets. Digital files were scattered across individual computers in different offices, often with separate versions of the same material and no centralized backup. I helped consolidate these files into centrally managed storage, digitize paper-based processes, and move selected spreadsheet-based workflows into database-backed applications. This provided more consistent access to shared information and brought important organizational data into the managed backup system.

## Virtualized Server Environment

I deployed and administered an on-premises KVM/libvirt environment to consolidate services that had previously depended on separate physical systems. The virtualized environment hosted directory services, file and print services, monitoring, backup infrastructure, web applications, and other internal services.

The primary hardware was an IBM server with hot-swappable SCSI drives. I configured its Linux storage using mdadm and LVM, providing software-managed disk arrays and flexible allocation of storage to the hosted services.

Virtualization made it easier to manage workloads centrally and use available hardware more efficiently. Monitoring and utilization data also supported capacity planning, hardware lifecycle decisions, and budgeting.

## Identity and Access Management

I implemented centralized identity and access management with Zentyal, OpenLDAP, PAM, Samba, and Kerberos. PAM connected Linux workstation logins to the centralized directory, while Samba and Kerberos supported shared services and single sign-on.

This design allowed users to authenticate to their workstations and access authorized internal resources without maintaining a separate account for every system.

After I took responsibility for IT, I established on-premises file and email services for the organization. The Linux file services used ext3 storage. I implemented role-based access by mapping employee job functions to Linux groups and using POSIX access control lists, administered with `setfacl` and `getfacl`, when the standard owner, group, and other permissions were not sufficient. I later migrated the file and email services to Google Apps, now called Google Workspace, and integrated authentication using OAuth.

I also integrated OrangeHRM with LDAP so employees could use centralized credentials to access the organization’s HR system.

I deployed and administered GNU Mailman as a central communication service for internal teams and external contacts. Mailing-list membership was organized around employees’ roles, allowing messages to reach the appropriate functional groups without maintaining individual recipient lists. The system also helped consolidate external communications with vendors, customers, and other contacts. I later migrated these role-based mailing-list functions to Google Groups within Google Workspace.

## Monitoring and Operational Support

I deployed Nagios/Icinga and SNMP monitoring to track network devices, servers, service availability, and system health. Each computer was supported by an uninterruptible power supply (UPS), and I used the temperature readings reported by those units to record conditions in rooms throughout the facilities. I also used Icinga to monitor the temperatures of the walk-in freezer and walk-in refrigerator at the remote manufacturing facility and warehouse. Icinga sent email alerts when monitored services or environmental readings indicated a problem. I used monitoring data to identify issues, investigate performance changes, and plan upgrades.

Request Tracker provided a centralized workflow for recording, assigning, and following technical issues. It also created a history that could be used for troubleshooting and operational planning.

## Automated Cross-Platform Backups

I designed and automated a backup workflow for Linux systems and the Windows machines. Bash scripts used rsync to collect and stage data from systems, with Cygwin providing the required tools on Windows. Cron scheduled the synchronization jobs, and Bacula managed the centralized backups.

The workflow used SSH public-key authentication, host-key validation, and restricted backup accounts. I tested restores to confirm that backed-up data could be recovered.

In addition to the centralized backups, I maintained a weekly offsite tape copy at a separate office so that recovery did not depend entirely on the primary site. Tapes at the primary location were stored in a fire-resistant safe.

## Web Services and Payment Security

I designed and administered the organization’s WordPress website and e-commerce services. I migrated the site from on-premises hosting to an AWS EC2 instance running a LAMP stack. The site supported event promotion, product sales, and public communication.

I also maintained PCI-DSS compliance for systems involved in payment processing.

## Project Boundary

I evaluated Compiere, ADempiere, OpenERP, and Openbravo as possible open-source ERP platforms. I selected Openbravo because it already offered a working restaurant-oriented point-of-sale system and began the groundwork for implementation, but the system was not deployed before I left the organization.

I considered using Alfresco for operational documentation, including HACCP food-safety materials, Safety Data Sheets (SDS), and related OSHA compliance records, but it was never put into use.

I began work on Moodle as a possible employee training platform and sought help developing learning modules. The content-development effort did not move forward, and Moodle was never fully deployed.

I configured TimeTrex to authenticate through LDAP as a possible timesheet system, but it did not progress to official organizational use.

Across this work, I was responsible for infrastructure design, implementation, administration, troubleshooting, documentation, access control, monitoring, automation, and recovery testing.
