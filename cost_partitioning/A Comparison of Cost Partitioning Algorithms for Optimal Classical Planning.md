---
authors:
  - Jendrik Seipp
  - Thomas Keller
  - Malte Helmert
venue: ICAPS
---
# Summary
Honestly what it says on the tin.  The paper investigates several approaches to cost partitioning heuristics for optimal combinatoric search including:
* Uniform Cost Partitioning
* Saturated Cost Patritioning
* Post-Hoc Optimization Cost Partitioning
* Greedy Zero One Cost Partitioning

They also do an investigation across a number of inputs to the cost partitioning process:
* Hill Clmbining on PBDs
* Systematic PDBs (Pommerening, Roeger and Helmert 2013)
* Cartesian Abstractions of Landmark Heuristics (Seipp and Helmert)
* Cost Partitioning of Landmark Heuristics Directly

There are some neat theoretical results.  Turns out there is a best, from heuristic accuracy and dominance standpoint, way of doing things.  That said, just because we can compute dominating heuristics doesn't mean that the optimal search goes fast.  The cost of solving an MILP at every node is prohibitively expensive, to the point that baseline heuristics like h_ff perform better in practice from a wall-clock time perspective.
## Related Works
* Domain-independent construction of pattern database heuristics for cost-optimal planning
* Getting the Most Out of Pattern Databases for Classical Planning
* Counterexample-guided Cartesian Abstraction Refinement

#TODO Refine with additional notes if we head this way with our own research