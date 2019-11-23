# Graph-3

## Problem1: Distribute Water in a Village (https://leetcode.com/problems/optimize-water-distribution-in-a-village/)

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

## Problem 2:Find Celebrity(https://leetcode.com/problems/find-the-celebrity/)

Suppose you are at a party with n people (labeled from 0 to n - 1) and among them, there may exist one celebrity. The definition of a celebrity is that all the other n - 1 people know him/her but he/she does not know any of them.

Now you want to find out who the celebrity is or verify that there is not one. The only thing you are allowed to do is to ask questions like: "Hi, A. Do you know B?" to get information of whether A knows B. You need to find out the celebrity (or verify there is not one) by asking as few questions as possible (in the asymptotic sense).

You are given a helper function bool knows(a, b) which tells you whether A knows B. Implement a function int findCelebrity(n). There will be exactly one celebrity if he/she is in the party. Return the celebrity's label if there is a celebrity in the party. If there is no celebrity, return -1.

Example 1:

Input: graph = [

 [1,1,0],

 [0,1,0],

 [1,1,1]

]

Output: 1

Explanation: There are three persons labeled with 0, 1 and 2. graph[i][j] = 1 means person i knows person j, otherwise graph[i][j] = 0 means person i does not know person j. The celebrity is the person labeled as 1 because both 0 and 2 know him but 1 does not know anybody.



Example 2:

Input: graph = [

 [1,0,1],

 [1,1,0],

 [0,1,1]

]

Output: -1

Explanation: There is no celebrity. (edited) 

Note:

The directed graph is represented as an adjacency matrix, which is an n x n matrix where a[i][j] = 1 means person i knows person j while a[i][j] = 0 means the contrary.

Remember that you won't have direct access to the adjacency matrix.
