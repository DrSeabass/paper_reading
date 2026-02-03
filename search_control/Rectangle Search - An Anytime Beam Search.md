---
authors:
  - Sofia Lemons
  - Wheeler Ruml
  - Rob Holte
  - Carlos Linares Lopez
venue: AAAI
---
# Summary
Paper introduces rectangle search.  A variant on beam search that exists in the family of anytime algorithms.  It eschews the memory limited nature of beam search in pursuit of better anytime behavior.

## Related Works
* Related Algorithms
	* Beam Search
	* Beam Stack Search
	* BULB
	* Anytime .* A*
	* Anytime EES
# Notes

## Contributions
![[paper_reading/search_control/rectangle_search.png]]
## Key Insights
* Remember that anytime search is actually a collection of algorithms with its own taxonomy
	* Contract Search is fed the deadline and tries to respond to it
	* Interruptable Searches try to have the best solution possible in hand at time T
* "However because anytime algorithms are intended for use cases in which the solutions found do not need to be proven optimal, and are not even expected to be optimal, it is not obvious that best first search is the most appropriate choice of algorithmic architecture."
* "On the other hand, rectangle search is not obliged to expand open nodes in order of their heuristic evaluation value (be it f, h, or d)"
## Questions
* How critical is the memory limitation anyway?
## Other Notes
* There's some fundamental relationship between
	* NP Hardness of a domain
	* Policy size for a policy that can provide optimal control
	* Computation needed to learn the above policy
	* Backtracking in search
* Effectively
	* All search is hedging
	* Hedging is required for NP hard problems
	* How you hedge is probably very important :tm:
	* 