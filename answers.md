# CMPS 2200 Assignment 3
## Answers

**Name:**Andrew Zimmerman


Place all written answers from `assignment-03.md` here for easier grading.

1a. To produce as few coins as possible that sum to n dollars using a greedy algorithm with denominations of powers of 2, we should start with the largest domination of coin that is less than or equal to n, and subtract the value of this chosen coin from n until n becomes 0. We are choosing the highest denomination of k where 2^k is <= N, and subtracting it from N until N becomes 0.

1b. This algorithm is optimal because it adopts a greedy strategy, as it selects the maximum possible number of the largest 2^k denomination coins before transitioning to the next denomination. By prioritizing the largest denominations, it minimizes the total count of coins needed to represent the amount. Each of the steps introduce a new problem of deducting the next largest 2^k denomination, which ensures that the process addresses each subproblem optimally. This approach effectively reduces the frequency of coin selections, optimizing the overall solution.

1c. Work and span are both O(logn)

2a. A simple counterexample demonstrating that the greedy algorithm does not always produce the fewest number of coins in Fortuito would be a scenario where the available denominations in Fortuito are 1,3, and 4 and we need to make change for 6. Using the greedy algorithm, the first selected denomination that is less than or equal to the target amount is 4. Then we would be left with 6-4 = 2, for which the largest denomination less than or equal to 2 is 1. So the greedy algorithm will select two 4 coins. A more optimal solution would be to use one $4 coin and one $1 coin, which totals 2 coins instead of 3 from the greedy algorithm. 


2b. The optimal substructure property of this problem states that an optimal solution to making change for a given amount can be constructed from optimal solutions to its subproblems. The optimal substructure property becomes evident when considering the minimum coins required to make change from 0 to N dollars in this problem. Employing a bottom-up algorithm to calculate these quantities can greatly streamline the process of determining the minimum coins needed for any specified amount.


2c. The work is O(nk), where n is the amount and k is the number of denominations.
The span will be O(n), as we can computer each subproblem independently
