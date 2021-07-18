# GAPS

_Generalized Assignment Problem Solver_

This code aims to implement an efficient solver for the generalized assignment problem.

## The generalized assignment problem

The generalized assignment problem is described quite well [on Wikipedia](https://en.wikipedia.org/wiki/Generalized_assignment_problem).

This code actually allows for further generalization, multiple agents to perform a single task (regulated by a task budget).

## The implementation

The implementation is a simple depth-first search algorithm. Therefore, it does not work well for very large problems.

The depth-first search expands most promising nodes first. True maximum assignment is guaranteed when algorithm is allowed to complete. Otherwise, the assignment printed last may be used as a best guess.

The code makes use of `frozendict` to keep track of the set of assignments.

## Running the code

Solving your assignment problem is easy. Just specify your assignment problem (refer to main method in `assign.py` for an example), then run it. An example problem specification is given, to make clear what syntax is expected.

The code offers a few features:
* Optional 'hard assignment' initializes the assignment with certain agents assigned to certain tasks
* Optional 'fair' parameter maximizes the profits related to the least profitable task (and thus equalizes the profits among tasks).
* Optional 'complete' parameter requires agents and tasks to fully use their budgets.
* 'verbose' option prettily prints the assignment information after the code finishes. May be turned off.
