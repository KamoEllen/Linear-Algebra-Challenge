# Linear Algebra Notes: Eigenvalues & Eigenvectors

## 1. Key Concepts

### What are Eigenvalues & Eigenvectors?
- **Eigen** comes from German meaning "own" or "characteristic"
- An eigenvalue (λ) is a special number associated with a matrix
- An eigenvector (v) is a non-zero vector that, when transformed by the matrix, only gets scaled by its corresponding eigenvalue

### The Fundamental Equation:
```
Av = λv
```
Where:
- A is the matrix
- v is the eigenvector
- λ is the eigenvalue

## 2. Geometric Interpretation

### Key Properties:
- When matrix A transforms an eigenvector, it only:
  * Stretches/shrinks the vector (by factor λ)
  * Does NOT change its direction (except possibly reversing it)
- Every vector along the same line as an eigenvector is also an eigenvector
- The zero vector is never an eigenvector

## 3. Finding Eigenvalues & Eigenvectors

### Step 1: Find Eigenvalues
1. Write the characteristic equation: det(A - λI) = 0
2. Solve for λ

### Step 2: Find Eigenvectors
For each eigenvalue λ:
1. Substitute λ into (A - λI)v = 0
2. Solve the system of equations
3. Find a non-zero solution for v

## 4. Example Walkthrough

Let's solve for a 2×2 matrix:
```
A = [3 1]
    [0 2]
```

### Finding Eigenvalues:
1. Set up det(A - λI) = 0:
```
|3-λ  1 | = 0
|0  2-λ |
```

2. Calculate determinant:
```
(3-λ)(2-λ) = 0
```

3. Solve:
```
λ = 3 or λ = 2
```

### Finding Eigenvectors:
For λ = 3:
```
[3-3  1 ][x] = [0]
[0  2-3][y]   [0]

[0  1 ][x] = [0]
[0 -1 ][y]   [0]
```
Solution: v₁ = [1, 0]ᵀ

For λ = 2:
```
[3-2  1 ][x] = [0]
[0  2-2][y]   [0]

[1  1 ][x] = [0]
[0  0 ][y]   [0]
```
Solution: v₂ = [-1, 1]ᵀ

## 5. Important Tips

- Always check:
  * Is your eigenvector non-zero?
  * Does Av = λv hold for your solution?
- Any scalar multiple of an eigenvector is also an eigenvector
- The number of eigenvalues equals the size of the square matrix
- For an n×n matrix, you'll get an nth-degree polynomial to solve

