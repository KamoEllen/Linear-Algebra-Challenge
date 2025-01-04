# Linear Algebra Complete Study Guide
## Table of Contents
1. Dot Product Fundamentals
2. Vector Basics & Geometric Interpretation
3. Orthogonal Sets & Complements
4. Vector Projections & Decomposition
5. Practice Problems & Applications

## 1. Dot Product Fundamentals

### 1.1 Basic Definition
The dot product takes two vectors and produces a scalar (number):
- 2D: **a**·**b** = (a₁×b₁) + (a₂×b₂)
- 3D: **a**·**b** = (a₁×b₁) + (a₂×b₂) + (a₃×b₃)
- n-D: **a**·**b** = Σ(aᵢ×bᵢ) for i = 1 to n

### 1.2 Key Properties
1. Commutative: **a**·**b** = **b**·**a**
2. Distributive: (**a** + **b**)·**c** = (**a**·**c**) + (**b**·**c**)
3. Scalar Multiplication: c(**a**·**b**) = (c**a**)·**b** = **a**·(c**b**)
4. Self-Product: **a**·**a** ≥ 0 (equals 0 only for zero vector)

### 1.3 Worked Examples
```
Example 1 (2D):
a = [3, 5]
b = [8, 2]
a·b = (3×8) + (5×2) = 24 + 10 = 34

Example 2 (3D):
a = [2, -1, 3]
b = [4, 2, -1]
a·b = (2×4) + (-1×2) + (3×-1)
    = 8 + (-2) + (-3)
    = 3
```

## 2. Vector Basics & Geometric Interpretation

### 2.1 Standard Position
Vectors are represented as arrows with:
- Starting point at origin (0,0,0)
- Ending point at coordinates (x₁, x₂, x₃, ...)

### 2.2 Vector Length (Norm)
```
||v|| = √(v·v)
- 2D: ||v|| = √(v₁² + v₂²)
- 3D: ||v|| = √(v₁² + v₂² + v₃²)

Example:
v = [3, 4]
||v|| = √(3² + 4²) = √(9 + 16) = √25 = 5
```

### 2.3 Direction Relationships
- Positive dot product → vectors point similarly
- Zero dot product → vectors are perpendicular
- Negative dot product → vectors point oppositely

### 2.4 Unit Vectors
```
Standard basis vectors:
e₁ = [1, 0, 0]
e₂ = [0, 1, 0]
e₃ = [0, 0, 1]

To normalize: û = u/||u||

Example:
v = [3, 4]
||v|| = 5
û = [3/5, 4/5]
```

### 2.5 Distance Between Vectors
Formula: ||u - v|| = √((u₁-v₁)² + (u₂-v₂)²)

```
Example:
u = [1, 4]
v = [3, 1]
Distance = √((1-3)² + (4-1)²)
        = √(4 + 9)
        = √13
```

## 3. Orthogonal Sets & Complements

### 3.1 Orthogonal Vectors
Two vectors are orthogonal if:
1. Their dot product = 0
2. ||u - v|| = ||u + v||

```
Example:
u = [3, 4]
v = [-4, 3]
u·v = (3×-4) + (4×3) = -12 + 12 = 0
Therefore, u and v are orthogonal
```

### 3.2 Orthogonal Set Example
```
Check if these vectors form an orthogonal set:
u₁ = [3, 1, 1]
u₂ = [-1, 2, 1]
u₃ = [-1/2, -2, 7/2]

Checking all pairs:
1. u₁·u₂ = (3×-1) + (1×2) + (1×1) = -3 + 2 + 1 = 0 ✓
2. u₁·u₃ = (3×-1/2) + (1×-2) + (1×7/2) = -3/2 - 2 + 7/2 = 0 ✓
3. u₂·u₃ = (-1×-1/2) + (2×-2) + (1×7/2) = 1/2 - 4 + 7/2 = 0 ✓

All pairs are orthogonal, so this is an orthogonal set!
```

### 3.3 Orthogonal Complements
- W⊥ (W-perp) = set of all vectors orthogonal to W
- If W is a plane, W⊥ is the line perpendicular to W

Important Relationships:
1. Column space(A)⊥ = Null space(Aᵀ)
2. Row space(A)⊥ = Null space(A)

## 4. Vector Projections & Decomposition

### 4.1 Decomposition Formula
Any vector u can be split into:
1. w₁ (parallel to v): [(u·v)/(||v||²)]×v
2. w₂ (perpendicular to v): u - w₁

```
Visual Representation:
        u
       ↗
      /  
w₁   /   w₂
→   /     ↑
   /      |
  /   θ   |
 /________|
    v
```

