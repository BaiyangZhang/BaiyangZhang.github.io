---
layout: post
title: Lecture Notes on Mathematics in Economics
subtitle: 
date: 2023-10-09
author: Baiyang Zhang
header-img: img/background2.jpg
catalog: true
tags:
 - lectureNote
 - mathematicalEconomics
---

### Syllabus

**Semester**: Fall 2023

**Duration:** 40 Real hours (54 teaching hours), 3 real hours per class, 14 classes / 7 weeks 

**Lecturer**: Dr. Baiyang Zhang

**Office Address:** N/A

**Email**: [byzhang@henu.edu.cn](mailto:james.fisher@henu.edu.cn)

**Lecture Schedule**: Monday and Wednesday, 2:30 - 5:30

**Classroom:** Monday at Teaching building Room 3502, Wednesday at Room 109 at the School of Economics

**Textbooks and References:**

1. “*Fundamental Methods of Mathematical Economics*” by Chiang and Wainwright

2. “*Introduction to Probability*” by Grinstead and Snell

3. "*Introduction to Linear Algebra*" by Strang.

**Course Objectives:**  This course will include the basics of analysis, derivatives and integration, linear algebra, optimization, and probability, with the goal of preparing students for further course work within the School of Economics.

**Assessment Policy:** The assessments for this course will one final, in addition to several homeworks. Each item is scored on a percentage basis. The final score for the class is the weighted sum of the items’ scores.  The weights are as follows: final accounts for 70% of the final grade, and the homeworks account for the remaining 30% of the final grade.

In general, the final grade is an A when the final score is 85% or better, a B when the final score is between 70% and 84.9%, a C when the final score is between 60% and 69.9%, a D when the final score is between 50% and 59.9%, and an F when the final score is below 50%.  Assessment and final grades, however, may be curved to the benefit of the students.

**Tentative Weekly Schedule:**

CW = Chiang and Wainwright, GS = Grinstead and Snell, W = Wooldridge.

Additional review sessions may be scheduled in advance of exams.

|**Lecture**|**Topics**|**Reading**|
|----------|----------|----------|
| 1  | Introduction and Basics of Analysis | CW, Ch. 1 and 2|
| 2-4 | Linear Algebra  | CW, Ch. 4 and 5|
| 5-6 | Derivatives | CW, Ch. 6,7 and 8|
| 7 | Integrals | CW, Ch. 14|
| 8-10 |Unconstrained Optimization | CW, Ch. 9, 10, and 11|
| 11 | Constrained Optimization with Equality Constraints | CW, Ch. 12|
| 12 | Probability Distributions and Combinatorics | GS, Ch. 1, 2 and 3|
| 13 | Common Distributions and Conditional Probability | GS, Ch. 4 and 5|
| 14 | Expected Values | GS, Ch. 6|

- - -

## Lecture 1

**Mathematical Economics versus Econometrics** 

Econometrics is concerned mainly with the measurement of economic data. Hence it deals with the study of empirical observations using statistical methods of estimation and hypothesis testing. Indeed, empirical studies and theoretical analyses are often complementary and mutually reinforcing. On the one hand, theories must be tested against empirical data for validity before they can be applied with confidence. On the other, statistical work needs economic theory as a guide, in order to determine the most relevant and fruitful direction of research.

**Economic Models**

A model is essentially and necessarily an abstraction from the real world. The sensible procedure is to pick out what appeals to our reason to be the primary factors and relationships relevant to our problem and to focus our attention on these alone. 

**Mathematics from a bird's eye view**

Explain: Algebra, Geometry, and Analysis.

Most people who have done some high school mathematics will think of algebra as the sort of mathematics that results when you substitute letters for numbers. Algebra will often be contrasted with arithmetic, which is a more direct study of the numbers themselves. 

There is, however, a different contrast, between algebra and geometry, which is much more important at an advanced level. The high school conception of geometry is that it is the study of `shapes` such as circles, triangles, cubes, and spheres together with concepts such as rotations, reflections, symmetries, and so on. Thus, the objects of geometry, and the processes that they undergo, have a much more visual character than the equations of algebra. 

Some parts of mathematics involve manipulating symbols according to certain rules: for example, a true equation remains true if you “do the same to both sides.” These parts would typically be thought of as algebraic, whereas other parts are concerned with concepts that can be visualized, and these are typically thought of as geometrical.

One is more symbolic and the other more pictorial.

The word “analysis,” used to denote a branch of mathematics, is not one that features at high school level. However, the word “calculus” is much more familiar, and differentiation and integration are good examples of mathematics that would be classified as analysis rather than algebra or geometry. The reason for this is that they involve limiting processes. For example, the derivative of a function f at a point x is the limit of the gradients of a sequence of chords of the graph of $f$ , and the area of a shape with a curved boundary is defined to be the limit of the areas of rectilinear regions that fill up more and more of the shape. 

Thus, as a first approximation, one might say that a branch of mathematics belongs to analysis if it involves limiting processes, whereas it belongs to algebra if you can get to the answer after just a finite sequence of steps.

**Branches of Mathematics**

- Algebra. Deals with number systems, polynomials, and more abstract structures such as groups, fields, vector spaces, and rings. 
- Number theory.
- Algebraic geometry
- Analysis
    - The study of PDE, ODE.
    - Dynamics. What happens when you take a simple process and do it over and over again?
- Logic
	- Set theory
	- Category theory
- Combinatorics
- Theoretical Computer Science
- Probability
- Mathematical Physics

- - -

1. *Math as a language with its own vocabulary and syntax.* 
2. *Introduction of set theory, including the basic concepts and operations that can be done to them.*
3. *Introduce the concept of function and functional. They are nothing but various maps from one set to another.* 
4. The number system. Explain integers, rational numbers, real numbers and complex numbers. $\mathbb{R},\mathbb{N}, \mathbb{Z}, \mathbb{Q}$. 

## Lecture 2


"You can't add apples and oranges." In a strange way, this is the reason for vectors. We have two separate numbers $v_  {1}$ and $v_  {2}$. The pair produces a two-dimensional vector $\vec{v}$. Explain the following concepts:
- column,
- components.

We don't add $v_  {1}$ and $v_  {2}$, but we do add vectors of the same type. Explain vector addition. We want to add apples with apples. 

Explain what is a scalar, and scalar multiplication. 

Given two vectors $\vec{v}$ and $\vec{w}$, explain the linear combination of them. 

This big view, taking all the combinations of $\vec{v}$ and $\vec{w}$, is linear algebra at work.

Illustrate the addition of vectors using arrows.

Introduce 
- dot product,
- length.

The dot product is gonna be needed when defining the action of a matrix on a vector. 

After introducing the product rules in two different ways, we introduce the linear equations. 

### Lecture 3

**Linear combination:**

Imagine you have a collection of building blocks, and each block represents a different item. A "linear combination" is like creating a new structure using these blocks, where you decide:

1. **How many of each block to use**: This is similar to multiplying the block (or item) by a number.
2. **How to combine them**: Essentially, you're just adding these multiplied blocks together.

Let's use a simpler example:

Imagine you have two types of fruit: apples and bananas. 

A "linear combination" of apples and bananas could be:

- 3 apples + 2 bananas
- 5 apples + 1 banana
- 2 apples - 4 bananas (Yes, in mathematics, you can have negative bananas! Just think of it as owing bananas to someone.)

In each of these cases, the number of apples and bananas you decide to use (3, 2, 5, 1, etc.) are called "coefficients". 

