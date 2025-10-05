---
title: 'Computer Vision - Transformation(2)'
mathjax: true
date: 2025-10-04
permalink: /posts/2025/10/blog-post-2/
tags:
  - Computer Vision
  - Transformation
---

# Geometric Primitives and Transformations

## $n$ as $\theta$

We can express $n$ as a function of $\theta$

$$
\hat{n} = (\hat{n_x}, \hat{n_y}) =(cos \theta,sin \theta)
$$

This is going to be used in **Hough Transformation** when we calculate accumulator's voting.
$(\theta , d)$ is also known as **Polar Coordinate**

---

### Intersection of Lines
We can compute the intersection point of two lines:


$$
\tilde{\mathbf{x}} = \tilde{l_1} \times \tilde{l_2}
$$

Also, the line that passes two points is:

$$
\tilde{l} = \tilde{x_1} \times \tilde{x_2}
$$

---

### 3D points

Points in 3D int homogeneous coordinate:

$$
\mathbf{x} = (x,y,z) \in \mathbf{R^3} 
$$

In homogeneous coordinates:

$$
\tilde{\mathbf{x}} = (\tilde{x}, \tilde{y}, \tilde{z}, \tilde{w}) \in \mathbf{P^3}
$$

In Augmented vector:

$$
\bar{\mathbf{x}} = (x,y,z,1)
$$
with $\tilde{\mathbf{x}} = w \bar{x}$ 

<img width="381" height="195" alt="image" src="https://github.com/user-attachments/assets/744b3d8d-acb9-4722-919a-9108652c5110" />

---

## 3D Planes

3D Planes with $\tilde{\mathbf{m}} = (a,b,c,d)$ in plane equation is:

$$
\bar{\mathbf{x}} \cdot \tilde{\mathbf{m}} = ax + by + cz + d = 0
$$  

When we normalize $\mathbf{m} =(\hat{m_x} , \hat{m_y}, \hat{m_x}, d) = (\hat{\mathbf{m}}, d)$:

$$
\hat{\mathbf{n}} = (cos \theta cos \phi, sin \theta cos \phi, sin \phi)
$$

Exception:
$\tilde{\mathbf{m}} = (0,0,0,1)$ cannot be normalized as this is **Plane at Infinity**.

---

### 3D Lines

In 3D, we can write the line when it can be represented with $(p,q)$:

$$
\mathbf{r} = (1- \lambda) \mathbf{p} - \lambda \mathbf{q}
$$

