Rating: 2000

Did not enjoy this problem.

Did this after doing some CSES. I right away made the observation about no 2 adjacent nodes being good.

If we have a good set, we can set everything else to 1. Then we just set the good nodes to the sum of their neighbors.

The only issue was the assignment. At first, I tried some naive strategies but realized they wouldn't work. After this, I realized it was clearly some DP but didn't want to mess with it any more.

We can write DP involving finding maximum number of nodes and minimum sum of weights if that maximum is achieved if a node is a good or not good node. A good node must have all children be not good. For a not good node, we can choose the better between good and not good for children. We can use pairs for this, but negate one of the values so it compares max for first and min for second.

Then, we can use our calculated DP to determine whether we should make nodes good or not, based on the optimal path to the root
