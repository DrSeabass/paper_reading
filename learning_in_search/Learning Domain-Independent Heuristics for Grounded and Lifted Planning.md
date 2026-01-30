---
authors:
  - Dillon Z Chen
  - Sylvie Thiebaux
  - Felipe Trevizan
venue: AAAI
---
# Summary
This paper shows how to use graph neural networks (GNNs) in order to learn direct guidance for algorithms like greedy search. The authors spend a lot of time focusing on the graph representation that enables the machine learning itself, but the produced heuristics appear to be quite strong and are relatively efficient to compute.

## Related Works
* The entire body of learning heuristic values directly is kind of anti-related, but massive
# Notes

* The focus is on representation size reduction.  
	* They learn in lifted planning to reduce size of representation and make things more tractable.
* Claimed contributions
	* New graph representations in grounded and lifted planning
	* First heuristic derived from such representation
	* Theoretical bounds on expressivity of a particular ML model, message passing neural networks (MPNN)