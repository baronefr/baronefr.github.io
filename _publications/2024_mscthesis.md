---
title: "Floquet counterdiabatic protocols for Quantum Annealing on Parity architecture"
collection: publications
permalink: /publication/2024-mscthesis
excerpt: 'We study Floquet counterdiabatic protocols for quantum annealing, specifically focusing on the Parity architecture.'
date: 2024-04-19
venue: 'Thesis UniPd'
paperurl: 'https://hdl.handle.net/20.500.12608/65146'
codelink: 'https://github.com/baronefr/parity-floquet'
citation: 'Francesco Pio Barone, 2024, Thesis UniPd'
---


### Abstract 

Combinatorial Optimization problems can be addressed with quantum computing techniques: the solution of an optimization problem can be encoded in the ground state of a quantum spin system, which in turn can be experimentally prepared through a suitable algorithm like Quantum Annealing. Still, annealing applications have to face several challenges. Firstly, the limited spin connectivity of current hardware requires the use of clever encoding strategies. In this sense, the Parity architecture can encode fully connected optimization problems without requiring on-hardware long-range connectivity. Secondly, a quantum system naturally transits toward excited states during its evolution, resulting in a prepared state with a reduced overlap over the true ground state of the problem-encoding Hamiltonian. To overcome this limitation, one needs to find and implement non-trivial Quantum Annealing protocols. In this work, we investigate Floquet counterdiabatic protocols for the Parity architecture. This combination of encoding and protocols constitutes a hardware-friendly recipe that does not require additional system controls. On the one hand, we study the accuracy of the Floquet protocols, eventually finding a suitable criterion to tune the protocol hyperparameters. On the other hand, we investigate the efficiency of Floquet schedules. We identify a narrow driving frequency regime where the Floquet protocol provides an advantage over the standard Quantum Annealing approach. We explore alternative protocols obtained by extending the derivation of Floquet schedules to higher orders of precision. Finally, we move away from the Floquet formulation and relax the requirement of preserving the original set of controls over the quantum system. Our work shows that numerically optimized counterdiabatic protocols using only extra local field controls can be advantageous over standard annealing approaches.