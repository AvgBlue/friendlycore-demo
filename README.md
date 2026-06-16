# FriendlyCore q(c) Demo

A tiny interactive page for understanding the simplified FriendlyCore keep probability `q(c)`.

- `n` is the dataset size.
- `c` is the number of friends a selected point has.
- `q(c)` is the probability that the point is kept in the FriendlyCore.

The demo shows the simplified rule from the lecture:

```text
q(c) = 0, if c <= n/2
q(c) = 1, if c = n
q(c) rises smoothly between n/2 and n
```

The page includes a toggle for several possible smooth shapes between `n/2`
and `n`:

- Linear: `q(c) = t`
- Smoothstep: `q(c) = 3t^2 - 2t^3`
- Slow start: `q(c) = t^2`
- Fast start: `q(c) = sqrt(t)`

where `t = (c - n/2) / (n - n/2)`.

Published with GitHub Pages.

## Point playground

The repo also includes `playground.html`, an interactive FriendlyCore point demo.
Users can add and drag points, choose the friend radius, and run randomized
FriendlyCore filtering repeatedly to see which points enter the core.
