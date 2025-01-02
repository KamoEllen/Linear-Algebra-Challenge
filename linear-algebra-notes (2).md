# Linear Algebra Notes: Matrix Inverses & Transformations

## 1. Matrix Inverses Fundamentals
---
### Definition
```
A × A⁻¹ = A⁻¹ × A = I
```
Think of it like numbers: 3 × (1/3) = 1

### Requirements for Invertibility
- Must be square matrix (n × n)
- Determinant ≠ 0
- Row reduction must yield identity matrix

### 2×2 Matrix Inverse Formula
For matrix A = $\begin{bmatrix} a & b \\ c & d \end{bmatrix}$

$A^{-1} = \frac{1}{ad-bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$

#### Example:
$A = \begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}$

$A^{-1} = \frac{1}{1(1) - 2(0)} \begin{bmatrix} 1 & -2 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 1 & -2 \\ 0 & 1 \end{bmatrix}$

## 2. Finding Matrix Inverses (Step-by-Step)
---
### Augmented Matrix Method
1️⃣ Write [A|I]
2️⃣ Row reduce until left side becomes I
3️⃣ Right side becomes A⁻¹

#### Example:
```
[1 2|1 0]     →     [1 0|1 -2]
[0 1|0 1]           [0 1|0  1]
```

## 3. Linear Transformations
---
### Key Properties
- Maps vectors between spaces
- Preserves vector operations
- Represented by matrices

### Visualization of Invertible vs Non-invertible Transformations

#### Invertible (One-to-one):
```
Input → Output
  v₁  →   w₁
  v₂  →   w₂
  v₃  →   w₃
```

#### Non-invertible (Many-to-one):
```
Input → Output
  v₁  →   w₁
  v₂  →   w₁  ❌ Multiple inputs map to same output
  v₃  →   w₂
```

## 4. Determinants
---
### 2×2 Determinant Formula
For $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$

det(A) = ad - bc

#### Example:
$\begin{vmatrix} 1 & 2 \\ 3 & 4 \end{vmatrix} = (1×4) - (2×3) = 4 - 6 = -2$

### 3×3 Sign Pattern
```
| +  -  + |
| -  +  - |
| +  -  + |
```

### Quick Tips
- det = 0 → Not invertible
- det ≠ 0 → Invertible
- det(AB) = det(A) × det(B)
- det(A⁻¹) = 1/det(A)
