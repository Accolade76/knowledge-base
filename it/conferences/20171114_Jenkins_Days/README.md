# Jenkins Days - Amsterdam - 14 November 2017

## Introductions

### Speaker: Dharmesh Sheta - Senior Solution Architect - Cloudbees

* Jenkins needed to be updated because its UI look & feel was too 2005. Blue Ocean look was integrated in.
* Declarative Scripting Language for Jenkins makes pipelines and infra-as-code more accessible to people who are not primarily developers. There is also a Blue Ocean plug-in that adds a Pipeline Editor.
* 'Rock-Solid Jenkins': Cloudbees picks up open-source plug-ins and improves/certifies them to ensure dependability. They also provide vendor support.
* 'CloudBees Assurance Program (CAP)', Fixed Release & Rolling Release versions:
  - Bug & Security fixes
  - New features (No for Fixed; Yes for Rolling)
  - Release frequency (2x year Fixed; Monthly Rolling Release)
  - Integrations included (~125)
* CloudBees Solutions:
  - Jenkins
  - Jenkins Team
  - Jenkins Enterprise Solution (to address enterprise-wide Jenkins support, it's no longer just on team managing their own jenkins orchestration). Sheta: "But as CD scales, business risk increases". Think upgrading your master and what impact that would have on 200 pipelines.
  - Distributed Pipeline Architecture: provide each team with their own Jenkins Master so they can install and maintain their own plug-ins & pipeline without impacting other teams.
  - Enterprise is for the 'shared services' team in an organization (same people who manage version control, etc.). It provides CD as a service, self-service Jenkins and turnkey provisioning.
  - Some big customers are using 2,000 Masters, 10,000 executors and 317 VMs (as an example of scale)
* Jenkins Open-Source is for individuals and single teams.
* CloudBees Jenkins Team - Teams
* Cloudbees Jenkins Enterprise - Organizations...etc.
* Introducing CloudBees DevOptics - (Monitoring?)
* Cloudbees Jenkins Adviser (Plug-in): Helps analyze, identify, and advise on your Jenkins installation.
  Challenges:
  - Teams only identify issue once it has impacted their delivery.
  - Jenkins instability is failure to follow best practices
