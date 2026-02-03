---
authors:
  - Levi Lelis
  - Sandra Zilles
  - Rob Holte
venue: AAMAS
---
# Summary
Stratified tree search uses a type system to ensure that only one node of each type is expanded at each depth.  The idea being that if types bin nodes by ultimate cost or quality of solutions beneath them, then stratified tree search can partition the space and search only a fraction of unique nodes with unique type combinations along a path and still find optimal solutions.

The type systems have to be effectively perfect for this to happen in practice.  Rather than rely on wishful thinking, they provide mechanisms for handling type collision with randomness, and for iterating over the search multiple times to create completeness.

## Related Works
* [[paper_reading/learning_in_search/Combining Heuristics and Transition Classifiers in Classical Planning|Combining Heuristics and Transition Classifiers in Classical Planning]]
	* classifier built in this set could be similar here
* [[paper_reading/learning_in_search/DLPlan - Description Logics State Features for Planning|DLPlan - Description Logics State Features for Planning]]
	* Description logics could form the basis for type classifications
# Notes

## Contributions

* The primary contribution is the algorithm.
* I don't know how to draw a visualization of the type system, so I'm going to leave off the algorithm sketch for now
## Key Insights
* If (and a big if) we can construct a type system to bin nodes in a certain way, we can restrict search to unique sequences of types and preserve both completeness and optimality
* This only works in domains with "weak" heuristics
	* Heuristics provide guidance on a node by node level
	* They aren't informative globally across the space
* In domains with strong heuristics we can expect
	* h to rank nodes semi-reliably globally
	* to be cheapish to compute
## Questions
## Other Notes
