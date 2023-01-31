---
description: Engine.Core.Maths
---

# Straight Class

Summary

The `Straight` class represents a straight line in 3D space.

* `public enum LineSetupType`: The `LineSetupType` is an enumeration that defines the possible ways to set up a straight line in the program, either by two points or by one point and a direction vector.

#### Properties

* `OA`: Represents the endpoint of the line.
* `OB`: Represents the endpoint of the line.
* `Dir`: Represents the direction of the line.

#### Constructors

* `Straight(Vector OA, Vector OB, LineSetupType setupType)`:  The `Straight` constructor initializes a straight line in 3D space, with `OA` and `OB` as input vectors and `setupType` specifying the type of initialization via the `LineSetupType` enum. The constructor switches between two cases based on the value of `setupType`, either initializing the line using two points or one point and a direction vector.

#### Static Properties

* `x1_Axis`: Represents the x-axis in 3D space.
* `x2_Axis`: Represents the y-axis in 3D space.
* `x3_Axis`: Represents the z-axis in 3D space.

#### Static Methods

* `Intersection(Straight, Straight, out Vector)`: Determines if the line intersects with another line.
* `Distance(Straight g, Straight h, out Vector OG, out Vector OH)`: The `Distance` method calculates the shortest distance between two straight lines `g` and `h` and stores the result in the output parameters `OG` and `OH`.
*   `Distance(Vector a, Straight b, out Vector l)`: The `Distance` method calculates the shortest distance between a vector `a` and a straight line `b` and stores the result in the output parameter `l` (plumb point).



#### Instance Methods

* `GetPointAt(float)`: Returns the point on the line at a given position.\
  Let the method parameter be $$t,t\in \mathbb{R}$$.  The point is being returned as position vector $$\mathbf{\vec{x}}$$, which is defined like this: $$g:\mathbf{\vec{x}}=\mathbf{\vec{a}}+t\cdot \mathbf{\vec{d}}$$ where $$\mathbf{\vec{a}}$$ the supporting vector of $$g$$ and $$\mathbf{\vec{d}}$$ the directional vector of $$g$$ is.
* `Distance(Vector, out Vector)`: Finds the distance between the line and a point in 3D space.
* `Distance(Straight)`: Finds the distance between the line and another line in 3D space.
* `Distance(Straight, out Vector, out Vector)`: Finds the distance between the line and another line in 3D space along with the closest points on both lines to the point of intersection.
