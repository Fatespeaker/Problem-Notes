Rating: 2000

I solved this in my calculus class. Took maybe 5 minutes to headsolve

This problem is very simple. To fix a node, we need to fix its children. Sometimes, when we fix a child, it will cause a path down to other children. The path will commence at some node where the sum of the children values exceeds the value of the node.

Simply, we can make a path down to depth d with the number of times equal to the sum of the children values minus the sum of the node at depth d value (for all nodes in subtree of depth d). We can store the totals in a vector of maps for each d and subtree root. We can take a path to a leaf as often as we want. 

We can small to large merge with the map and store the set of the depths we can make a path to. Now, we just always take the earliest depth possible if our child sum is too small and subtract however much we use each depth.

I made several rejected submissions:
- Accidentally multiplied the occurrences of depth taken by the number of nodes on the path when subtracting
- Added to my sentinel values. Needed extra check for 67676767
- int vs long long

