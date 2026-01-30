---
authors:
  - Farid Musayev
  - Dominik Drexler
  - Daniel Gnad
  - Jendrik Seipp
venue: ECAI
---
# Summary
How can we learn to guide algorithms better for satisficing search?  We learn to classify transitions directly as being either:
* Leading to a goal
* Not making progress towards a goal
* Leading to a portion of the search where no solutions exist
In this way, we can learn to guide a search algorithm directly.  Following such a learn policy can be effective on its own, but it's better when hedged with greedy search on a numeric heuristic:

![[policy_plus_greedy_search.excalidraw.png]]

Learning relies on description logic to lift features and optimal solutions on small reference instances.  The idea was that the behaviors learned in small instances of a given domain could transfer.
## Related Works
* [[Guiding GBFS through Learned Pairwise Rankings]]
	* Similar
		* Also learns to decide which node should be expanded
		* Also treats the problem of learning as classification
	* Difference
		* Labels are global here, local there
* [Github Repo](https://github.com/mrlab-ai/transition-classifier)
* Feature Generation
	* Learning General Planning Policies from Small Examples without Supervision #TODO put it on the to-read pile
	* Description Logics state features for planning #TODO put it on the to-read pile
# Notes
* Contributions
	* New search algorithm that blends policy following and traditional best first search strategies
	* Description logic as a way of mining features out for classification
	* The notion of the three labels and a technique for training a classifier to make them
* Key Insights
	* Sometimes you only need heuristics for discrimination
	* If the heuristic is perfect, you can follow it greedily to the goal
	* Pruning plateaus early should help tons
* Questions
	* How does this work in domains that aren't logic based (numeric planners, industry solvers?)
	* How critical is the presence of large unsolvable portions of space to the performance?
	* Can we be more aggressive in our segregation of nodes
		* e.g. only expand green nodes in our queue first, then considering orange or red when we are starved for progressing nodes