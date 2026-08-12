---
layout: page
title: Concerto reconfiguration
description: Component-based coordination applied to the deployment and reconfiguration of distributed databases
img: assets/img/proj_concerto.svg
importance: 4
category: research
tags: [Concerto, Galera, Ansible, Grid'5000, Python]
links:
  - name: Galera experiment
    url: https://gitlab.inria.fr/VeRDi-project/galera-experiment
    icon: fa-brands fa-gitlab
  - name: Concerto-D
    url: https://github.com/Concerto-D/concerto-decentralized
    icon: fa-brands fa-github
  - name: Grid'5000
    url: https://www.grid5000.fr
    icon: fa-solid fa-server
---

**Concerto** is a formal, component-based model for coordinating the lifecycle of distributed
software: each component is described by **places**, **transitions**, and **ports**, and the
coordination engine derives a correct parallel execution of deployment and reconfiguration
operations.

This work is the experimental groundwork behind [CoAnsible]({{ '/projects/5_project/' | relative_url }}):
before extending Ansible with coordination logic, you need a reference point on what coordinated
reconfiguration actually buys you.

---

### 🧩 What I worked on

- Running **Galera cluster** deployment and reconfiguration scenarios on **Grid'5000**, comparing
  Concerto-driven coordination against plain imperative automation
- Translating existing **Ansible playbooks into Concerto assemblies**, and building the tooling that
  extracts the dependency structure from a playbook to generate the corresponding component code
- Measuring reconfiguration time and parallelism on multi-node deployments, across several Grid'5000
  sites

---

### 🔍 Why it is interesting

Configuration management tools describe _what_ the state of a machine should be, but they have no
first-class notion of _when_ an operation on one node may proceed with respect to another. Adding a
coordination model on top exposes the real parallelism of a reconfiguration, and makes the
synchronization points explicit instead of implicit in the order of tasks.
