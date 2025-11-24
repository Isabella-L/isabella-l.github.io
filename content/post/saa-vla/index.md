---
title: SAA - Stealthy Adversarial Attack on Vision-Language-Action Models
description: My master dissertation on the security vulnerability study of VLA models in robotics manipulation
slug: SAA
date: 2025-11-24T01:47:28+08:00
image: cover.jpg
math: true
categories:
    - Academic
tags:
    - embodied AI
    - robotics 
    - security 
    - MComp
# weight: 1       # You can add weight to some posts to override the default sorting (date descending)
hidden: false
comments: true
draft: false
---

## Overview of Attack Methodology

$$ 
\left\lVert f_\theta(v + \delta, l) - y^\text{true} \right\rVert_2 \ge \tau,\quad 
\mathcal{D}(v, v + \delta) \le \varepsilon
$$

![Overall SAA attack framework](image.png)

Here we see two objectives defined: 
1. The attack objective 
> $
\left\lVert f_\theta(v + \delta, l) - y^\text{true} \right\rVert_2 \ge \tau,
$
2. The Stealth objective 
> $ \mathcal{D}(v, v + \delta) \le \varepsilon$

Each objective are assigned with a threshold to define training optimal. 

They are trained in an alternative optimization algorithm inspired by [SPAA](https://arxiv.org/pdf/2012.05858), the algorithm is heavily altered to adapted to the adversarial need of VLA attacker. 

![SAA Algorithm](algorithm.png)


To understand more, you can check out my [presentation](/saa-presentation.pdf) or contact me at lusicheng@u.nus.edu 

## Simulation Experiment Result 

UPL is applied to the LIBERO Spatial Suite, showing task failure due to discrepancy in action

![Demonstration of task failure under perturbation](demo.png)

- d_thr = 15
- p_thr = 0.3

## Supplementary Training Information Report

![W&B Training Report](wnb.png)

## Photo with my senior 

![With Chongkai](with_gck.jpg)

My supervisor [Prof Shao](https://www.comp.nus.edu.sg/cs/people/shaol/) assigned one of his all mighty PhD to provide some support. Turns out, [Chongkai](https://chongkaigao.com/) is one of the best mentor I ever had. I appreciate his guidance very very much.

<!-- ## Guide on Finding a Professor 

## How to get started 

## Implementation

## Someone that is really important -->