When it comes to mathematics and vectors, the idea is the same. You're combining different vectors using certain coefficients to produce a new vector. But the basic idea is just like combining apples and bananas!

- - -

There are many ways to look at a matrix. 

1. **Table of Numbers**: At its core, a matrix is like a table or grid filled with numbers. Think of it like a spreadsheet or a bingo card. Each number sits in its own little box, and these boxes are organized into rows and columns.

2. **Collection of Column Vectors**: Imagine each column in that table as a list of numbers. This list can be seen as a "column vector". So, a matrix can be thought of as a collection of these column vectors, standing side by side. For example, a matrix with three columns is like having three lists (or column vectors) put together.

3. **Collection of Row Vectors**: Similarly, you can think of each row in the matrix as a separate "row vector". So, another way to view a matrix is as a stack of these row vectors, one on top of the other.

4. **Transformation Machine**(we will go to more details in this class): This is a more advanced way to think about matrices, especially in linear algebra. Imagine you have a point on a graph. A matrix can act as a "machine" where you input your point, and out comes a new point. This new point might be stretched, squished, rotated, or even flipped compared to the original. In essence, the matrix transformed it!

5. **System of Equations**(topic of this class too): If you've ever dealt with multiple equations at once (like trying to figure out both the price of a burger and fries when given combined costs), matrices can represent these systems. Each row could represent a different equation, and the numbers in that row represent the coefficients of variables in that equation.

6. **Storage and Organization**: In computer science and data analysis, matrices can be used to store data. For instance, consider ratings given by users to movies on a streaming platform. Each row might represent a user, each column might represent a movie, and the number in a specific box represents the rating that user gave to that movie.

These are just some of the many ways to look at matrices. Depending on the subject (like physics, computer graphics, or economics), matrices might take on other interesting interpretations!

- - -

**The multiplication of matrices**

**The Basics**:

Matrix multiplication is not just multiplying numbers. Instead, it's a combination of multiplication and addition. Remember, the way you multiply matrices is quite different from multiplying regular numbers, so it's essential to understand the steps and rules.

**The Key Rule**:

For two matrices to be multiplied, the number of columns in the first matrix must be equal to the number of rows in the second matrix. This is a crucial rule. 

If Matrix A has dimensions of $m \times n$ (meaning $m$ rows and $n$ columns) and Matrix B has dimensions of $p \times q$ (meaning $p$ rows and $q$ columns), then for A and B to be multipliable, $n$ must equal $p$. The resulting matrix will have dimensions $m \times q$.

**How to Multiply**:

Let's consider two simple matrices:

Matrix A:

$$
\begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix}
$$

Matrix B:

$$
\begin{pmatrix}
2 & 1 \\
0 & 3
\end{pmatrix}
$$


To multiply them:

1. **First element of the result (top-left corner)**:
   - Take the first row of Matrix A: (1, 2).
   - Take the first column of Matrix B: (2, 0).
   - Multiply corresponding elements and add them up: (1×2) + (2×0) = 2.

2. **Second element in the first row (top-right corner)**:
   - Take the first row of Matrix A: (1, 2).
   - Take the second column of Matrix B: (1, 3).
   - Multiply corresponding elements and add them up: (1×1) + (2×3) = 7.

3. **First element in the second row (bottom-left corner)**:
   - Take the second row of Matrix A: (3, 4).
   - Take the first column of Matrix B: (2, 0).
   - Multiply and add: (3×2) + (4×0) = 6.

4. **Second element in the second row (bottom-right corner)**:
   - Take the second row of Matrix A: (3, 4).
   - Take the second column of Matrix B: (1, 3).
   - Multiply and add: (3×1) + (4×3) = 15.

The resulting matrix is:


$$
\begin{pmatrix}
2 & 7 \\
6 & 15
\end{pmatrix}
$$

**Visualization**:

Imagine Matrix A's rows as horizontal hands reaching out, and Matrix B's columns as vertical hands reaching up. When these hands "high-five", they form the elements of the resulting matrix by the rule we just discussed.

**Practice**:

The best way to get comfortable with matrix multiplication is to practice. Start with smaller matrices, understand the patterns, and then work with larger ones.

Remember, the rule of matching columns of the first matrix to rows of the second is crucial. If they don't match, the matrices can't be multiplied.

- - -

### Example: Production in a Shoe Factory

Imagine you run a small shoe factory. You produce two types of shoes: sneakers and boots.

**Vectors**:
1. **Production Vector** for a given week:
   - Sneakers: 100 pairs
   - Boots: 50 pairs

   We can represent this as:
   
   $$
   \text{Shoes} = \begin{bmatrix} 100 \\ 50 \end{bmatrix}
   $$

2. **Cost Vector** for producing each type of shoe:
   - Cost to produce one pair of sneakers: $20
   - Cost to produce one pair of boots: $40

   This can be represented as:
   
   $$
   \text{Cost} = \begin{bmatrix} 20 \\ 40 \end{bmatrix}
   $$

**Matrix**:
Let's say, to produce each shoe, you need two main raw materials: leather and rubber. We can create a **Material Requirement Matrix** that tells us how much of each material is required to produce one unit of each shoe type.

For example:
- Each pair of sneakers requires 1 unit of leather and 2 units of rubber.
- Each pair of boots requires 3 units of leather and 1 unit of rubber.

This matrix is:

$$
\text{Materials} = \begin{bmatrix} 1 & 2 \\ 3 & 1 \end{bmatrix}
$$

Where the first column corresponds to the requirements for sneakers and the second column to boots.

**Matrix Multiplication**:

Now, suppose you want to find out how much raw material (leather and rubber) you'll need for the entire week's production.

To do this, you'd multiply the Material Requirement Matrix by the Production Vector:

$$
\text{Total Materials} = \text{Materials} \times \text{Shoes}
$$

Multiplying, we get:

$$
\text{Total Materials} = \begin{bmatrix} 1 & 2 \\ 3 & 1 \end{bmatrix} \times \begin{bmatrix} 100 \\ 50 \end{bmatrix} = \begin{bmatrix} 200 \\ 350 \end{bmatrix}
$$

So, you'll need:

- 200 units of leather (100 for the sneakers and 150 for the boots)
- 350 units of rubber (200 for the sneakers and 150 for the boots)

This simple example demonstrates the power of vectors and matrices in understanding and organizing economic production.

- - -

Apply the multiplication of matrices to the product of:
1. row vector times column vector,
2. column vector times row vector (this one is strange).

- - -
Certainly! Let's embark on this journey to understand transposes and inverses using clear examples and relatable analogies tailored for students stepping into the realm of mathematical economics.

---

**Transposes**

**What is a Transpose?**
The transpose of a matrix is obtained by flipping the matrix over its main diagonal (the diagonal from the top-left to the bottom-right). In simpler terms, the rows of the matrix become the columns, and the columns become the rows.

