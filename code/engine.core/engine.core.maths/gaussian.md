---
description: Engine.Core.Maths
---

# Gaussian Class

The Gaussian class is a class that performs a Gaussian elimination on a matrix and its augmentation.

`public class Gaussian` This is the main Gaussian class.

`public class GaussianResult` This is an inner class that contains the result of the Gaussian elimination.

`public List<float> results` A list that contains the results of the Gaussian elimination.

`public Straight straight` A Straight object that represents a straight.

`public Plane plane` A Plane object that represents a plane.

`public static bool Elimination(Matrix matrix, Matrix augmentation, out GaussianResult result)` This is the main method of the Gaussian class. It takes a matrix and its augmentation and returns the results of the Gaussian elimination.

* The method starts by initializing the GaussianResult object and setting the results list, plane, and straight to null.
* Then, it checks if the matrix and its augmentation have the same number of rows and if the augmentation has only one column.
* If the matrix and its augmentation are in the correct format, the method performs partial pivoting and scaling on the matrix and its augmentation.
* After pivoting and scaling, the method performs elimination on the matrix and its augmentation.
* After elimination, the method checks if the system of equations is consistent by back-substituting and checking the results against the augmentation.
* If the system of equations is consistent, the method returns true and the GaussianResult object contains the results of the Gaussian elimination.
* If the system of equations is not consistent, the method returns false and the GaussianResult object does not contain any results.
