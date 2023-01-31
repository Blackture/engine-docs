---
description: Engine.Core.Maths
---

# Plane Class

Summary

This class represents a plane in 3D space. A plane is defined by its normal vector `n` and a position vector `p` which lies on the plane, as well as its `b` value, which is the value of the constant in the equation $$n_1\cdot x_1+n_2\cdot x_2+n_3\cdot x_3-b=0$$ that represents the plane.

### Properties

* `Vector N`: The normal vector of the plane.
* `Vector P`: A position vector on the plane.
* `float B`: The `b` value of the equation $$n_1\cdot x_1+n_2\cdot x_2+n_3\cdot x_3-b=0$$ representing the plane.

### Constructors

* `Plane(Vector n, float b)`: Creates a plane with a normal vector `n` and a constant `b` such that $$n_1\cdot x_1+n_2\cdot x_2+n_3\cdot x_3-b=0$$ represents the plane.
* `Plane(Vector p1, Vector s1, Vector s2, PlaneSetupType setupType)`: Creates a plane with a position vector `p1`, span vectors `s1`, `s2`, and a `setupType` that determines how the plane is constructed.
* `Plane(Vector p, Vector n)`: Creates a plane with a normal vector `n` and a position vector `p` on the plane.

### Methods

* `GetPoint_00X()`: Gets a point on the plane with X1 = 0, X2 = 0 and X3 = b/n3.
* `Contains(Vector v)`: Returns `true` if the vector `v` lies on the plane, `false` otherwise.
* `Contains(Straight s)`: Returns `true` if the straight `s` lies on the plane, `false` otherwise.
* `GetPositionVectorAt(float s1, float s2)`: Gets the position vector of a point on the plane defined by `s1` and `s2`.
* `Intersects(Plane plane, Straight line)`: Returns `true` if the plane intersects with another plane `plane` along a straight `line`, `false` otherwise.
* `Intersection(Plane p1, Plane p2, out Straight s, out Plane p, out Vector v)`: Gets the intersection between two planes `p1` and `p2` and outputs the results as a straight `s`, a plane `p`, and a vector `v`. Returns `true` if the intersection is not empty, `false` otherwise.

### Enums

* `PlaneSetupType`: Specifies the setup type for creating a plane. It has two values: `_3PositionVectors` and `_1PositionVector2SpanVectors`.
