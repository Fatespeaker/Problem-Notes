Rating: 2200

Took me <5 minutes to headsolve and about 30 minutes total to AC. I'm tired after school and can't think straight

This problem is very simple. If we consider all nodes at some depth as an array, the node u in our query limits us to some interval of this array. To find the bounds of this interval, we can use Euler tour + binary search. Use Euler tour to get in/out times for nodes and binary search on first node with later in time than parent and last node with earlier out time than parent (at that depth)

Within this interval, we simply use prefix XOR. We can make a bitset $b$ where $b_i$ is $1$ if the number of occurences of the $i$th character is odd and $0$ otherwise. Now, we can use a similar technique to prefix sums to find the XOR of all the bitsets in the interval. If the popcount is $\leq 1$, we can make a palindrome. All but one frequency must be even to form a palindrome

I made one rejected submission:
- Forgot to call Euler tour function