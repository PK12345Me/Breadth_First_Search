The purpose behind this code was to learn and demonstrate Breadth First Search(BFS) and traverse from point a to point b inside of a 3x3 matrix as given below:
grid = [[1, 2, 3], 
        [4, 5, 6], 
        [7, 8, 9]]

The code employs a Breadth-First Search (BFS) algorithm, utilizing a FIFO queue and an explored set. The Explored set ensures that the code does not enter an infinite loop by revisiting the same node repeatedly. The FIFO queue determines the order in which nodes are explored next.

![image](https://github.com/user-attachments/assets/3224bc5a-de07-4965-9820-5fe791633757)

Suppose we want to travel from '9' to '1', and the only available movements are Up, Down, Left, and Right. Starting from 9, the FIFO queue initially contains [6, 8] (represented as a list for easy value unpacking). Only 6 and 8 are selected because 9 is at the corner with no other movement options (no diagonal movements allowed). With this step, 9 is added to the Explored set.

Out of 6 and 8, we expand (explore the neighbors) of 6 first because BFS uses a FIFO strategy. Exploring node 6 and adding it to the Explored set gives us a new frontier of [3, 5, 9]. We then add these to the FIFO queue, which now becomes [8, 3, 5, 9]. The code then moves to 8 (the next in the FIFO queue), adding [5, 7, 9] to the FIFO queue and 8 to the Explored set.

This process continues until the currently expanded value from the FIFO queue matches the target, i.e., 1, at which point the code execution stops.

This traversal can be visualized in the form of the following table:

![image](https://github.com/user-attachments/assets/9435fe89-e7a9-47e6-abce-8955f5b75252)

Please note - the FIFO Queue stores all nodes, regardless of whether they have been explored or not. However, during expansion, nodes are checked for exploration status to avoid revisiting them.
