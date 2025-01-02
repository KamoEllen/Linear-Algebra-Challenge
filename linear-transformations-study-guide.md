# LINEAR TRANSFORMATIONS STUDY GUIDE

## 1. ONE-TO-ONE AND ONTO TRANSFORMATIONS

### Basic Definitions
- Transformation T maps from domain RN to codomain RM
- Two key properties: one-to-one and onto

### Onto Transformations
- Definition: Every vector in codomain is hit by something from domain
- Mathematical form: For any Y in codomain, ∃X in domain where T(X) = Y
- Example of ONTO: T(x,y) = (x,y) [Identity transformation]
  - Every point (a,b) in codomain has corresponding input (a,b)
- Example of NOT ONTO: T(x,y) = (x,0) [Projection onto x-axis]
  - Points like (1,1) can never be reached
  - Only points on x-axis are hit

### One-to-One Transformations
- Definition: Different inputs always give different outputs
- Mathematical form: If T(x₁) = T(x₂), then x₁ = x₂
- Example of ONE-TO-ONE: T(x,y) = (2x,2y) [Scaling]
  - Input (1,1) → Output (2,2)
  - Input (2,2) → Output (4,4)
  - No overlap in outputs
- Example of NOT ONE-TO-ONE: T(x,y) = (x,0)
  - Both (1,2) and (1,3) map to (1,0)
  - Multiple inputs collapse to same output

## 2. COMPOSITION OF TRANSFORMATIONS

### Basic Rules
- For composing T_A and T_B:
  - T_B: RP → RN
  - T_A: RN → RM
  - Composition (T_A ∘ T_B): RP → RM

### Matrix Multiplication
- Represents composition of transformations
- For matrices A (m×n) and B (n×p):
  - Product AB will be m×p
  - Middle dimension n must match
- Methods:
  1. Column method: AB = [AB₁ AB₂ ... ABₙ]
  2. Row-Column method: Entry (i,j) = dot product of row i (A) with column j (B)

### Composition Examples
1. Order Doesn't Matter Example:
   ```
   T₁(x,y) = (2x,2y)    [Scale by 2]
   T₂(x,y) = (x,-y)     [Flip over x-axis]
   (T₂ ∘ T₁)(x,y) = (2x,-2y)
   (T₁ ∘ T₂)(x,y) = (2x,-2y)
   ```

2. Order Matters Example:
   ```
   T₁(x,y) = (x+y,y)    [Shear]
   T₂(x,y) = (x,2y)     [Vertical stretch]
   (T₂ ∘ T₁)(1,1) = (2,2)
   (T₁ ∘ T₂)(1,1) = (3,2)
   ```

## 3. GEOMETRIC VISUALIZATION

### Standard Basis Vectors
- e₁ = [1,0]
- e₂ = [0,1]

### Common Transformations
1. Identity:
   ```
   Matrix: [[1 0], [0 1]]
   e₁ → (1,0)
   e₂ → (0,1)
   ```

2. Scaling:
   ```
   Matrix: [[2 0], [0 2]]
   e₁ → (2,0)
   e₂ → (0,2)
   ```

3. Shear:
   ```
   Matrix: [[1 1], [0 1]]
   e₁ → (1,0)
   e₂ → (1,1)
   ```

### Key Properties
- Linear combinations are preserved
- For v = x₁e₁ + x₂e₂:
  T(v) = x₁T(e₁) + x₂T(e₂)
- Order of transformations matters: AB ≠ BA generally

## IMPORTANT REMINDERS
1. Always check matrix dimensions match for multiplication
2. Composition order can affect result
3. One-to-one means no collapsing
4. Onto means everything in codomain is hit
5. Matrix entries show where basis vectors go

