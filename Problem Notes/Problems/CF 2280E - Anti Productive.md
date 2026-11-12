Rating: ???

Obviously, we care about the maximum and the second maximum. We want to reduce the maximum element to something, and cap everything else at something else. The main observation here is that due to small l, we can check all divisors of l in $\sqrt{l}$ complexity, resulting in $O(n + \sqrt{l})$ complexity per test case. We can use prefix sums and two pointers to find the change needed.

I also applied ranges::sort and ranges::reverse for the first time, as suggested by my IDE.