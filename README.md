# Dynamic Colonel Blotto for Cybersecurity

This repository contains the full dataset, source code, and simulation framework developed for the MSc thesis **“Colonel Blotto in Cybersecurity: Real-World Data,
Reinforcement Learning and Information Asymmetry”** by **Zalán Nagy** (Budapest University of Technology and Economics, 2025).


## Overview

The project models attacker–defender interactions as a **reinforcement learning–driven Colonel Blotto game** grounded in real-world vulnerability data.

- **Data sources:** CVE, CVSS, and EPSS datasets  
- **Languages:** Python (Q-learning framework, simulation scripts)  
- **Structure:** Daily-updating vulnerability environment and intra-day adaptive learning episodes  
- **Scenarios:** Four information-asymmetry regimes reflecting different intelligence conditions  
- **Metrics:** Reward ratios, entropy dynamics, breakthrough probability, and top-k vendor coverage  


## Abstract

In the modern cybersecurity landscape the rapid discovery and exploitation of vulnerabilities create a constant state of competition between attackers and defenders.  
The exposure of products released by vendors evolves continuously as newly disclosed vulnerabilities reshape the risk map through their severity and exploitability.  
Within this framework the allocation of resources represents a critical decision-making challenge.  
The focus of the analysis is on how an attacker and a defender agent can make strategic decisions and adapt within this dynamically changing game space.

The thesis examines the problem of cybersecurity resource allocation within a multibattlefield Blotto-type game in which the battlefields represent vendors.  
The value of each battlefield is derived from real vulnerability data and a vendor-level risk indicator is updated daily.  
This indicator takes into account both the severity and exploitability of vulnerabilities.  
In each round a fixed budget is available which the defender and the attacker distribute across the battlefields as resources.  
This corresponds to the practical scheduling of patch priorities inspection capacity and attack focus.  
The allocation expresses how much capacity is devoted to inspecting or attacking a given vendor’s products and software components.  
Four situations are compared that differ in information access opponent observability and in the knowledge of perceived versus actual battlefield values.

Both players are modeled as learning agents and their decisions are tuned using reinforcement learning specifically Q-learning over a predefined small strategy set.  
The model evolves on two time scales.  
Reinforcement learning occurs within episodes and when new data arrive the battlefield values are updated.  
The convergence of strategy selection is quantified via a stabilization index and the results are compared across information access settings using multiple complementary measures.  
The learning defender consistently outperforms non-adaptive approaches and remains effective in a changing risk environment.  
The amount and freshness of available information significantly affect both the speed of convergence and the final performance providing practical guidance for patch management and compliance (for example NIS2) processes.  
Regular data-driven reallocation supported by a learning agent measurably improves defensive effectiveness in a dynamically changing threat environment.