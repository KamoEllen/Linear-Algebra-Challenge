# Linear Algebra Notes - Dimension & Basis Changes

## 1. Dimension
**Definition**: The dimension of a subspace is the number of basis vectors needed to span it.

Key Properties:
- Dimension is unique (same number of basis vectors regardless of which basis is chosen)
- For RN: dim(RN) = N
- For zero vector subspace: dim({0}) = 0

Visual Example:
```
Plane in R3:
• Has 2 basis vectors → dimension = 2
• Different bases possible but always need exactly 2 vectors
• Any 2 linearly independent vectors in plane form basis
```

## 2. Dimensions of Matrix Spaces

### Null Space Dimension
- dim(Null Space) = number of free variables
- Found by reducing Ax = 0 to RREF

### Column Space Dimension
- dim(Column Space) = number of leading 1's in RREF
- Also called rank(A)

Key Theorem:
```
dim(Null Space) + dim(Column Space) = n
where n = number of columns in matrix A
```

## 3. Change of Basis

### Core Concept
Converting vector coordinates between different bases:
```
Standard Basis ↔ B-basis ↔ C-basis
```

### Change of Basis Matrix Formula
For vector x:
- xC = PC⁻¹PB(xB)  
where:
- xB = coordinates in B-basis
- xC = coordinates in C-basis
- PB = matrix with B-basis vectors as columns
- PC = matrix with C-basis vectors as columns

### Geometric Interpretation
1. Start in B-basis (looks like standard grid to B-basis observer)
2. PB maps to standard basis
3. PC⁻¹ maps to C-basis 

Visual Process:
```
B-basis → Standard → C-basis
[2,-1]B → Standard coords → [3,2]C
```

Example:
```
If B = {[7,5], [4,3]} and C = {[1,1], [1,2]}
Change of basis matrix = [9 7; -2 -5]
```

## Practice Tips
1. When finding dimension:
   - Count linearly independent vectors
   - Count leading 1's (for column space)
   - Count free variables (for null space)

2. For basis changes:
   - Write out basis vectors
   - Form PB and PC matrices
   - Use formula xC = PC⁻¹PB(xB)
