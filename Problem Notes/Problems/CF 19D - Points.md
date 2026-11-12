Rating: 2800

This was my first purple rated solve on Luogu. When I first read it, I thought it must be 2D segment tree due to the rating on both platforms.

I could not get my 2D segment tree approach to pass due to constant factor even with many optimizations. After beginning to think of a new approach, I got it almost instantly. The solution was trivial.

We can store the highest point at each x coordinate. Then, we can use range maximum segment tree + binary search (or segment tree walk) to find the closest point to our given x coordinate in the query that has a great enough maximum y. Then, we can look at all of the y coordinates of points at that x value and use binary search to find the closest one greater than the given one in the query.

We can use coordinate compression and offline answering to avoid sparse tree. We can use filler values for remove query.