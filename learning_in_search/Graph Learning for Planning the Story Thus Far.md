---
authors:
  - Dillon Z Chen
  - Mingyu Hao
  - Sylvie Thiebaux
  - Felipe Trevizan
venue: arXiv
---
# Summary

A brief history of graph learning for planning, central results, and future research directions.

## Related Works
* [[paper_reading/learning_in_search/Effective Data Generation and Feature Selection in Learning for Planning|Effective Data Generation and Feature Selection in Learning for Planning]]
	* Talks about feature generation and construction of useful graphs
* [[paper_reading/learning_in_search/Guiding GBFS through Learned Pairwise Rankings|Guiding GBFS through Learned Pairwise Rankings]]
	* Uses graphs to produce pairwise comparators to guide greedy search
* [[paper_reading/learning_in_search/Learning Domain-Independent Heuristics for Grounded and Lifted Planning|Learning Domain-Independent Heuristics for Grounded and Lifted Planning]]
	* A direct application of the graph learning work
# Notes

## Contributions
* A solid citation of the history of prior work from the field
* A good summary of planning, graphs in planning, and how they are used
* A flag in the sand and a call to arms both scientifically and community-wise
## Key Insights
* Despite repeated attempts, LLMs haven't successfully solved general planning tasks
	* Despite repeated failures, people are still running at that particular wall
	* _Completeness_ seems to be the saving grace here.
		* Reinforcement learning approaches learn policies which may be incomplete
		* LLMs are, at their heart, reinforcement learning based.
* h^* is the wrong heuristic for satisficing search
	* Fucking preach it sister!
		* Guidance and pruning aren't the same thing
		* Guidance and bounds aren't the same thing
		* Their work is closely aligned with mine
	* The reason for this is multi-faceted
		* Search algorithms assume it
			* ![[paper_reading/learning_in_search/heuristic_search_taxonomy.jpg]]
		* It's an easy canonical thing to learn
		* It's obvious how to build the training set
* Their Key Takeaways
	* Classical ML consistently outperforms deep learning in symbolic planning
		* Autoencoders have too much overhead from a performance perspective
		* Human intuition about feature selection is really good here
	* Learned ranking functions consistently outperform learned cost to go estimates
	* Learned heuristics with simple search algorithms are competitive with well engineered algorithms
		* Doing the simple thing well and wrenching on it a bit is equivalent to over-engineering a system in less diplomatic terms
* Open Questions / Issues
	* The community is shit at reproduction and this area is particularly thorny
		* What do we learn from?
		* How do we evaluate fairly?
	* Generalization is a real problem
		* All of the learning is applied to problem instances that are out of distribution
		* We're trying to learn on simple instances and bootstrap from there
		* This suggests an approach that #future_research
			* Ranks instances by hardness
			* Buckets
			* Solves smallest buckets optimally
			* trains h_1
			* solves next bucket approximately 
			* trains h_2
			* etc
## Questions
## Other Notes