**Visual Analogy**: 
Imagine you have a bookshelf full of books (your matrix). If you were to tip that bookshelf onto its side (so that it's lying down), the rows of books would now appear as columns. That's the transpose!

**Example**:
Given the matrix:

$$
A = \begin{bmatrix}
2 & 5 \\
3 & 7 \\
1 & 4 \\
\end{bmatrix}
$$

The transpose, denoted as $A^T$, is:

$$
A^T = \begin{bmatrix}
2 & 3 & 1 \\
5 & 7 & 4 \\
\end{bmatrix}
$$

**In Mathematical Economics**: 
Transposing can be useful for various reasons, such as making certain operations or calculations easier or more intuitive. For instance, when working with data sets or in regression analysis, transposes come in handy.

**Inverses**

**What is an Inverse?**
The inverse of a matrix, if it exists, is a matrix that, when multiplied with the original matrix, results in the identity matrix. The identity matrix is a special square matrix with ones on the main diagonal and zeros elsewhere.

In symbols, for a matrix $A$, its inverse is denoted $A^{-1}$, such that:

$$ A \times A^{-1} = I $$

where $I$ is the identity matrix.

**Real-life Analogy**: 
Think of the process of multiplication and its inverse, division. When you multiply a number by its reciprocal, you get 1. Similarly, in the world of matrices, when you multiply a matrix by its inverse, you get the identity matrix.

**Properties**: 
1. Not all matrices have inverses. Only square matrices (matrices with the same number of rows and columns) have the potential to have an inverse, and even among them, not all do.
2. A matrix that does not have an inverse is called "singular" or "non-invertible". 

**Example**:
For a 2x2 matrix:

$$
A = \begin{bmatrix}
a & b \\
c & d \\
\end{bmatrix}
$$

Its inverse is:

$$
A^{-1} = \frac{1}{ad-bc} \begin{bmatrix}
d & -b \\
-c & a \\
\end{bmatrix}
$$

However, this inverse exists only if $ad-bc$ is not zero. If $ad-bc = 0$, then the matrix is singular and does not have an inverse.

**In Mathematical Economics**: 
The concept of an inverse matrix is fundamental when solving systems of linear equations, which frequently appear in economics. For example, determining equilibrium in markets, analyzing input-output models, or finding solutions to optimization problems often involve the use of matrix inverses.

Both transposes and inverses are fundamental tools in the toolbox of mathematical economics. Just as we learn to add, subtract, multiply, and divide with numbers, we learn operations and manipulations with matrices to understand and solve intricate economic phenomena. As students progress, they'll witness the power and elegance of linear algebra in analyzing economic systems.



- - -

**Square Matrix vs. Non-Square Matrix**

**1. Square Matrix**:
A matrix is called a "square matrix" if it has the same number of rows and columns. In other words, its dimensions look like $n \times n$, where $n$ is a positive integer. You can visualize it as a perfect square filled with numbers, just like a chess or checkerboard.

**Example**: A 2x2 matrix:

$$
\begin{bmatrix}
2 & 5 \\
3 & 7 \\
\end{bmatrix}
$$

**2. Non-Square Matrix**:
Any matrix that doesn't have the same number of rows and columns is a "non-square matrix". Its dimensions might look like $m \times n$, where $m$ and $n$ are positive integers, and $m \neq n$.

**Example**: A 2x3 matrix:

$$
\begin{bmatrix}
1 & 4 & 7 \\
2 & 5 & 8 \\
\end{bmatrix}
$$

---

**Square Matrices are Special in Multiplication.**

When we talk about multiplication in the world of matrices, square matrices have a unique property: they're "closed under multiplication". This might sound fancy, but let's break it down:

**Closed Under Multiplication**: This means that if you multiply two square matrices of the same size, you'll get another square matrix of that same size as the result.

Let's say you have two square matrices, both of size $2 \times 2$. When you multiply them, the resulting matrix will also be $2 \times 2$. This property will hold true no matter how big or small the matrices are, as long as they're square.

**Economic Analogy**: Imagine each square matrix as a factory machine. When a factory machine (a square matrix) processes another machine of the same size (another square matrix), the result is always a new machine of the same dimensions. This predictable outcome allows for consistent planning and operation, making these "machines" reliable and preferred in many scenarios.

**Forming a Nice Algebra**: The fact that square matrices are closed under multiplication means they form a consistent system, or a "nice algebra". In this system, you can perform operations, like multiplication, and always know what kind of result to expect (another square matrix). This consistency is useful in mathematical economics because it provides a stable framework for analysis and predictions.

---

**What is a Linear Equation?**

**Definition**: 
A linear equation is an equation of the form:

$$a_ 1x_ 1 + a_ 2x_ 2 + ... + a_ nx_ n = b$$

where $x_ 1, x_ 2, ... x_ n$ are the variables, $a_ 1, a_ 2, ... a_ n$ are constants (known as coefficients), and $b$ is another constant. 

**Key Features**:

1. Each term consists of a variable multiplied by a constant.
2. No term has a variable raised to a power higher than one.
3. There are no products of variables (e.g., $x_ 1 \times x_ 2$).

**Simple Example**: 

Consider the equation $3x + 2y = 12$. Here, $x$ and $y$ are the variables, and the numbers 3 and 2 are their respective coefficients.

Imagine you're graphing this equation on a coordinate plane. For an equation with two variables, the graph would be a straight line. That's why it's called "linear" – the graph is a line.

**What is a System of Linear Equations?**

**Definition**: 

A system of linear equations is just a collection of two or more linear equations that involve the *same set of variables*.

**Simple Example**:

$$
\begin{align*}
3x + 2y &= 12 \quad \text{(Equation 1)} \\
x - y &= 5 \quad \text{(Equation 2)}
\end{align*}
$$

In this system, you have two linear equations, and you'd typically try to find values for $x$ and $y$ that satisfy both equations simultaneously.

**Graphical Interpretation**:

When you plot both equations on a graph:
1. If they intersect at a point, that point is the solution to the system (i.e., the values of $x$ and $y$ at that point satisfy both equations).
2. If they never meet (parallel lines), the system has no solution.
3. If the two equations represent the same line, then there are infinitely many solutions - any point on that line is a solution.

Such systems help in understanding multiple interdependencies. For instance, if you have a market with two goods, and each equation represents how demand or supply changes based on the price of both goods, the system helps find an equilibrium where both goods' demands are satisfied.

Think of a linear equation as a single straight path (line) and a system of linear equations as multiple paths. Our goal is often to find where these paths meet or if they never do. In the context of economics, these meeting points can represent equilibrium states, optimal solutions, or any scenario where multiple conditions are satisfied at once. As students dive deeper into mathematical economics, they'll see that these simple linear systems can be powerful tools for understanding complex economic relationships.

- - -

Certainly! Let's simplify the concept and lay it out for students transitioning from a high school math background.

---

### **Using Matrices to Represent Equations**

Let's say we have the following system of equations:

$$
\begin{align*}
2x + 3y &= 8 \\
x - 4y &= -3
\end{align*}
$$

This can be represented in a matrix format as $AX = B$:

Where:
$$ A = \begin{bmatrix} 2 & 3 \\ 1 & -4 \end{bmatrix} $$
(Coefficients of the variables)

$$ X = \begin{bmatrix} x \\ y \end{bmatrix} $$

(Our unknowns)

$$ B = \begin{bmatrix} 8 \\ -3 \end{bmatrix} $$

(Results of the equations)

## Lecture 4

### **Solving Using the Inverse**

Here's the magic part: If we multiply both sides of our matrix equation $AX = B$ by the inverse of matrix $A$, which we'll call $A^{-1}$, we can isolate $X$ (our unknowns).

Doing the math:

$$ A^{-1}AX = X = A^{-1}B $$


So, if we can find the inverse of $A$ (remember, not all matrices have inverses!), then we can multiply it with $B$ to get our solution, $X$.

In economics, we often deal with many variables and relationships at the same time. Instead of trying to solve each relationship individually, matrices allow us to represent these complex relationships together and solve them in a more streamlined way. 

For example, imagine you're studying how the price of one product affects the demand for another, and vice versa. Instead of solving each relationship individually, we can group them in a system of equations, represent them as matrices, and solve them all at once.

Using the inverse matrix to solve a system of linear equations is like having a secret decoder ring. It's a powerful tool that can make solving complex problems more manageable. As students dive deeper into mathematical economics, they'll find that these tools, while initially seeming abstract, can be invaluable in understanding and analyzing economic relationships and behaviors.

---

Let's think about 2D space for a moment. We've all seen the classic X-Y coordinate plane. Imagine you've got two vectors (think of them as arrows) on this plane. Sometimes, these two arrows will point in completely different directions. But occasionally, they might just lay flat on top of one another or be exactly opposite.

Now, if we use these vectors as rows or columns in a matrix, the question becomes: Does this matrix have a unique way to revert any transformation it causes? Or in other words, can we find its inverse?

This is where the idea of a matrix being "singular" comes in. A **singular matrix** doesn't have an inverse. Visually, if you were to transform the entire 2D space using a singular matrix, some areas would scrunch up so much that they'd be impossible to revert to their original form.

To figure out if a matrix is singular, we need a tool, and that tool is the **determinant**.

Think of the determinant as a special number associated with a matrix. If the determinant is zero, our matrix is singular (it can't be inverted). If the determinant isn't zero, then the matrix can be inverted.

For our 2x2 matrices (which are often the starting point in learning), the determinant gives us a sense of the "area scaling factor" when the matrix is used for a transformation. If the determinant is zero, it means the matrix squishes everything down to a line or a point, losing all the original area, making it impossible to revert.

For a matrix to be nonsingular (i.e., to have an inverse), each row (like our detectives) has to bring something unique to the table. If even one row is just a repeat or combination of others, it's like missing out on crucial information. And without that unique contribution from every row, we can't find an inverse for our matrix.

****Rank of a Matrix****

The rank of a matrix is a measure of the "dimension" of the linear space spanned by its rows or columns. In simpler terms, it tells us the number of linearly independent rows or columns in the matrix.

*The Library Analogy:*

- Imagine you have a library of books. Some books might be exactly the same, and some might be different.
- If you were asked, "How many unique books do you have?", you would ignore all duplicates and count only the distinct ones.
- The rank of a matrix is similar: It tells us how many "unique" rows (or columns) there are, ignoring any that can be made by combining others.

*Determining Rank:*

1. If a matrix has all zeros, its rank is 0.
2. If a matrix has some non-zero elements but some rows (or columns) are just scalar multiples or combinations of other rows (or columns), its rank will be less than the total number of rows (or columns).
3. If no row (or column) can be expressed as a combination of any other rows (or columns), the matrix is said to have full rank, meaning its rank is equal to the smaller of the number of rows or columns.

---

**Rank of a Matrix:**

The rank of a matrix is a measure of the "dimension" of the linear space spanned by its rows or columns. In simpler terms, it tells us the number of linearly independent rows or columns in the matrix.

**Analogies & Insights:**

1. **The Library Analogy:**
    
    - Imagine you have a library of books. Some books might be exactly the same, and some might be different.
    - If you were asked, "How many unique books do you have?", you would ignore all duplicates and count only the distinct ones.
    - The rank of a matrix is similar: It tells us how many "unique" rows (or columns) there are, ignoring any that can be made by combining others.

---

**Rank of a Matrix:**

The rank of a matrix is a measure of the "dimension" of the linear space spanned by its rows or columns. In simpler terms, it tells us the number of linearly independent rows or columns in the matrix.

**Analogies & Insights:**

1. **The Library Analogy:**
    
    - Imagine you have a library of books. Some books might be exactly the same, and some might be different.
    - If you were asked, "How many unique books do you have?", you would ignore all duplicates and count only the distinct ones.
    - The rank of a matrix is similar: It tells us how many "unique" rows (or columns) there are, ignoring any that can be made by combining others.

**Determinant**:

The term "determinant" was used because it can "determine" whether or not a matrix has an inverse.

Let's say you have a 2x2 matrix:

$$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix} $$

The determinant, often denoted as |A| or det(A), is calculated as:

$$|A| = ad - bc $$

If |A| equals zero, then A is singular.

Introduce the Levi-Civita tensor. Use it to define the determinant. 

Of course! The Laplace Expansion is an important technique for calculating the determinant of a matrix. It's especially useful when we have a matrix larger than $3 \times 3$, though it can be used for smaller matrices as well. The method is essentially a recursive process that breaks down a larger matrix into smaller ones.

**Steps for Laplace Expansion:**

1. **Choosing a Row or Column:**
   You can choose any row or column to expand upon. For the sake of simplicity, we often choose a row or column with the most zeros because it reduces the number of calculations we have to make (since any term multiplied by zero is zero).

2. **Calculate Minors:**
   For each element $a_ {ij}$ of the matrix, remove the i-th row and the j-th column, and compute the determinant of the resulting $(n-1) \times (n-1)$ matrix. This determinant is called the "`minor`" of the element, often denoted $M_ {ij}$.

3. **Calculate Cofactors:**
   Associated with each minor is a cofactor, which is defined as: $C_ {ij} = (-1)^{i+j} \times M_ {ij}$. This alternating sign pattern helps ensure the determinant computation is accurate.

4. **Compute the Determinant:**
   The determinant of the matrix is the sum of the products of the elements of your chosen row or column with their respective cofactors. Mathematically, if you chose the i-th row, this can be written as:
   
$$\text{det}(A) = \sum_ {j=1}^{n} a_ {ij} C_ {ij} $$
   
Alternatively, if you chose the j-th column, it is:

$$\text{det}(A) = \sum_ {i=1}^{n} a_ {ij} C_ {ij} $$

**Example: Determinant of a $3 \times 3$ Matrix using Laplace Expansion:**

Given matrix A:

$$
\begin{pmatrix}
1 & 3 & 2 \\
4 & 1 & 3 \\
2 & 2 & 1 \\
\end{pmatrix}
$$

To compute its determinant, let's expand using the first row:

1. For the element $a_ {11} = 1$:
   - Minor $M_ {11}$ is the determinant of:

$$
\begin{pmatrix}
1 & 3 \\
2 & 1 \\
\end{pmatrix}
$$

   - $M_ {11} = 1 - 6 = -5$
   - Cofactor $C_ {11} = (-1)^{1+1} \times (-5) = 5$

2. For the element $a_ {12} = 3$:
   - Minor $M_ {12}$ is the determinant of:

$$
\begin{pmatrix}
4 & 3 \\
2 & 1 \\
\end{pmatrix}
$$

   - $M_ {12} = 4 - 6 = -2$
   - Cofactor $C_ {12} = (-1)^{1+2} \times (-2) = 2$

3. For the element $a_ {13} = 2$:
   - Minor $M_ {13}$ is the determinant of:

$$
\begin{pmatrix}
4 & 1 \\
2 & 2 \\
\end{pmatrix}
$$

   - $M_ {13} = 8 - 2 = 6$
   - Cofactor $C_ {13} = (-1)^{1+3} \times 6 = -6$

Combining the results, 

$$\text{det}(A) = 1 \times 5 + 3 \times 2 + 2 \times (-6) = 5 + 6 - 12 = -1 $$

And that's how you can use the Laplace Expansion to compute the determinant of a matrix! This method becomes more cumbersome for larger matrices, but the principles remain the same.

**Properties of determinants**

The addition (subtraction) of a multiple of any row to (from) another row will leave the value of the determinant unaltered. The same holds true if we replace the word row by column in the previous statement. 

*It preserves the multiplication of matrices.* $\left\lvert A \cdot B \right\rvert = \left\lvert A \right\rvert \times \left\lvert B \right\rvert$. 

**Finding the Inverse Matrix**

Introduce the adjoint of a matrix, and then the inverse. 

**Cramer's rule**

Let's break down Cramer's rule into a simple-to-understand explanation.

Imagine you're trying to solve a system of equations. This system might represent different scenarios. For instance, let's say you and a friend are buying apples and bananas. Two different days, two different scenarios:

1. On Monday, you bought 3 apples and 2 bananas, and it cost you $13.
2. On Tuesday, you bought 4 apples and 5 bananas, and it cost you $31.

From this, you have:

1) 3A + 2B = 13
2) 4A + 5B = 31

