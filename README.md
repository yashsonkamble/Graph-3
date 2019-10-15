# Graph-3

## Problem1: Min Diff Between Given Path and Path in the Graph

Given a graph whose nodes are 3-letter words and an array of 3-letter words. Find a path in the graph such that the difference b/w words in the path and given array is minimum.

We are given 2 APIs which work for this graph:

    class Graph {

	/**

	* Get all neighbors of a node.

	*/

	Set<String> getNeighbors(String node);


	/**

	* Get a list of all nodes in no particular order.

	*/

	Set<String> listAllNodes();

    }
Consider a graph G:


Example 1:

Input: G, arr = [AAA, BBB, CCC, DDD]

Output: 2

Explanation: The path [AAA, BBC, CCD, DDD] is closest to given array.

In path, BBC differs from BBB by 1 and CCD differs from CCC by 1 hence answer is 1 + 1 = 2.

Example 2:

Input: G, arr = [AAA, CCC, AAA, BBD]

Output: 3

Explanation: The path [AAA, BBC, AAA, BBC] is closest to given array.

In path, BBC differs from CCC by 2 and BBC differs from BBD by 1 hence answer is 2 + 1 = 3.


Notice that we can visit the same node multiple times.

## Problem2: Distribute Water in a Village (https://leetcode.com/problems/optimize-water-distribution-in-a-village/)

There are n houses in a village. We want to supply water for all the houses by building wells and laying pipes.

For each house i, we can either build a well inside it directly with cost wells[i], or pipe in water from another well to it. The costs to lay pipes between houses are given by the array pipes, where each pipes[i] = [house1, house2, cost] represents the cost to connect house1 and house2 together using a pipe. Connections are bidirectional.

Find the minimum total cost to supply water to all houses.

Example 1:

Input: n = 3, wells = [1,2,2], pipes = [[1,2,1],[2,3,1]]

Output: 3

Explanation: 

The image shows the costs of connecting houses using pipes.

The best strategy is to build a well in the first house with cost 1 and connect the other houses to it with cost 2 so the total cost is 3.

Constraints:

1 <= n <= 10000

wells.length == n

0 <= wells[i] <= 10^5

1 <= pipes.length <= 10000

1 <= pipes[i][0], pipes[i][1] <= n

0 <= pipes[i][2] <= 10^5

pipes[i][0] != pipes[i][1]
