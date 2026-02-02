---
authors:
  - Dominik Drexler
  - Jendrik Seipp
venue: ICAPS
---
# Summary
An introduction of the DLPlan learning tool as part of their entry into the KR track for the planning competition I would guess.

## Related Works

* [[paper_reading/learning_in_search/Combining Heuristics and Transition Classifiers in Classical Planning|Combining Heuristics and Transition Classifiers in Classical Planning]] 
	* describes the planning approach that this tool allows
	* Builds on the repo directly
* [The Git Repo](https://github.com/rleap-project/dlplan)
* Derived Reading List
	* Learning and Exploiting Progress States in Greedy Best First Search
	* A Review of Generalized Planning in the Knowledge Engineering Review
	* Learning Control Knowledge for Forward Search Planning
# Notes

## Contributions
* The DLPlan tool for helping the community do learning
## Key Insights
* Taxonomies
	* We distinguish two types of knowledge:
		* Instance Specific Knowledge
			* What my path based corrections are
			* What my global corrections are
		* Domain General Knowledge
			* Learning on a domain that generalizes to instances
				* always fill both grippers when possible
				* always dump both grippers when it achieves goal predicates
				* etc
* Good High Level Descriptions
	* The concepts and roles are expressions describing unary and binary relationships over the domain (delta in the text). Both types of expressions are built recursively, starting from primitives and combining primatives to more expressive relationships.
	* Description logics are more expressive than propositional logic but less general that two-variable first order logic.
## Questions
* Was the goal of description logics generally and their application to planing in specific really to create human-understandable learnings?
	* Was the goal human knowledge or human understanding for debugging, explainable planning, etc.?
## Other Notes