Where A represents the cost of an apple and B represents the cost of a banana.

Cramer's rule helps you find the cost of A and B using determinants of matrices. 

**Step-by-step with Cramer's Rule:**

1. **Main Determinant (D)**:
2. 
   First, make a matrix of the coefficients of A and B:

$$ 
\begin{pmatrix}
3 & 2 \\
4 & 5 \\
\end{pmatrix}
$$

Calculate its determinant (D). This determinant represents the "base scenario" of our system.

2. **Determinant with respect to A:**
   Replace the first column (which represents apples) with the numbers on the right side of our equations (13 and 31):
   
$$ 
\begin{pmatrix}
13 & 2 \\
31 & 5 \\
\end{pmatrix}
$$

Calculate its determinant. This determinant represents the scenario when we're focusing just on the apples.

3. **Determinant with respect to B**:
   Replace the second column (which represents bananas) with the numbers on the right side:
   
$$ 
\begin{pmatrix}
3 & 13 \\
4 & 31 \\
\end{pmatrix}
$$

Calculate its determinant. This represents the scenario when we're focusing just on the bananas.

4. **Solving for A and B**:
5. 
   - The cost of an apple (A) is found by $A = D_ A / D$
   - The cost of a banana (B) is found by $B = D_ B / D$

This gives you the individual prices of apples and bananas!

