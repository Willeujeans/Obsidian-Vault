## Problem:
Starting at San Francisco and finding the shortest path to hit all major cities once then return back to San Francisco.

This is a graph theory problem, the cities being nodes and the connections are the edges

These is an impossible algorithm because if you want the best answer every time you'll need to check the travel distance between many variations of paths.
It can be simplified to: $\frac{(n-1)!}{2}$ 
Because as we travel we have 1 less city to travel to
Divide by 2 because half of the options are simply reordered but the same distance.

## Finding Close to Perfect
Minimum spanning tree (MST)
Nodes are connected with the minimal edge distance, with no cycles.
This will touch everything once on the path but will not return back home, and does involve touching at least one node again.

## Heuristic Solutions
### Nearest Neighbor
Starting at the first node we travel to the nearest node in distance, and repeat.

### Greedy
Nodes will be connected shortest edges first.
If a connection will form a cycle then we reject it.
If a connection will make the node have a degree of 3 (3 connections) then we reject it.

## Improvements
Once you have the path you'll be taking you can improve it

Random swapping
Swap the order of two cities at random to see if the distance is reduced.

2-Opt Improvement
Connecting 2 pairs of edges in the only other configuration

3-Opt Improvement
Connecting 3 sets of edges in the only other configuration


