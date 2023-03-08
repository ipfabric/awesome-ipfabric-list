# Awesome IP Fabric [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

List of links and repos of useful integrations for IP Fabric users and developers.

Repo is mirrored from https://gitlab.com/ip-fabric/integrations/awesome-ipfabric-list. Please open all issues or Pull Requests on GitLab.

## Table of Contents

- [Libraries](#libraries)
- [Monitoring](#monitoring)
- [Source of Truth](#source-of-truth)
- [Configuration Management](#configuration-management)
- [ChatOps](#chatops)
- [Miscellaneous](#miscellaneous)
- [Videos](#videos)
- [Blogs](#blogs)
- [Community](#community)

## Libraries

- [python-ipfabric](https://gitlab.com/ip-fabric/integrations/python-ipfabric)
  - IP Fabric supported Python SDK for interacting with IP Fabric API.
  - Please open bugs or feature requests on [GitLab](https://gitlab.com/ip-fabric/integrations/python-ipfabric/-/issues)
- [python-ipfabric-diagrams](https://gitlab.com/ip-fabric/integrations/python-ipfabric-diagrams)
  - IP Fabric supported Python SDK for interacting with IP Fabric Diagrams in v4.3 and above.
  - Example code to show how to use the diagram APIs - including the production of a reachability matrix
  - Please open bugs or feature requests on [GitLab](https://gitlab.com/ip-fabric/integrations/python-ipfabric-diagrams/-/issues)
- [aio-ipfabric](https://github.com/jeremyschulman/aio-ipfabric)
  - Community built Python Asyncio Client for IP Fabric.
  - [Python AsyncIO with IP Fabric Demo Video](https://www.youtube.com/watch?v=RLyKYP2_uiE)

## Monitoring

- [How to integrate with Splunk](https://ipfabric.io/blog/how-to-integrate-ip-fabric-with-splunk/)
  - Blog article discussing how a Splunk integration is performed.

## Source of Truth

- [Nautobot Single Source of Truth (SSOT) IP Fabric Plugin](https://github.com/nautobot/nautobot-plugin-ssot-ipfabric)
  - This is a plugin for the [Nautobot](https://nautobot.readthedocs.io/) platform (Netbox Fork) which allows for 
    connecting to an IP Fabric instance and using the information in IPF to populate or update Nautobot.
- [NAUTI (Network Automation Tools Integrator)](https://nauti-netdev.github.io/nauti-docs/)
  - This tool allows for the ability to sync from IP Fabric to Sources of Truth such as Netbox.
- [ipfabric-netbox](https://github.com/community-fabric/ipfabric-netbox)
  - The project is a combination of code samples and examples to migrate data between IP Fabric v4.4.x and NetBox v3.3.2.
- [ipf-netbox](https://github.com/jeremyschulman/ipf-netbox)
  - This package provides a CLI and python modules useful to integrate between IP Fabric and the Netbox project.

## Configuration Management

- [ipfabric-ansible](https://gitlab.com/ip-fabric/integrations/ipfabric-ansible)
  - Ansible collection to work with IP Fabric (Inventory, Modules).
- [nornir-ipfabric](https://github.com/routetonull/nornir_ipfabric)
  - IP Fabric inventory plugin for [nornir](https://github.com/nornir-automation/nornir).
- [ipf-netcfgbu](https://github.com/jeremyschulman/ipf-netcfgbu)
  - Save the network device configuration from IP Fabric into a Git repository.
- [python-ipfabric Config Example](https://gitlab.com/ip-fabric/integrations/python-ipfabric/-/blob/develop/examples/tools/config.py)
  - Example on how to use python-ipfabric to search and get device configurations or logs.

## ChatOps

- [Nautobot Chatops application](https://github.com/nautobot/nautobot-plugin-chatops-ipfabric)
  - [Nautobot](https://nautobot.readthedocs.io/) IP Fabric ChatOps integration with Slack, Teams, Webex etc
- [IP Fabric Webhook Notification](https://github.com/community-fabric/ipfabric-webhook-listener/tree/notify)
  - IP Fabric supported webhook listener and will send a notification to Slack or Teams when Snapshot events occur.
- [IP Fabric Slack Integration](https://github.com/ipfabric/ipfabric-slack-integration)
  - IP Fabric Slack Integration Example (built for IPF v3)

## Miscellaneous

- [Copy IP Fabric Settings](https://gitlab.com/ip-fabric/integrations/python-ipfabric/-/tree/develop/examples/copy_settings)
  - Copies settings including Intents and Dashboards from one instance to another
  - Excludes items such as authentication, users, passwords, etc.
- [Integration Demos](https://github.com/community-fabric/integration-demos)
  - Python examples used to demonstrate IP Fabric's integrations with other systems.
- [OSPF Cost Baseline](https://github.com/jamieparks/IPFabric-OSPF-Cost-Baseline)
  - Compares live OSPF Interface costs against a set of values in a CSV file.
- [Site Separation](https://github.com/sdargoeuves/ipf-siteSeparation)
  - With the addition of new Site Separation rules in IPF v4.3 please see 
    [Site Separation using Device Attributes Example](https://github.com/community-fabric/python-ipfabric/blob/main/examples/settings/attributes.py)
  - Python script to automatically update siteSeparation in IP Fabric based on external source for v4.2 or below.
- CVE reporting examples:
  - [python-ipfabric CVE Example](https://gitlab.com/ip-fabric/integrations/python-ipfabric/-/blob/develop/examples/tools/cve_check.py)
    - Uses python-ipfabric to pull CVE data for devices, sites, or vendors.
  - [CVE Report](https://github.com/community-fabric/cve-report)
    - Also uses python-ipfabric but creates an Excel report for all devices.
- Intent Rules
  - [python-ipfabric Intent Rule Reporting](https://gitlab.com/ip-fabric/integrations/python-ipfabric/-/blob/develop/examples/intent_reports.py)
    - Uses python-ipfabric to pull Intent checks and the example also shows an Excel report.
    - Also shows ho to use the comparison feature which compares Intent checks between snapshots.
  - [python-ipfabric Intent Rule Data](https://gitlab.com/ip-fabric/integrations/python-ipfabric/-/blob/develop/examples/intent.py)
    - Uses python-ipfabric to pull the data for an Intent checks which will return the table data not just the number
      of results.
- [Automated PDF Report](https://github.com/community-fabric/ipfabric-webhook-listener/blob/pdf_report/README-pdf.md)
  - Uses the webhook listener to create and email a PDF summary report when an automated snapshot completes
- [Webhook Listener to Postgres DB](https://github.com/community-fabric/ipfabric-webhook-listener/blob/postgres/README-postgres.md)
  - Uses webhook listener to extract certain data from IP Fabric and insert it into a Postgres DB for long term
    trending analysis for tools lie Tableau, Grafana, etc.

## Videos

- [Netbox September Community Call](https://netbox.dev/announcements/september-community-call/)
  - The recording of our September community call is now available on YouTube! This month, we welcome Jonathan Senecal to the maintainers team, celebrate the release of terraform-provider-netbox version 3.0, and highlight some interesting recent discussion. Perhaps most exicting is that Daren Fulwell joins us to demonstrate how users can leverage IP Fabric network assurance platform to programmatically and safely populate NetBox data.
- [Integrated Network Automation & Assurance](https://www.itential.com/tech-partners/ipfabric/)
  - [Live Network Field Day Presentation](https://youtu.be/2cq-5CDlFHI)
  - Using Itential with IP Fabric & Netbox to automate ServiceNow requests and check connectivity using Path Lookups
- [Closing the Loop with Network Assurance with IP Fabric](https://youtu.be/acZR2e8qJTM)
  - Product Evangelist with IP Fabric, will discuss how introducing network assurance completes the loop. Using IP Fabric’s model of the network of networks, you can measure the success of multi-stage, cross-domain workflows; validate the data in supporting tooling like IPAM, CMDB and monitoring; and use IP Fabric’s insight into your network behavior to trigger and influence automation workflow logic.
- [IP Fabric Youtube Channel](https://www.youtube.com/c/IPFabric/videos)
  - IP Fabric's official Youtube channel.
- [IP Fabric Network Field Day 27 (2022)](https://techfieldday.com/appearance/ip-fabric-presents-at-networking-field-day-27/)
  - Network Field Day 27 IP Fabric presentations.
- [IP Fabric Network Field Day 23 (2020)](https://www.youtube.com/playlist?list=PLinuRwpnsHaeH9fOOOKuXJWjijBZHa1iA)
  - Network Field Day 23 where IP Fabric presented.
- [Unboxing the IP Fabric API](https://www.youtube.com/watch?v=QX9o7UQJ9h4)
  - Discovering how to use the IP Fabric API.
- [Python for Excel Worksheets, data validation and modeling with IP Fabric](https://www.youtube.com/watch?v=JxWX1pOwZvg)
  - Using Python with IP Fabric to do data validation and create Excel documents.
- [Automated network remediation with IP Fabric](https://www.youtube.com/watch?v=pVGcqf1hNHQ)
  - Using IP Fabric's webhooks to trigger network automation activities in Python/Nornir
- [IP Fabric and Cisco PSIRT API](https://www.youtube.com/watch?v=1NAuWwwycDg)
  - Demo of a script to take output from IP Fabric and the Cisco PSIRT API and produce vulnerability reports for 
    Cisco devices in the inventory

## Blogs

- [Official IP Fabric Blogs](https://ipfabric.io/blog/)

## Community

- [Community Fabric Slack](https://join.slack.com/t/ipfabric-community/shared_invite/zt-1gqe9jvw1-aJImnQuieH3CR2KVqWZJzA)
  - IP Fabric's Open Slack server for access to the IP Fabric team and wider community discussion
- [Network to Code Slack](https://slack.networktocode.com/)
  - There is an #ipfabric channel on Network to Code's Slack which users can ask about Nautobot integrations.