**In simple words:** Cramer's rule lets you focus on one variable at a time (like just apples or just bananas) and then combine the results to find out the cost of each. It does this using determinants, which are a special number for matrices, like a fingerprint for the matrix.

Remember, Cramer's rule works best for systems where the number of equations matches the number of unknowns, and the main determinant (D) is not zero. If D were zero, it would be like trying to divide by zero, which we can't do.

**Application**

Let's walk through a simplified example of Input-Output Analysis using a hypothetical economy with just three industries: Agriculture, Manufacturing, and Services.


Imagine the following table showing how each industry's output is used as input by the others:

|                     | To Agriculture | To Manufacturing | To Services | Final Demand |
|---------------------|----------------|------------------|-------------|--------------|
| **From Agriculture**    | 10            | 30               | 10          | 50           |
| **From Manufacturing**  | 20            | 40               | 20          | 20           |
| **From Services**       | 10            | 10               | 30          | 50           |

Each row represents the output of an industry, and each column (excluding the Final Demand column) represents the input to an industry. For example, the number 30 in the 'From Agriculture' row and 'To Manufacturing' column means that the Manufacturing sector uses 30 units of the Agriculture sector's output.

1. **Creating the A matrix (Input-Output Coefficient Matrix):** This matrix is obtained by dividing each element of the table by the total output of the corresponding industry. The total output for each industry is the sum of its outputs to all industries plus its final demand.

   Total output for each sector:
   - Agriculture: 10 + 30 + 10 + 50 = 100
   - Manufacturing: 20 + 40 + 20 + 20 = 100
   - Services: 10 + 10 + 30 + 50 = 100

   Now, construct the A matrix:
   ``` 
   |  0.1  0.3  0.1 |
   |  0.2  0.4  0.2 |
   |  0.1  0.1  0.3 |
   ```

2. **The Leontief Inverse**: To find the total output required to satisfy a given final demand, we use:
   $$ X = (I - A)^{-1} Y $$
   
   Where:
   
   - $X$ is the total output vector.
   - $Y$ is the final demand vector.
   - $I$ is the identity matrix.

   In our case, $Y$ is:
   
   ```
   | 50 |
   | 20 |
   | 50 |
   ```

   And $I$ is:
   
   ```
   | 1  0  0 |
   | 0  1  0 |
   | 0  0  1 |
   ```

   Calculating $(I - A)$, and then finding its inverse can be done using a tool or software that supports matrix operations, such as MATLAB, Python (using NumPy), or even specialized calculators.

3. **Computing the Result**: Once you have the Leontief inverse, you multiply it by the final demand vector $Y$ to get the total output vector $X$.

The resulting $X$ vector will tell you how much each industry needs to produce in total to meet the given final demand, taking into account not just the direct demand for each industry's products, but also the indirect demand generated by the need for inputs from other industries.

In practice, real-world Input-Output tables are much larger and more complex, often involving hundreds of industries. Still, the basic principles and steps remain the same. Modern software tools make handling and analyzing these large matrices feasible.


## Lecture 5

Imagine you have a seesaw in a playground. When two people of the same weight sit on each end, the seesaw will be balanced and level. This is similar to equilibrium in economics.

In economics, equilibrium is like a balanced seesaw, but instead of people and weight, we are balancing supply and demand. When the amount of goods people want to buy (demand) is equal to the amount of goods available for sale (supply), we have what is called a market equilibrium. This balance determines the price of the good.

For example, let's say you and your friends want to buy lemonade on a hot day. If there's a lot of lemonade available and not many people want to buy it, the price will likely be low. But if there's only a little lemonade and a lot of people want it, the price will be high. The point at which the amount of lemonade people want to buy is equal to the amount available, and everyone is happy with the price, is the equilibrium.

- - -

Calculus is a branch of mathematics that deals with the study of change (differential calculus) and accumulation (integral calculus). It provides us with the tools to analyze and understand dynamic processes and systems that change continuously. 

When we talk about differential calculus, we are primarily concerned with the concept of a derivative, which represents the rate at which a function changes as its input changes. In simpler terms, derivatives help us find the slope of a curve at any given point. This is crucial in economics when we want to understand how one variable responds to changes in another variable, such as the relationship between price and quantity demanded in the market.

On the other hand, integral calculus is concerned with the concept of an integral, which represents the accumulation of quantities. Integrals allow us to calculate areas under curves and can be used to find total cost, total revenue, or consumer surplus, given their respective density functions.

Together, these concepts from calculus are fundamental tools in mathematical economics, helping us model and analyze the dynamic and complex relationships between different economic variables.

- - -

Review the concept of maps, functions. Then the concept of the slope (of the graph of a function). Then finite change and infinitesimal change. Then the derivative.

## Lecture 6

**Euler's number $e$**

The Euler constant $e$ is an irrational and `transcendental`(explain) number approximately equal to $2.71828$. It has a beautiful and interesting origin that can be traced back to compound interest.

**Origin of $e$:**

Imagine you invest \$1 at an interest rate of 100% per year. How much will you have at the end of one year?

1. **No compounding (n = 0):**
   - You would have \$2 at the end of the year.

Now, consider the interest is compounded, meaning that the interest is added to the principal periodically and the new total then earns interest.

