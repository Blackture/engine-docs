---
description: 'Namespace: Engine.Core.Maths'
---

# Vector Class

Summary

The `Vector` class represents a mathematical vector in 3-dimensional space. It provides various methods and operator overloads to perform operations on vectors such as addition, subtraction, dot product, cross product, normalization, and more.

#### Properties

* `X1`: A float value representing the x1 component of the vector.
* `X2`: A float value representing the x2 component of the vector.
* `X3`: A float value representing the x3 component of the vector.
* `Length`: A readonly float value representing the magnitude (length) of the vector.
* `LengthSquared`: A readonly float value representing the magnitude squared of the vector.
* `Normalized`: A readonly `Vector` instance representing the normalized form of the vector.

#### Indexer

The class has an indexer property that allows you to access the x1, x2, and x3 components of the vector by using an integer index (0, 1, 2).

#### Static Properties

* `Zero`: A readonly `Vector` instance representing the zero vector $$\mathbf{\vec{0}}=\begin{pmatrix} 0 \\ 0 \\ 0\end{pmatrix}$$.
* `One`: A readonly `Vector` instance representing the vector $$\mathbf{\vec {1}}=\begin{pmatrix} 1 \\ 1 \\ 1\end{pmatrix}$$.

#### Constructors

* `Vector(float x1, float x2, float x3)`: Constructs a new `Vector` instance with the given x1, x2, and x3 components.
* `Vector(Vector vector)`: Constructs a new `Vector` instance with the components of the given `Vector` instance.

#### Operator Overloads

* `+`: Adds two vectors together.\
  Let Let $$\mathbf{\vec{v_1}} = \begin{pmatrix} v_{1,1} \\ v_{1,2} \\ v_{1,3}\end{pmatrix}$$and $$\mathbf{\vec{v_2}} = \begin{pmatrix} v_{2,1} \\ v_{2,2} \\ v_{2,3}\end{pmatrix}$$be a 3-dimensional vector. The difference of two vectors is defined as the following operation: $$\mathbf{\vec{v_1}}+\mathbf{\vec{v_2}}=\begin{pmatrix}v_{1,1}+v_{2,1} \\ v_{1,2}+v_{2,2} \\v_{1,3}+v_{2,3}\end{pmatrix}$$
* `-`: Subtracts one vector from another.\
  Let Let $$\mathbf{\vec{v_1}} = \begin{pmatrix} v_{1,1} \\ v_{1,2} \\ v_{1,3}\end{pmatrix}$$and $$\mathbf{\vec{v_2}} = \begin{pmatrix} v_{2,1} \\ v_{2,2} \\ v_{2,3}\end{pmatrix}$$be a 3-dimensional vector. The difference of two vectors is defined as the following operation: $$\mathbf{\vec{v_1}}-\mathbf{\vec{v_2}}=\begin{pmatrix}v_{1,1}-v_{2,1} \\ v_{1,2}-v_{2,2} \\v_{1,3}-v_{2,3}\end{pmatrix}$$
* `*`: Multiplies a vector by a scalar or a vector by a vector.&#x20;
  * **Vector by Scalar**\
    Let $$\mathbf{\vec{v}} = \begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix}$$ be a 3-dimensional vector and $$f,f\in \mathbb{R}$$ be a scalar. The scalar multiplication of a vector is defined as the following operation:$$f \cdot \mathbf{\vec{v}} = \begin{pmatrix} f\cdot v_1 \\ f\cdot v_2 \\ f\cdot v_3 \end{pmatrix}$$
  * **Vector by Vector**\
    Let $$\mathbf{\vec{v_1}} = \begin{pmatrix} v_{1,1} \\ v_{1,2} \\ v_{1,3}\end{pmatrix}$$and $$\mathbf{\vec{v_2}} = \begin{pmatrix} v_{2,1} \\ v_{2,2} \\ v_{2,3}\end{pmatrix}$$be a 3-dimensional vector. The dot product of a vector is defined as the following operation $$\mathbf{\vec{v_1}}\cdot \mathbf{\vec{v_2}} = v_{1,1}\cdot v_{2,1} + v_{1,2}\cdot v_{2,2} + v_{1,3}\cdot v_{2,3}$$
* `/`: Divides a vector by a scalar. _(Multiplies the vector by the reciprocal of the scalar defined by_ $$\mathbf{r} = \frac{1}{s}$$_where_ `r` _is the reciprocal of the scalar_ `s`)

#### Static Methods

* `CrossProduct(Vector u, Vector v)`: Computes the cross product of two vectors.\
  Let $$\mathbf{\vec{u}} = \begin{pmatrix} u_1 \\ u_2 \\ u_3 \end{pmatrix}$$and $$\mathbf{\vec{v}} = \begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix}$$be a 3-dimensional vector. The cross product of a vector is defined as the following operation: $$\mathbf{\vec{u}} \times \mathbf{\vec{v}}=\begin{pmatrix}u_2\cdot v_3-u_3\cdot v_2 \\ u_3\cdot v_1-u_1\cdot v_3 \\ u_1\cdot v_2-u_2\cdot v_1\end{pmatrix}$$\

* `DotProduct(Vector u, Vector v)`: Computes the dot product of two vectors.
* `Normalize(Vector v)`: Normalizes a given vector by executing the `Normalize()` method of the given vector.
* `GetLength(Vector v)`: Gets the length of a given vector using the `v.GetLength()`
*   `AngleBetween(Vector a, Vector b)`: Gets the angle between two vectors in degrees.\
    Let \mathbf{\vec{a\}} and \mathbf{\vec{b\}} be a 3-dimensional vector and l\_a and l\_b their length. The angle between \mathbf{\vec{a\}} and \mathbf{\vec{b\}} is defined as the following operation: $$\alpha = \large{\frac{\small{\arccos}(\frac{\small{\mathbf{\vec{a}}\cdot \mathbf{\vec{b}}}}{\small{||\mathbf{\vec{a}}||} \cdot ||\mathbf{\vec{b}}||}) \cdot 180^\circ}{\small{\pi}}}$$


* `OrthogonalityCheck(Vector a, Vector b)`: Checks if two vectors are orthogonal.\
  Returns true if $$\mathbf{\vec{a}}\cdot \mathbf{\vec{b}}=0$$ -> Vectors are orthogonal if the dot product results 0.

#### Instance Methods

* `Normalize()`: Normalizes the current `Vector` instance by using the `CalculateNormalization()` method and returning the Normalized property.\

* `GetLength()`: Gets the length of the current `Vector` instance.\
  Let $$l,l\in \mathbb{R}$$ be a scalar representing the length of vector $$\mathbf{\vec{v}}=\begin{pmatrix}v_1 \\ v_2 \\ v_3\end{pmatrix}$$. The length $$l$$ of $$\mathbf{\vec{v}}$$ is defined as the following operation: $$l=\sqrt{v_1^2+v_2^2+v_3^2}$$
* `CalculateNormalization()`: Calculates the normalization of the current `Vector` instance.\
  Let current `Vector` instance be a 3-dimensional vector $$\mathbf{\vec{v}} = \begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix}$$. The normalized vector is defined as the following: $$\mathbf{\vec{n}}=\mathbf{\vec{v}}\cdot \large{\frac{1}{l}}$$where $$l$$ is the length of the vector $$\mathbf{\vec{n}}$$.
