# Least-Squares Solutions in Linear Algebra

## Key Concept
When a system of equations Ax = b has no solution, we can find an approximate solution using the least-squares method. This gives us the "closest possible" solution.

## The Fundamental Theorem
For a matrix A (m×n) and vector b in Rᵐ, the least-squares solution is found by solving:
* (AᵀA)x = Aᵀb

## Solution Process
### Step 1: Verify No Exact Solution Exists
* Write the augmented matrix [A|b]
* Reduce to row echelon form
* Look for contradictions (like 0 = 1)

### Step 2: Find Least-Squares Solution
1. Calculate AᵀA
2. Calculate Aᵀb
3. Solve (AᵀA)x = Aᵀb using augmented matrix method
4. The resulting x is the least-squares solution (often written as x̂)

## Detailed Example
Given:
```
A = [0  6]
    [1  1]
    [2  1]

b = [6]
    [0]
    [0]
```

### 1. Calculate Aᵀ
```
Aᵀ = [0  1  2]
     [6  1  1]
```

### 2. Calculate AᵀA
```
AᵀA = [5  3]
      [3  3]
```

### 3. Calculate Aᵀb
```
Aᵀb = [0]
      [6]
```

### 4. Solve (AᵀA)x = Aᵀb
```
[5  3 | 0]
[3  3 | 6]  → RREF → Solution: x̂ = [-3]
                                    [5]
```

## Geometric Interpretation
* The least-squares solution x̂ gives Ax̂ that is closest to b
* In the example:
  * Ax̂ = [5, 2, 1]ᵀ (approximation)
  * b = [6, 0, 0]ᵀ (target)
  * Distance between Ax̂ and b = √6 units

## Visual Understanding
* The column space of A forms a plane
* b is a point (usually not on this plane)
* Ax̂ is the projection of b onto the column space of A
* The error (b - Ax̂) is perpendicular to the column space of A

## Important Properties
1. Ax̂ is the projection of b onto col(A)
2. (b - Ax̂) is orthogonal to col(A)
3. The least-squares solution minimizes ||Ax - b||

## Common Notation
* x̂ : least-squares solution
* col(A) : column space of matrix A
* ||v|| : magnitude/norm of vector v