2. **Compounded annually (n = 1):**
   - You would have $1 \times \left(1 + \frac{1}{1}\right)^1 = \$2$.

3. **Compounded semi-annually (n = 2):**
   - You would have $1 \times \left(1 + \frac{1}{2}\right)^2 = \$2.25$.

4. **Compounded quarterly (n = 4):**
   - You would have $1 \times \left(1 + \frac{1}{4}\right)^4 \approx \$2.44$.

As you increase the frequency of compounding ($n$), the total amount you would have at the end of the year approaches $e$. Mathematically, this is expressed as:

$$
\lim_  {n \to \infty} \left(1 + \frac{1}{n}\right)^n = e \approx 2.71828...
$$

This is the origin of Euler's number $e$ in the context of compound interest. The more frequently interest is compounded, the more money you end up with, and this approaches a limit as the compounding frequency goes to infinity, which is $e$.

**Importance in Economics:**

The number $e$ plays an important role in economics, particularly in financial mathematics. Here are some examples:

1. Compound Interest:
   - As we've seen in the example above, $e$ is crucial in calculating compound interest, which is foundational in economics and finance.

2. Exponential Growth and Decay:
   - Many economic processes, like population growth, inflation, and depreciation, can be modeled by exponential functions, and the base of these exponential functions is often $e$.

3. Option Pricing:
   - In the Black-Scholes model for option pricing, the exponential function with base $e$ is used to model the behavior of stock prices over time.

4. Elasticity:
   - In microeconomics, elasticity, which measures the responsiveness of demand or supply to changes in price or income, often involves exponential functions with base $e$.

In summary, the number $e$ has a rich and intuitive origin in compound interest, and its applications in economics, particularly in financial mathematics and modeling, make it an essential constant in the field.

**Understanding the Chain Rule in Calculus**

To introduce the concept of the chain rule and its applications in finding the derivatives of composite functions.

The chain rule is a fundamental principle in calculus that allows us to find the derivative of a composite function. A composite function is a function that combines two or more functions in a specific order. For example, if we have two functions, $f(x)$ and $g(x)$, then a composite function could be $f(g(x))$, where we first apply $g(x)$ and then apply $f(x)$ to the result.

The Chain Rule:
The chain rule states that if you have a composite function $f(g(x))$, and you want to find its derivative, you would do the following:

$$
\frac{d}{dx} f(g(x)) = f'(g(x)) \cdot g'(x)
$$

Here, $f'(g(x))$ is the derivative of $f$ with respect to $g(x)$, and $g'(x)$ is the derivative of $g$ with respect to $x$.

Example 1:
Let's consider an example to understand the application of the chain rule.

$$
h(x) = \sin(x^2)
$$

Here, we can consider $f(x) = \sin(x)$ and $g(x) = x^2$, so that $h(x) = f(g(x))$. Now, we want to find the derivative of $h(x)$.

$$
\begin{aligned}
h'(x) &= \frac{d}{dx} \sin(x^2) \\
&= \cos(x^2) \cdot \frac{d}{dx} x^2 \\
&= 2x \cdot \cos(x^2)
\end{aligned}
$$

Example 2:
Let's take another example.

$$
h(x) = \exp(\sin(x))
$$

Here, $f(x) = \exp(x)$ and $g(x) = \sin(x)$, so $h(x) = f(g(x))$. We want to find the derivative of $h(x)$.

$$
\begin{aligned}
h'(x) &= \frac{d}{dx} \exp(\sin(x)) \\
&= \exp(\sin(x)) \cdot \frac{d}{dx} \sin(x) \\
&= \exp(\sin(x)) \cdot \cos(x)
\end{aligned}
$$

The chain rule is an essential tool in calculus that allows us to find the derivatives of composite functions. It provides a systematic way to break down complex functions into simpler parts, find their derivatives individually, and then multiply them together to get the desired result. As we have seen from the examples, the chain rule is applicable to a wide range of functions, making it a versatile and powerful tool in mathematics.

Explain partial derivative, and gradient.

Introduce the concept of implicit functions and discuss the implications of the Implicit Function Theorem.

In calculus, we often deal with functions that are explicitly defined, where the dependent variable is isolated on one side of the equation. However, in some cases, the dependent variable cannot be easily isolated, and we have to work with implicit functions, where the dependent and independent variables are mixed together. The Implicit Function Theorem provides a way to handle such cases.

**Implicit Function Theorem:**
The Implicit Function Theorem states that if we have an equation in two or more variables, we can often solve for one variable as a function of the others, even if the equation doesn’t explicitly define it as such. In other words, it allows us to find the derivative of an implicitly defined function without explicitly solving for the function.

**Example 1:**
Consider the equation:

$$x^2 + y^2 = 1$$

This equation defines $y$ implicitly as a function of $x$. We can use the Implicit Function Theorem to find $\frac{dy}{dx}$:


$$
\begin{aligned}
2x + 2y\frac{dy}{dx} &= 0 \\
\frac{dy}{dx} &= -\frac{x}{y}
\end{aligned}
$$

**Example 2:**
Consider the equation:

$$x^2 - 2xy + y^2 = 3.$$

Again, this equation defines $y$ implicitly as a function of $x$. We can find $\frac{dy}{dx}$ by differentiating both sides of the equation with respect to $x$:

$$
\begin{aligned}
2x - 2y - 2x\frac{dy}{dx} + 2y\frac{dy}{dx} &= 0 \\
(2y - 2x)\frac{dy}{dx} &= 2y - 2x \\
\frac{dy}{dx} &= \frac{y - x}{y - x} \\
\frac{dy}{dx} &= 1
\end{aligned}
$$

The Implicit Function Theorem is a powerful tool in calculus that allows us to find the derivatives of implicitly defined functions. It is useful in cases where isolating the dependent variable is difficult or impossible. By understanding the Implicit Function Theorem, we can better analyze and interpret complex relationships between variables in mathematics and other related fields.

### Lecture 7

Integral calculus is an essential mathematical tool in economics for several reasons:

1. **Understanding Accumulation:** Integral calculus helps to model and analyze accumulated quantities, such as total revenue, cost, and profit, over a certain period.

2. **Area Under Curves:** It is used to calculate areas under curves, which can represent total income, cost, or other economic variables over time or quantity.

3. **Consumer and Producer Surplus:** In microeconomics, integral calculus is used to calculate consumer and producer surplus, which are areas between demand and supply curves.

4. **Marginal Analysis:** Integrals can be used to find the total effect of a marginal change, like the total cost from a marginal cost function.

5. **Economic Growth and Investment:** In macroeconomics, integral calculus is used to model economic growth and investment over time.

6. **Optimization:** Integral calculus is often paired with differential calculus to find optimal solutions, like maximizing profit or minimizing cost.

7. **Solving Differential Equations:** Many economic models are described by differential equations, and integral calculus is used to solve these equations.

In summary, integral calculus is a powerful tool in economics that helps to analyze and solve complex problems related to accumulation, areas under curves, optimization, and differential equations. By understanding how quantities accumulate and how to find areas under curves, economists can gain valuable insights into various economic phenomena and make more informed decisions.

- - -

One of the classical models used to describe market growth is the logistic growth model. The logistic growth model is represented by the following differential equation:

$$ \frac{dP}{dt} = rP\left(1 - \frac{P}{K}\right) $$

Where:
- $\frac{dP}{dt}$ represents the rate of change of the market size or population over time.
- $P$ is the market size or population at time $t$.
- $r$ is the growth rate of the market.
- $K$ is the carrying capacity of the market, which is the maximum market size that can be sustained given the available resources.

