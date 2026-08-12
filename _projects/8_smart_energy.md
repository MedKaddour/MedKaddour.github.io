---
layout: page
title: Smart energy & NILM
description: Event detection, deep clustering and anomaly detection on residential electricity consumption
img: assets/img/proj_nilm.svg
importance: 6
category: research
tags: [NILM, Python, TensorFlow, Signal Processing, Anomaly Detection]
links:
  - name: Tukey's Fences (arXiv)
    url: https://arxiv.org/abs/2402.17809
    icon: fa-solid fa-file-pdf
  - name: Outlier detection (IJSSCI)
    url: https://doi.org/10.4018/IJSSCI.2021070102
    icon: fa-solid fa-file-lines
  - name: Thesis (HAL)
    url: https://theses.hal.science/tel-04461469
    icon: fa-solid fa-graduation-cap
---

**Non-Intrusive Load Monitoring (NILM)** infers what individual appliances consume from a single
aggregate electricity signal, without installing a sensor on every device. This line of work started
during my PhD and continued through several student supervisions and publications.

---

### ⚡ Event detection with Tukey's Fences

The core contribution is a **statistical event detector** for aggregate current signals: a fast
Fourier transform isolates the relevant frequency content, and **Tukey's fences** flag the samples
that fall outside the expected spread. Appliance switching events are then detected without training
data, and with a high accuracy compared to threshold-based baselines.

Published as a preprint: _Event Detection for Non-intrusive Load Monitoring using Tukey's Fences_
(Kaddour, Lehsaini, Bouchachia).

---

### 🧠 Unsupervised disaggregation

Building on the detected events, I worked on **convolutional deep embedded clustering**: a
convolutional autoencoder compresses each event window into a small latent representation, K-Means
initializes the cluster centroids, and a DEC objective refines the assignment. The goal is to group
switching events by appliance **without labelled data**, which is the main practical obstacle to
deploying NILM in real homes.

---

### 📉 Anomaly detection in consumption data

Earlier work compared unsupervised **outlier detection** methods (Isolation Forest, One-Class SVM,
K-Means) on real consumption traces to identify abnormal electricity usage, published in the
_International Journal of Software Science and Computational Intelligence_.

---

### 🧑‍🎓 Related supervision

This topic fed three Master's internships I supervised at the University of Tlemcen: daily activity
detection in smart homes, deep clustering for non-intrusive device monitoring, and anomaly detection
in electricity consumption.
