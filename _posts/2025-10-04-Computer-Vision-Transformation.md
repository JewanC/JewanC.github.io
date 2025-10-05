---
title: 'Computer Vision - Transformation'
date: 2025-10-04
permalink: /posts/2025/10/blog-post-1/
tags:
  - Computer Vision
  - Transformation
---
Geometric primitives and transformations
======
2D points
------
In 2D space, A pixel coordinate of an image is:
  $x = \begin{bmatrix} x\\y \end{bmatrix}

Homogeneous coordintate:
  If direction is same, only sclale is different, it is called as **Homogeneous Coordinate**

if $P^2 = R^3 -(0,0,0)$
  This is 2D projective Image which has same direction each other.
Augment vector:
  $\tilde{X} = (\tilde x, \tilde y, \tilde w) =\tilde w(\tilde x, \tilde y, 1) = \tilde w \tilde x$
  At this equation,
    $\bar x = (x,y,1) is **Augmented Vector**
  Exception!
    When $\tilde w = 0$, There is no possibility to have equivalent inhomogeneous representation.
    Also, $\tilde w = 0$ is called **Ideal Point/Points at Infinity**.

  2D Lines
  ------
    When $\tilde I = (a,b,c)$, Line equation is:
      $\bar x \cdot \tilte l = ax+by+c=0$ 
    Normalized Line Equation:
      $I=(\hat{n_x}, \hat{n_y}, d) = (\hat n, d), where $||n|| =1$
      $n =$ **Normal Vector**, which is perpendicular to the line 
      $d =$ Distance from origin
    Exception!
      When $\tilde I = (0,0,1)$, as this includes all ideal points, there is no possibility to have normalized line equation.
      $\tilde I$ is line at infinity.
      