This model describes how the market growth rate is proportional to the current market size, but it also includes a term that slows down the growth rate as the market size approaches the carrying capacity.

To use this model, you would need to:
1. Determine the parameters $r$ and $K$ based on historical data or expert knowledge.
2. Solve the differential equation to get the market size as a function of time, $P(t)$.
3. Analyze the solution to make predictions about future market growth.

For example, if you have a new product and you want to predict how its market will grow over time, you would collect data on the current market size, growth rate, and potential maximum market size. Then, you would use the logistic growth model to predict how the market will evolve over time. This can help you make informed decisions about production, marketing, and other strategic considerations.

- - -

Introduce the initial value problems.

Introduce the indefinite integrals. The integral sign, the measure and the integrand. 

Introduce the definite integrals. Explain the connection between definite and indefinite integrals. 

Explain the power rule. The exponential rule and the logarithmic rule. Integrals are linear. 

Introduce the substitution rule. For example, 

$$
\int dx \, 2x (x^{2}+1). 
$$

Integral by parts. 

Explain the improper integrals.

### Lecture 8 (Nov 1st)

An economic equilibrium refers to a state where supply equals demand and all agents in the economy are optimizing their decisions given the constraints they face, and there are no tendencies for change. In other words, it is a state where all forces in an economy are balanced, and the economy is stable. There are different types of equilibria in economics, such as market equilibrium, general equilibrium, and Nash equilibrium, each referring to different contexts and conditions of balance and stability. 

Optimization, meaning “the quest for the best.” For example, a business firm may seek to maximize profit $P$, that is, to maximize the difference between total revenue $R$ and total cost $C$. 

- - -

**output level**

In economics, output level refers to the total quantity of goods or services produced by an individual, firm, industry, or entire economy within a specific period. It's an important indicator of economic activity and is often used to analyze the performance and health of an economy.

For an individual firm or industry, the output level would be the total quantity of products or services produced. For an entire economy, the output level is typically represented by the Gross Domestic Product (GDP), which measures the total value of all goods and services produced within a country's borders over a specific period. Another related measure is the Gross National Product (GNP), which represents the total value of all goods and services produced by the residents of a country, regardless of where they are produced.

Understanding output levels is crucial for economists and policymakers because it helps to:

1. **Measure Economic Performance:** The output level indicates how efficiently an economy is using its resources to produce goods and services.

2. **Analyze Business Cycles:** By observing changes in output levels over time, economists can identify trends and business cycles, including periods of economic growth and recession.

3. **Formulate Economic Policy:** Policymakers use output levels to develop strategies to manage economic activity, such as monetary and fiscal policies.

4. **Make Forecasts:** Economists use past output levels to make predictions about future economic activity and growth.

In summary, the output level is a fundamental concept in economics that provides valuable insights into the health and performance of an economy. It is used to analyze trends, develop economic policy, and make forecasts about future economic activity.

- - -

**First-Derivative Test**

How can be tell the local stationary point using first derivatives. What else is needed to tell if it is the local maximum or minimum?

**Second derivative and higher derivatives.** Concave and convex functions. **Introduce the second derivative test**.

Introduce the Taylor expansion.

### Lecture 9 (Nov 6th)

Introduce exponent and logarithmic functions. Talk about their derivatives and applications.

One interesting and significant application of exponential functions in economics is in the concept of the "Multiplier Effect" associated with fiscal policy.




### Lecture 10 (Nov 8)

Consider a consumer with the simple utility (index) function

$$
U = x_ {1}x_ {2}+2x_ {1}.
$$

Without any constraints, it is impossible to optimize $U$. But with some budget constrain, for instance 

$$
x_ {1}+2x_ {2}=50,
$$

then we can optimize it. 

Introduce the Lagrangian multiplier method. 

Some examples for the Lagrange multiplier:

Ex1. Find the extremum of $z=xy$ subject to $x+y=6$.

Ex2. Find the extremum of $z=x_ {1}^{2}+x_ {2}^{2}$ subject to $x_ {1}+4x_ {2}=2$.

### Lecture 11 (Nov 15)

Introduction of the basic concepts of probability. 

1. Probabilistic vs. deterministic world views. Is there such thing as free will or it is determined by nature?
2. Why probability works in predicting the future. Two causes of probability.
3. The sample space. Including the application of set theory.
### Lecture 12 (Nov 22)

Countable infinite sample space and continuous sample space. 

Permutation and combination.

The Gaussian (normal, bell) distribution.

### Lecture 13 (Nov 29)

**Conditional Probability**

Ex.1 An experiment consists of rolling a die once. Let $X$ be the outcome. Let $F$ be the event $\left\lbrace X=6 \right\rbrace$, and let $E$ be the event $\left\lbrace X>4 \right\rbrace$. 

Ex.2 One finds that in a population of 100,000 females, 90% can expect to live to age 60, while 50% can expect to live to age 80. Given that a woman is 60, what is the probability that she lives to age 80?

Ex.3 Three candidates A, B, and C are running for office. We decided that A and B have an equal chance of winning and C is only 1/2 as likely to win as A. Let A be the event “A wins,” B that “B wins,” and C that “C wins.” Hence, we assigned probabilities $P(A) = 2/5, P(B) = 2/5$, and $P(C) = 1/5$. Suppose that before the election is held, A drops out of the race.

Introduce the conditioned probability.

Introduce the Bayes probabilities.

We have two urns, I and II. Urn I contains 2 black balls and 3 white balls. Urn II contains 1 black ball and 1 white ball. An urn is drawn at random and a ball is chosen at random from it. We can represent the sample space of this experiment as the paths through a tree. Show the probabilities assigned to the paths.

Another example, consider the following description: Steve is very *shy and withdrawn*, invariably helpful but with very little interest in people or in the world of reality. A meek and tidy soul. He has a need for order and structure, and a passion for detail. Now, what is he more likely to be, a farmer or a librarian?

## Final Exam 

**Problem 1**

Consider a production firm that manufactures a single product. The firm's production output depends on two factors: labor (L) and capital (K). The market for its product is competitive, and the firm aims to maximize its profit.

*Part 1: Production Function and Cost Analysis* [30 Points]

- 1.1 Linear Algebra Application (10 points): The firm's production function is given by $Q(L, K) = aL + bK$, where $Q$ is the quantity of output, and $a$ and $b$ are constants. Represent this production function in matrix form and find the level of output when $L = 3$ and $K = 5$, given $a = 2$ and $b = 3$.
- 1.2 Calculating Costs (20 points): Assume the firm's total cost (TC) function is $TC = cL^2 + dK^2 + f$, where $c, d,$ and $f$ are constants. Calculate the marginal cost (MC) of labor and capital. 

*Part 2: Profit Maximization* [30 Points]

- 2.1 Differential Calculus (15 points): Given the price per unit of the product is $P$, write the profit function $\Pi$ and use differentiation to find the conditions for profit maximization.
- 2.2 Break-Even Analysis (20 points): Determine the break-even points for the firm in terms of $L$ and $K$.

- - -

**Problem 2** [20 Points]

Consider a market where the supply curve is given by $S(q)=2q^{2}$ and the demand curve is given by $D(q)=40-q$, where $q$ is the quantity of goods. The market reaches equilibrium where supply equals demand. Calculate the consumer surplus at equilibrium.

- - -

**Problem 3** [20 Points]

