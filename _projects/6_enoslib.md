---
layout: page
title: EnOSlib multi-provider
description: Driving distributed system experiments across several testbeds from a single description (DAIS 2025)
img: assets/img/proj_enoslib.svg
importance: 3
category: research
tags: [EnOSlib, Grid'5000, Python, Reproducibility, Edge-to-Cloud]
links:
  - name: Paper (Springer)
    url: https://link.springer.com/chapter/10.1007/978-3-031-95728-4_2
    icon: fa-solid fa-file-lines
  - name: Open access PDF
    url: https://inria.hal.science/hal-05052776v1/document
    icon: fa-solid fa-file-pdf
  - name: EnOSlib
    url: https://gitlab.inria.fr/discovery/enoslib
    icon: fa-brands fa-gitlab
  - name: Documentation
    url: https://discovery.gitlabpages.inria.fr/enoslib/
    icon: fa-solid fa-book
---

**EnOSlib** is the experiment library the STACK and Discovery teams use to describe, deploy, and
evaluate distributed systems on real infrastructures. Historically, an experiment targeted a single
provider: you reserved machines on Grid'5000, or on a cloud, or on IoT-lab, but not all of them at
once.

Together with **Baptiste Jonglez**, **Matthieu Simonin**, and **Jolan Philippe**, I contributed to
extending EnOSlib with **multi-provider capabilities**, so that a single experiment description can
span the whole edge-to-cloud continuum.

---

### 🧪 What the extension brings

- **Synchronized reservations** across several testbeds, so that heterogeneous resources are
  available in the same time window
- A **uniform abstraction** over providers with very different reservation models (batch schedulers,
  cloud APIs, sensor testbeds)
- **Reproducible deployments**: the same description drives bare-metal nodes, virtual machines, and
  constrained edge devices
- Support for realistic **edge-to-cloud experiment topologies**, including network emulation between
  the tiers

---

### 🎯 Why it matters

Experimental research on the continuum is only credible if the experiments can be re-run. Being able
to describe a multi-tier deployment once, and replay it across providers, removes a large part of the
manual glue code that usually makes such experiments fragile and unrepeatable.

This work was published at **DAIS 2025** (25th IFIP WG 6.1 International Conference on Distributed
Applications and Interoperable Systems, part of DisCoTec 2025, Lille), and directly supports the
experimental setups used in my own observability and orchestration work.
