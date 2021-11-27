# fl-client-selection
> a very brief summary of client selections in federated learnings

[TOC]

## Client Selection for Federated Learning with Heterogeneous Resources in Mobile Edge

<u>*IEEE TWC 2019*</u>

**Motivation**

existing works focus on the problem in individual learning ⇒ overlooking long term performance

**Client Selection**

Goal & Criterion:

- energy efficient
  - transmission power (Shannon's formula)
  - local training energy consumption
- later training result is better (exp. verification, ascend > uniform || descend) in terms of loss, accuracy, robust
  - remark: mostly empirical, may need more experiments on temporal pattern

- more client is better [[2](https://arxiv.org/abs/1812.11750)] [[3](https://arxiv.org/abs/1907.06040)]

Solve:

incorporated client selection into overall performance optimization using Lyapunov method

use decision variable to decide whether a client is selected

## FedMCCS: Multicriteria Client Selection Model for Optimal IoT Federated Learning

<u>*IEEE IOTJ 2021*</u>

**Motivation:**

current complete/quasi random client selection cannot handle the heterogeneity of the client devices ⇒ some of the client may fail to complete task ⇒ many discarded learning rounds ⇒ affect the model accuracy

**Client Selection (FedMCCS)**

Goal: 

- consider the heterogeneity of the clients
- their limited computation and communication resources
- achieve maximum number of those that can complete FL rounds with out system cash
- maintain high-performance Fl mode in the mean time

Criterion:

- resource utilization is under budget per device type
  - CPU frequency
  - memory cost
  - energy cost
- time needed to complete a round is under threshold
  - download time
  - predicted update time (RUPred-LR)
  - upload time
- maximize event rate (?)

## Budgeted Online Selection of Candidate IoT Clients to Participate in Federated Learning

<u>*IEEE IOTJ 2021*</u>

**Motivation:**

optimize accuracy in *stateful* FL with a budgeted number of candidate clients

improve test accuracy

---

**Client Selection:**

Goal: select the $R$ best candidate clients based on their test accuracy

Criterion: test accuracy

Formulation & Solve: similar to secretary problem [[4](https://dl.acm.org/doi/10.1145/1399589.1399596)] [[5](https://www.jstor.org/stable/24540892)]

- evaluate the test accuracy of the first $\alpha^*$ clients and reject them all
- select the next $R$ clients with test accuracy better than the best test accuracy of the first $\alpha^*$ clients
- if none is found then select the last clients

*How to select the value of* $\alpha^*$ is a problem of probability.

## An Efficiency-Boosting Client Selection Scheme for Federated Learning With Fairness Guarantee

<u>*IEEE TPDS 2021*</u>

**Motivation:**

1. the number of clients could be sufficiently large & bandwidth is limited ⇒ should select clients
2. clients with low priority are simply being deprived of chances to participate at the same time ⇒ data imbalanced

---

**Client Selection (C2MAB + RBCS-F)**

Goal: select clients to minimize long-term model exchange time while guaranteeing fairness

Criterion:

- long-term fairness

- availability of clients
- selection fraction: sometimes available clients is not enough


Solve:

Lyapunov method

and one more thing to answer: *how to calculate the model exchange time?*

here using *Contextual Combinatorial Multi Arm Bandit*

<u>*The methods and formulations in this paper is highly similar to TWC2020*</u>

## SAFA: A Semi-Asynchronous Protocol for Fast Federated Learning With Low Overhead

*IEEE TC 2021*

**Motivation**

- address problems in federated learning  in extreme conditions
- mitigate the impacts of stragglers, crashes and model staleness

---

---

## Age-Based Scheduling Policy for Federated Learning in Mobile Edge Network

*IEEE ICASSP 2020*

---

## Federated Machine Learning: Survey, Multi-Level Classification, Desirable Criteria and Future Directions in  Communication and Network Systems

*IEEE Communications Survey & Tutorials 2021*