A company is planning to launch a new product. Market research suggests that the demand for this product can be modeled as a normally distributed random variable with a mean of 1000 units and a standard deviation of 200 units. Calculate the probability that the demand will exceed 1200 units. Also, determine the probability that the demand will be between 800 and 1200 units.


### Answer to the final exam

**Problem 1**

Consider a production firm that manufactures a single product. The firm's production output depends on two factors: labor (L) and capital (K). The market for its product is competitive, and the firm aims to maximize its profit.

*Part 1: Production Function and Cost Analysis* [30 Points]

- 1.1 Linear Algebra Application (10 points): The firm's production function is given by $Q(L, K) = aL + bK$, where $Q$ is the quantity of output, and $a$ and $b$ are constants. Represent this production function in matrix form and find the level of output when $L = 3$ and $K = 5$, given $a = 2$ and $b = 3$.

**Answer**: To represent this in matrix form, consider the vector of inputs $\begin{bmatrix} L \\ K \end{bmatrix}$ and the matrix of coefficients $\begin{bmatrix} a & b \end{bmatrix}$. The production function becomes a matrix product. The key points is that the production has to be the form

$$
\begin{bmatrix} a & b \end{bmatrix} \cdot \begin{bmatrix} L \\ K \end{bmatrix},
$$

it shouldn't be written as, for example

$$
\begin{bmatrix} a & b \end{bmatrix} \cdot\begin{bmatrix} L & K \end{bmatrix} , \quad \text{Incorrect!}
$$

Substitution of the variables with numbers is straightforward,

$$ Q = \begin{bmatrix} a & b \end{bmatrix} \begin{bmatrix} L \\ K \end{bmatrix} = \begin{bmatrix} 2 & 3 \end{bmatrix} \begin{bmatrix} 3 \\ 5 \end{bmatrix} = 2 \times 3 + 3 \times 5 = 21.$$

- 1.2 Calculating Costs (20 points): Assume the firm's total cost (TC) function is $TC = cL^2 + dK^2 + f$, where $c, d,$ and $f$ are constants. Calculate the marginal cost (MC) of labor and capital. 

**Answer**: Marginal Cost (MC) is the derivative of the Total Cost (TC) with respect to a particular input while holding other inputs constant. We just need to calculate $MC_L = \frac{\partial TC}{\partial L}$ and $MC_K = \frac{\partial TC}{\partial K}$. To be specific,

$$
\frac{\partial TC}{\partial L} = 2cL,\quad  \frac{\partial TC}{\partial K}=2dK.
$$

*Part 2: Profit Maximization* [30 Points]

- 2.1 Differential Calculus (15 points): Given the price per unit of the product is $P$, write the profit function $\Pi$ and use differentiation to find the conditions for profit maximization.
- 2.2 Break-Even Analysis (20 points): Determine the break-even points for the firm in terms of $L$ and $K$.

**Answer**: The profit function is 

$$
\Pi = P \times  Q -TC = P(aL+bK)-(cL^{2}+dK^{2}+f),
$$

the conditions for profit maximization is where the first order partial derivatives are zero,

$$
\frac{\partial \Pi}{\partial L}=ap-2cL=0
$$

and 

$$
\frac{\partial\Pi}{\partial K}=bP-2dK=0. 
$$

A common mistake here is to put the total derivative symbol $d\Pi / dL$ instead of partial derivative symbol.

Break-even occurs when $\Pi = 0$. We can set the profit function $\Pi = 0$ and solve for $L$ and $K$ to find the break-even points. The break even point is given by $L$ and $K$ such that 

$$
-P(aL+bK)+(cL^{2}+dK^{2}+f)=0.
$$

For more mathematically advanced students, we can also try to complete the square,

$$
\begin{align*}
&(c L^{2}-aP L ) +(dK^{2}-PbK) +f =0\\
\implies& \left( cL^{2} -2\cdot \sqrt{ c }L \cdot \frac{aP}{2\sqrt{ c }} + \frac{a^{2}P^{2}}{4c} \right)-\frac{a^{2}P^{2}}{4c}  \\
&+\left( dK^{2}-2\cdot\sqrt{ d }K\cdot \frac{Pb}{2\sqrt{ d }}+ \frac{P^{2}b^{2}}{4d} \right)-\frac{P^{2}b^{2}}{4d}+f=0\\
\implies & \left( \sqrt{ c }L- \frac{aP}{2\sqrt{ c }} \right)^{2}+\left( \sqrt{ d }K- \frac{pB}{2\sqrt{ d }} \right)^{2} = \text{Const}
\end{align*}
$$

where the const term is an expression of all the parameters of the model. We see that the break even points in terms of $(L,K)$ *form an ellipse*! 

- - -

**Problem 2** [20 Points]

Consider a market where the supply curve is given by $S(q)=2q^{2}$ and the demand curve is given by $D(q)=40-q$, where $q$ is the quantity of goods. The market reaches equilibrium where supply equals demand. Calculate the consumer surplus at equilibrium.

**Answer**.  From $D(q)=S(q)$ we get $q^{\ast}\approx 4.23$, the other negative root can be safely neglected. Then the consumer surplus is 

$$
\text{Consumer surplus} = \frac{1}{2}\times q^{\ast } \times (40-D(q^{\ast })) \approx 8.9.
$$

A common mistake is that when people draw the demand-supply plot, the supply curve appears to be a straight line, which is what students would get from most online teaching materials on consumer surplus. However, in our case, the supply line is quadratic.

- - -

**Problem 3** [20 Points]

A company is planning to launch a new product. Market research suggests that the demand for this product can be modeled as a normally distributed random variable with a mean of 1000 units and a standard deviation of 200 units. Calculate the probability that the demand will exceed 1200 units. Also, determine the probability that the demand will be between 800 and 1200 units.

**Answer.** To calculate these probabilities, we'll use the properties of the normal distribution and integrate the probability density function (PDF) over the desired range. The PDF of a normal distribution with mean $\mu$ and standard deviation $\sigma$ is given by:

$$
f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}
$$

For our case, $\mu = 1000$ and $\sigma = 200$.

To calculate the probability that demand exceeds 1200 units, we need to integrate the PDF from 1200 to infinity:
   $$
   P(X > 1200) = \int_{1200}^{\infty} \frac{1}{200 \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-1000}{200}\right)^2} dx
   $$

This integral can be transformed into a standard normal distribution integral by substituting $z = \frac{x - 1000}{200}$, which simplifies the integral to a form involving the standard normal cumulative distribution function. Similarly, we integrate the PDF from 800 to 1200: 

$$
   P(800 < X < 1200) = \int_{800}^{1200} \frac{1}{200 \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-1000}{200}\right)^2} dx.
$$

Let's calculate these integrals and their numerical values in Mathematica. The code to calculate $P(X>1200)$ reads

```mathematica
NIntegrate[1/(200 Sqrt[2 Pi]) Exp[-1/2 ((x - 1000)/200)^2], {x, 1200, Infinity}]
```

and yields  $0.1587$. This means there is about a 15.87% chance that the demand will exceed 1200 units.

The Mathematica code for integral 

$$
   P(800 < X < 1200) = \int_{800}^{1200} \frac{1}{200 \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-1000}{200}\right)^2} dx
$$

   is 
   
```mathematica
NIntegrate[1/(200 Sqrt[2 Pi]) Exp[-1/2 ((x - 1000)/200)^2], {x, 800, 1200}]
```

and yields $0.6827$. This indicates there is about a 68.27% chance that the demand will be between 800 and 1200 units.