### 4.2 Detailed Example
```
Given:
y = [0, 3, -5]
u = [1, -2, 4]

Step 1: Calculate y·u
y·u = (0×1) + (3×-2) + (-5×4) = 0 - 6 - 20 = -26

Step 2: Calculate u·u
u·u = 1² + (-2)² + 4² = 1 + 4 + 16 = 21

Step 3: Find parallel component
y_parallel = (-26/21)u = [-26/21, 52/21, -104/21]

Step 4: Find perpendicular component
y_orthogonal = y - y_parallel = [26/21, 11/21, -1/21]
```

### 4.3 Properties to Remember
1. w₁ is parallel to v
2. w₂ is perpendicular to v
3. u = w₁ + w₂
4. w₁ ⊥ w₂

## 5. Practice Problems & Applications

### 5.1 Common Applications
1. Physics
   - Force decomposition
   - Motion analysis
   - Gravity on slopes

2. Computer Graphics
   - 3D to 2D projection
   - Shadow calculations
   - Camera positioning

3. Data Analysis
   - Dimensionality reduction
   - Feature extraction
   - Principal Component Analysis

### 5.2 Practice Problem
```
Problem: Find the orthogonal projection of u = [2, 3] onto v = [1, 1]

Solution:
1. Calculate u·v = (2×1) + (3×1) = 5
2. Calculate ||v||² = 1² + 1² = 2
3. w₁ = (5/2)[1, 1] = [5/2, 5/2]
4. w₂ = [2, 3] - [5/2, 5/2] = [-1/2, 1/2]

Check: w₁·w₂ should equal 0
(-1/2)(5/2) + (1/2)(5/2) = -5/4 + 5/4 = 0 ✓
```

### 5.3 Key Study Tips
1. Always check orthogonality with dot product = 0
2. Draw vectors when possible to visualize relationships
3. Break complex problems into parallel/perpendicular components
4. Remember that unit vectors simplify calculations
5. Verify your answers using key properties


-----------------------------------------------------------------------
add notes from lecture :
0:00
in this video we'll talk about the
0:02
gram-schmidt process which is also
0:04
sometimes called gram-schmidt
0:05
orthogonalization so our goal for this
0:09
process is given a subspace of RN we'd
0:12
like to find an orthogonal or
0:13
orthonormal basis for W and the
0:16
gram-schmidt process allows us to start
0:17
with any basis for W and use it to
0:19
construct a new basis that is orthogonal
0:21
or orthonormal whichever one we want so
0:26
here's how the process works so we start
0:28
with a basis X 1 X 2 up through XP and
0:31
we assume that that's a basis for the
0:32
subspace W and then we're going to
0:34
construct new vectors which we'll call
0:36
these V 1 V 2 up through V P and this is
0:39
the way we're going to construct it so
0:40
starts off easy the first V 1 is just
0:42
the same as X 1 but then V 2 is X 2
0:46
minus X 2 dot V 1 divided by V 1 V 1
0:49
times B 1 so what I want you to
0:52
recognize is that this right here is the
0:54
projection of X 2 onto V 1 and so when
1:05
we subtract that what V 2 is is the
1:08
component of X 2 that's orthogonal to V
1:11
1 and so that's gonna guarantee two
1:14
things it's gonna guarantee that V 2 is
1:16
orthogonal to V 1 and it's also gonna
1:18
guarantee that the span of v1 and v2 is
1:21
the same as the span of X 1 and X 2 and
1:23
now when we move onto V 3 we're
1:26
subtracting both the projection of X 3
1:29
onto V 1 and also the projection of X 3
1:32
onto V 2 so we're taking away the
1:35
portions the components of X 3 that
1:37
point in the direction of V 1 or the
1:39
point in the direction of V 2 and so
1:41
what we'll remain after we subtract
1:43
those pieces is the component of X 3
1:45
that's orthogonal to both v1 and v2 and
1:48
so V 3 will be orthogonal to both V 1
1:51
and V 2 and we won't lose anything from
1:54
the span the span of v1 v2 and v3 will
1:57
be the same as the span of X 1 X 2 and X
1:59
3 and so on so when we finish this
2:02
process this V vectors will all be
2:04
orthogonal to each other and they'll
2:07
span the same subspace that the XS band
2:09
and so that's the theorem the theorem
2:12
says that when we do this construction
2:14
those V vectors form not just a basis
2:17
for W because we already had that but
2:18
this is an orthogonal basis for W now
2:22
what do we do if what we really wanted
2:24
was an orthonormal basis well in that
2:26
case all we do is first use the
2:28
gram-schmidt process to find an
2:29
orthogonal basis and then we just
2:31
normalize each vector to obtain an
2:33
orthonormal basis remember that to
2:35
normalize a vector you just divide it by
2:37
its length so you take the V vectors and
2:39
you look at the lengths of each of those
2:41
vectors and if that vector isn't already
2:43
a unit vector you divide that vector by
2:45
its length to create a unit vector 
