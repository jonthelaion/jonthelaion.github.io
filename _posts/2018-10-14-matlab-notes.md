---
layout: post
title: MATLAB Notes
date: 2018-10-14 11:40
description:
categories:
 - matlab
tags:
---

MATLAB is a numerical computing environment commonly used by engineers and scientists. I'll be needing it next semester for some of my subjects, so just getting a bit of a head-start at the moment by working through some freely available training material. Here are some of my notes:

## MATLAB Basics

* General actions:
  * `clear`: clear variables
  * `clc`: clear command window
* Creating matrix:
  * `x = [a b c;d e f]`: creates a 2 x 3 row matric with `;` used to start a new row
  * `x = a:b`: creates a row matrix from a to b
  * `x = a:z:b`: creates a row matrix from a to b by step z
  * `x = linspace(a,b,n)`: creates a row matrix from a to b with n elements
* Transpose:
  * `x = x'`: transpose x
  * `x = (a:z:b)'`: create column vector by step z (since the transpose of a row vector is a column vector)
* Generating matrix of random values / zeros:
  * `x = rand(n)`: creates a n x n matrix with random values
  * `x = rand(m,n)`: creates a m x n matrix with random values
  * `x = zeros(m,n)`: creates a m x n matrix with zeros
* Saving and loading variables to/from files
  * `save data_file.mat var_name`
  * `load data_file.mat`
* Indexing into arrays
  * `x = m(row,col)`: select individual value in an array
  * `x = m(end, end-1)`: `end` can be used to select the last row/column
  * `x = m(row,:)`: to select a row
  * `x = m(:,col)`: to select a column
* Indexing into vectors
  * `x = v(n)`: select nth element in vectors
* Array operations on vectors
  * Scalar addition: `v_add = v1 + 2`
  * Adding vectors together: `v_sum = v1 + v2`
  * Scalar division: `v_div = v1 / 2`
* Basic functions on vectors
  * `max`
  * `round`
  * `mean`
  * `size`
* Multiplying vectors
  * Element-wise multiplication: `z = [3 4] .* [10 20]`
* Multiple assignment
  * `[dr,dc] = size(m)`: assigning outputs of size() to dr and dc respectively
  * `[vMax, ivMax] = max(v)`: when max is called with two variables, it will return the max into the first nd then the index into the second
* Plotting vectors
  * `plot(x,y)`: basic plotting function
  * `plot(x,y,'r--o','LineWidth',3)`: plot and specify colour, line type, marker type and other arguments such as line width. Note that additional arguments such as `LineWidth` got at the end.
  * `hold on`: allows for plotting of multiple lines onto same plot
  * `hold off`: stops `hold on`
  * `close all`: closes all plots
  * `title('title')`: sets title of graph
  * `xlabel('time')`: labelling x-axis
  * `ylabel('distance')`: labelling y-axis
* __Live scripts__ are the MATLAB equivalent of Jupyter notebooks and R markdown, allowing for the creation of a single document containing code, outputs and explanatory text. These can then be shared with other people in a variety of formats. For users who have MATLAB, `.m` is just the code while `.mlx` contains codes along with outputs any explanatory text. For users who do not have MATLAB, live scripts can also be exported to `.pdf` or `.html` format as well.
* __Logical operators__ such as `>`, `>=`, `<`, `<=`, `==`, `~=` can be combined with `&`, `|` to be used for comparisons.
* __Logical arrays__ can be used as an array index, to extract all elements based on a certain condition. Some examples of how this can be used:
  * The following will extract all elements in `v1` that are greater than `6`: `v = v1(v1 > 6)`.
  * To modify `v1` so that any value greater than `5` is replaced with the value `10`: `v1(v1 > 5) = 10`
* __Conditional operators__ such as `if`, `then`, `else` also exist in MATLAB.

```
x = rand;
if x > 0.5
  y = 3;
else
  y = 4;
end
```

* __Loops__ also exist in MATLAB.

```
for i = 1:3
  disp(i)
end
```

## Linear Algebra

* Write in the form `Ax = b` where `A` is the coefficient matrix and `b` is the constant vector.
* The backslash operator (`\`) can be used to compute the solution to systems of linear equations: `x = A\b`.
* `linsolve(A,b)`: same as above
* An __overdetermined system__ of equations is one where there are more equations then there are unknowns. An example of this is where there are three straight lines on a 2D plane (2 variable plane) intersecting at 3 different points. MATLAB will return the best solution using least squares, but will not give you all three intersection points.


## Sources

* [MATLAB Academy](https://matlabacademy.mathworks.com/)
  * MATLAB Onramp - 100%
  * Introduction to Linear Algebra with MATLAB - 48%
