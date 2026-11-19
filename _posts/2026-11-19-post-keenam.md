---
layout: post
title: Post keenam
date: 2026-11-19 11:30:00 +0700
---
This post shows a formula rendered with MathJax and a short Python example.

The quadratic formula solves equations of the form $ax^2 + bx + c = 0$:

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

This Python function calculates the two real solutions:

```python
import math

def solve_quadratic(a, b, c):
    d = b**2 - 4*a*c

    if d < 0:
        return "No real solutions"

    return (
        (-b + math.sqrt(d)) / (2*a),
        (-b - math.sqrt(d)) / (2*a)
    )

print(solve_quadratic(1, -5, 6))


Gunakan kolom **Date** di Decap untuk tanggal post. Setelah menyimpan dan menerbitkan, rumus akan dirender MathJax dan kode Python tampil sebagai blok kode.
