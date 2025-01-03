# Linear Algebra: Matrix Diagonalization & Powers

## 1. Why Diagonalization Matters

### Key Concept
A diagonalizable matrix A can be written as: A = PDP⁻¹
- P = matrix of eigenvectors
- D = diagonal matrix of eigenvalues
- P⁻¹ = inverse of P

### Advantages of Diagonal Matrices
1. Easy to compute powers
2. Simple multiplication with vectors
3. Straightforward rank calculation
4. Immediate eigenvalue identification

## 2. Diagonal Matrix Properties

### Definition
A diagonal matrix has:
- Non-zero entries possible only on main diagonal
- All other entries are zero

Example:
```
[2 0 0]
[0 5 0]
[0 0 1]
```

### Benefits
1. **Linear Systems**: Easy to solve
   - Each variable can be solved independently
   - Example: Dx = b becomes:
   ```
   [2 0 0][x₁]   [b₁]
   [0 5 0][x₂] = [b₂]
   [0 0 1][x₃]   [b₃]
   ```
   Solution: x₁ = b₁/2, x₂ = b₂/5, x₃ = b₃

2. **Rank**: Simply count non-zero diagonal entries

3. **Eigenvalues**: They are the diagonal entries

## 3. Matrix Powers Using Diagonalization

### Key Formula
For a matrix A raised to power n:
Aⁿ = (PDP⁻¹)ⁿ = P(Dⁿ)P⁻¹

### Example
For matrix A = [1 -1]
                [2  4]

1. Find eigenvalues (λ): λ = 2, 3
2. Find eigenvectors and form P
3. Create diagonal matrix D = [2 0]
                            [0 3]
4. For A¹⁰⁰:
   - Just compute 2¹⁰⁰ and 3¹⁰⁰ on diagonal
   - No need to multiply A by itself 100 times

## 4. Steps for Diagonalization

1. Find eigenvalues (λ)
2. Find eigenvectors for each λ
3. Form P from eigenvectors
4. Create D with eigenvalues on diagonal
5. Verify A = PDP⁻¹

## 5. Important Notes

### When is a Matrix Diagonalizable?
- Must have n linearly independent eigenvectors
- Number of linearly independent eigenvectors must equal matrix dimension

### Common Mistakes to Avoid
1. Forgetting to check if matrix is diagonalizable
2. Mixing up order of eigenvalues and eigenvectors
3. Not verifying final result

## 6. Applications

1. **Powers of Matrices**
   - Useful in:
     - Population growth models
     - Markov chains
     - Recursive sequences

2. **System Analysis**
   - Simplifies complex calculations
   - Makes long-term behavior visible

## Practice Problems

1. Given matrix A = [3 1]
                    [0 2]
   Calculate A⁵ using diagonalization.

2. Determine if matrix B = [1 1]
                          [0 1]
   is diagonalizable.

Remember: The power of diagonalization lies in converting complex matrix operations into simpler diagonal matrix operations!
