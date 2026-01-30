---
authors:
  - Mingyu Hao
  - Felipe Trevizan
  - Sylvie Thiebaux
  - Patrick Ferber
  - Joerg Hoffmann
venue: IJCAI
---
# Summary
This paper was really exciting because the authors focus on learning a ranking function for greedy best first search directly.  Their concern isn't in learning a numeric representation (though they do ultimately produce one), their interest is in learning the ranking specifically. That's cool because it's philosophically aligned with my beliefs about heuristic search and search guidance.

How it works is by optimally solving problems, and looking at nodes on the path to 

## Related Works
* All of the work on learning h^* from data found before search #TODO add some pointers
* My online learning stuff
* Effective Heuristics for Suboptimal Best first Search, Wilt & Ruml #TODO probably goes on the reading pile
* Chrestien et al, 2023, Optimize Planning Heuristics to Rank, Not to Estimate Cost-to-Goal from Neurips. #TODO probably goes on the reading pile
* [[Learning Domain-Independent Heuristics for Grounded and Lifted Planning]]
# Notes

* Key Insights
	* However, labelling states with informative values and attempting to learn accurate values for the heuristic is expensive and _unnecessary_ for the purpose of learning to guide GBFS.
	* While learning a pointwise ranking function is a regression problem, learning a pairwise ranking function is a classification problem.
		* This technically extends to any fixed number of elements n to be ordered, right?
		* Because of the reduced target complexity (ranking vs. estimation), it should be formally easier to recover a correct function for ranking rather than estimation
	* __learned heuristic__ orders more states than are necessary to find the optimal solution
		* Hell yes! The heuristic only need be accurate on the states encountered from the root towards the goal on a greedy search. 
		* Global accuracy is a hedge
		* To the extent that we can get away with it, we ought to prefer accuracy on nodes on the solution path over global ranking accuracy.
		* They leverage this in definition 3, but I think they don't go far enough
			* Still focused on cost optimal solutions as opposed to
				* Shortest possible solutions
				* Solutions through portions of the space that aren't 'puzzley'
* Contributions
	* Hey, greedy search isn't required to be guided by cost estimates
		* I mean, I've been banging that drum my whole career
		* And so have many authors before me (Gaschnig, Samuelson, etc)
		* Still, nice to see Joerg and Sylvie agree
	* They show how to learn from nodes off of optimal solution paths, increasing leverage of data generated for training
	* Better coverage in IPC domains
* h and h^* may necessarily have trouble distinguishing between states, but greedy search guidance needn't be limited in such ways
* GBFS is the algorithm most commonly used for satisficing planning
	* That's wild to me.  There are a large number of alternatives.
	* Can this truly be the best?
* Questions
	* How critical is reflexivity in the learned ranking?
		* I would guess critical for most open list as heap implementations?
		* Could we build an openlist that was designed to handle a relaxation of that constraint?