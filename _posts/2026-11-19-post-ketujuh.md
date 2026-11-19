---
layout: post
title: Post keTujuh
date: 2026-11-19 12:10:00 +0700
categories: Algebra
---
Quadratic equations appear in many areas of mathematics. A quadratic equation has the form

$$
ax^2 + bx + c = 0,
$$

where $a$, $b$, and $c$ are constants, and $a \ne 0$.

## The quadratic formula

The solutions can be found with the quadratic formula:

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}.
$$

The expression under the square root, $b^2 - 4ac$, is called the **discriminant**. If it is negative, the equation has no real solutions.

## A Python example

The function below calculates the real solutions. It returns `None` when there are no real solutions.

```python
import math

def solve_quadratic(a, b, c):
    discriminant = b**2 - 4*a*c

    if discriminant < 0:
        return None

    first = (-b + math.sqrt(discriminant)) / (2*a)
    second = (-b - math.sqrt(discriminant)) / (2*a)

    return first, second


solutions = solve_quadratic(1, -5, 6)
print(solutions)
```

The output is `(3.0, 2.0)`. This means that the equation

$$
x^2 - 5x + 6 = 0
$$

has two solutions: $x = 3$ and $x = 2$. Substituting either value into the equation makes the left-hand side equal to zero.
