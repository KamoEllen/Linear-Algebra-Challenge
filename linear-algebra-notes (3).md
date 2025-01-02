# 📚 Linear Algebra: Comprehensive Study Notes

## 1. Vector Spaces Fundamentals 🔲

### Core Requirements
A vector space must have:
1. Vector Addition (v + w)
2. Scalar Multiplication (cv)

Think of it like building blocks that you can:
- Add together (vector addition)
- Stretch or shrink (scalar multiplication)

## 2. Subspaces 📐

A subspace is like a "mini vector space" within a larger space. 

### Must satisfy 3 rules:
1. ⭕ Contains zero vector
2. ➕ Closed under addition
3. ✖️ Closed under scalar multiplication

### Visual Examples:
```
Valid Subspaces:          Not Subspaces:
↗️ Line through origin    ➖ Line not through origin
📋 Plane through origin  🔵 Circle not at origin
⚪ Just {0} vector       ❌ Empty set
```

## 3. Spans and Linear Independence 🌟

### Span Definition
If v₁, v₂ are vectors, their span is:
```
span{v₁, v₂} = {c₁v₁ + c₂v₂ | c₁, c₂ ∈ ℝ}
```

### Visual Examples:
- Span of 1 vector: Line through origin
```
    ↗️
    ↗️
----+----
    ↗️
    ↗️
```

- Span of 2 independent vectors: Plane through origin
```
    ↗️ ↗️
   ↗️↗️↗️
---+---
 ↗️↗️↗️
↗️ ↗️
```

## 4. Matrix Spaces 🔲

### Column Space (Col A)
- Lives in output space (ℝᵐ)
- All possible outputs b where Ax = b has a solution

#### Example:
For matrix A = [1 0; 0 0]:
```
Input space (ℝ²)    Output space (ℝ²)
    ↑               
    |     A         ───────
────+────  →       |
    |              |
```
Column space is just the x-axis!

### Null Space (Null A)
- Lives in input space (ℝⁿ)
- All vectors x where Ax = 0

#### Example:
For matrix A = [1 1; 0 0]:
```
Null space is the line y = x:
    ↑
   ↗️
──↗️+────
 ↗️ |
↗️  |
```

## 5. Basis Vectors 📏

A basis is like a coordinate system. It needs:
1. Independence (no redundancy)
2. Spans space (reaches everywhere)

### Standard Basis Examples:
```
ℝ² Standard Basis:      Alternative Basis:
    ↑                       ↗️   ↖️
    |                        \   /
────+────                ────+────
    |                        /   \
                           ↙️   ↘️
e₁ = [1,0]               a₁ = [1,1]
e₂ = [0,1]               a₂ = [-1,1]
```

## 6. Finding Bases in Practice 📝

### For Null Space:
1. Set up Ax = 0
2. Solve using RREF
3. Write parametric solution

Example:
```
A = [1 2 1;
     2 4 3]

Null space basis:
v = [-2; 1; 0]
```

### For Column Space:
1. Get RREF
2. Identify pivot columns
3. Use ORIGINAL columns at pivot positions

Example:
```
A = [1 2 1;
     2 4 3]
     
Column space basis:
v₁ = [1; 2] (first column)
```

## 🎯 Key Takeaways:
1. Every subspace can be described by a basis
2. Column space shows possible outputs
3. Null space shows what gets mapped to zero
4. Basis gives minimum vectors needed to reach all points

Need help with any specific topic? Let me know! 📚
