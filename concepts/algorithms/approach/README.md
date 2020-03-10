Dynamic programming and Greedy algorithm to be used when the problem demands maximization or minimization of result. Greedy algorithm generates optimal solutions.


To create an algorithm for any problem, following are the 4 steps:à

Write down the input and output of the problem


Think of a brute force approach that can be used to generate the output from the given input


Make use of either pre-processing or extra space to lower down the complexity of the above solution


Create a mathematical, diagramatic, etc representation of the solution and wite down the pseudo code


The is a way called “exchange argument” that is a very useful tool for proving the correctness of a greedy algorithm.


To prove that an algorithm is correct, I generlly used some set of inputs and try to run the algorithm over it.
Inputs can be of many kinds. There is also a way to use Mathematical induction to prove that an algorithm is correct.

Adding more to solving problems, I have to gain expert knowledge of all the algorithms like Bipartite matching, Topological sort, etc
so that any problem that I read can be broken  down and checked for solution using the above mentioned algorithms.

 For using the Dynamic programming, you have to first make sure that the problem can be solved by the dynamic programming. To do this,
check if solution of the problem can be done memorising some sort of information collected during the solution. If this occurs, then the
dynamic programming can be used.


Also there is an approach to solve a problem by using dynamic prograaming in which the result of computation done till now is stored and used in the further
iterations to avoid re-calculation of the same result. Thus the recomputation is preserved. To store the results, we need to have additional space.



Solve the problem first using brute force approach. No harm in this. At least the problem gets solved.
Then focus on optimisation.

For optimization, you have to perform pre-processing of input so that the further logic can work in less time.
This pre-processing can be like sorting, searching or creating some additional data structure to work later.


For dynamic programming, thinking must be done from last to first. That is think like if nth item is part of the optimal solution or not. Then try to find the recursive solution. This will give better and quick break up. Refer to Activity scheduling problem