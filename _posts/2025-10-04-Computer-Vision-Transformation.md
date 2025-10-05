---
title: 'Computer Vision - Transformation'
mathjax: true
date: 2025-10-04
permalink: /posts/2025/10/blog-post-1/
tags:
  - Computer Vision
  - Transformation
---

# Geometric Primitives and Transformations

## 2D Points

In 2D space, a pixel coordinate of an image is:

$$
\mathbf{x} = 
\begin{bmatrix}
x \\
y
\end{bmatrix}
$$

---

### Homogeneous Coordinates

If the direction is the same and only the scale differs, it is called a **homogeneous coordinate**.

$$
\tilde{\mathbf{x}} = (\tilde{x}, \tilde{y}, \tilde{w})
$$

If
$$
\mathbb{P}^2 = \mathbb{R}^3 - (0,0,0)
$$

this represents the **2D projective space**, where all points with the same direction are equivalent.

---

### Augmented Vector

$$
\tilde{\mathbf{x}} = (\tilde{x}, \tilde{y}, \tilde{w}) 
= \tilde{w}(x, y, 1) 
= \tilde{w}\bar{\mathbf{x}}
$$

At this equation,

$$
\bar{\mathbf{x}} = (x, y, 1)
$$

is the **Augmented Vector**.

**Exception:**  
When $\tilde{w} = 0$, there is no equivalent inhomogeneous representation.  
Also, $\tilde{w} = 0$ corresponds to **Ideal Points (Points at Infinity)**.

---

## 2D Lines

When  
$$
\tilde{\mathbf{l}} = (a, b, c),
$$  
the line equation is:

$$
\bar{\mathbf{x}} \cdot \tilde{\mathbf{l}} = ax + by + c = 0
$$

---

### Normalized Line Equation

$$
\mathbf{l} = (\hat{n}_x, \hat{n}_y, d) = (\hat{\mathbf{n}}, d), \quad \|\hat{\mathbf{n}}\| = 1
$$

Here,  
- $\hat{\mathbf{n}}$ is the **normal vector**, perpendicular to the line.  
- $d$ is the **distance from the origin**.

**Exception:**  
When $\tilde{\mathbf{l}} = (0,0,1)$, since this includes all ideal points, it cannot be normalized.  
This $\tilde{\mathbf{l}}$ is called the **line at infinity**.

<img width="612" height="233" alt="image" src="https://github.com/user-attachments/assets/5f7be454-d932-4980-8ded-b66dad83ed94" />

