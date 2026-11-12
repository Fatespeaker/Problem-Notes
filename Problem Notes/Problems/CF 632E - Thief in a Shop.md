Rating: 2400

First ever application of FFT!

The problem is fairly simple, solved at school.

We can simplify this problem to: given 2 sets, find all possible sums of one element from first set with another from second set. Then, we can just use binary power to extend for k>2.
This subproblem can be solved with FFT. We can make the items in the set the exponent of each term, then repeatedly multiply the polynomial with itself.