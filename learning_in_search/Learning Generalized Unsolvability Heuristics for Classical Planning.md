---
authors:
  - Simon Stahlberg
  - Guillem Frances
  - Jendrik Seipp
venue: IJCAI
---
# Summary
We can learn to recognize dead ends in planning problems. If we're lucky, we can learn this on small instances and extrapolate the learning to larger domains, especially if the features somehow generalize.

## Related Works
* [[paper_reading/learning_in_search/Combining Heuristics and Transition Classifiers in Classical Planning|Combining Heuristics and Transition Classifiers in Classical Planning]]
	* Transition classification vs state classification, but both the data generation approach and the binning approach as "good" vs "not good" states is similar
# Notes

## Contributions
* Investigates 3 ways of learning policies for dead end detection
* Shows formal results on what is needed for learning dead end detection
## Key Insights
* Dead end detection in the broadest sense is as hard as decidability
* Not every domain makes it that hard
	* In fact, some domains are only hard because of representation
* Not every domain makes it feasibly
	* Logics used are planning specific
	* Dead ends have to be representable in a liftable way
## Questions
## Other Notes
