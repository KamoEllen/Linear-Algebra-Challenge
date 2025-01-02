# Linear Algebra: Coordinate Systems & Basis Vectors

## 1. What is a Coordinate System?

A coordinate system is a way to track points in space using basis vectors. It provides instructions for how to reach any point using combinations of basis vectors.

### Standard Coordinate System:
- Uses standard basis vectors: 
  - e₁ = (1,0) → one step right
  - e₂ = (0,1) → one step up
- Example: Point (2,-2) means:
  - 2 steps along e₁
  - -2 steps along e₂

## 2. Alternative Basis Vectors

Any pair of vectors can form a basis if they are:
1. Linearly independent (can't make one from the other)
2. Span the space (can reach any point)

### Example of New Basis:
```
v₁ = (1,0)
v₂ = (1,2)
```

The same point can be written differently in each basis:
- Standard basis: (2,-2)
- New basis: (3,-1)

## 3. Important Notation

For vector x written in different bases:
- Standard basis: x = (2,-2)
- B-basis: x_B = (3,-1)
- Formal notation: x_ℰ for standard basis

## 4. Converting Between Bases

### Method:
1. Create matrix P_B using basis vectors as columns
2. For vector x in standard basis to B-basis:
   - x_B = P_B^(-1) × x

### Example:
```
Given basis B: [(1,1), (-2,1)]
To convert (4,1) to B-basis:

1. P_B = [1  -2]
         [1   1]

2. P_B^(-1) × (4,1) = (2,-1)
```

## 5. Grid Systems

### Properties:
- Created by integer combinations of basis vectors
- Grid lines represent fixed integer steps along one basis vector
- Intersection points are integer combinations of both vectors

### Types:
1. Standard Grid:
   - Vertical and horizontal lines
   - Regular square pattern

2. Alternative Basis Grid:
   - Skewed lines based on basis vectors
   - Creates parallelogram pattern

## 6. Applications in Higher Dimensions

- Useful for subspaces in R³
- When standard basis vectors don't lie in subspace
- Create coordinate system using basis vectors within subspace

### Example:
- Plane in R³
- Need two basis vectors lying in plane
- Grid lines follow basis vectors' directions

## Key Takeaways

1. Any basis can define a coordinate system
2. Same vector has different coordinates in different bases
3. Can convert between bases using matrix operations
4. Grid systems visualize integer combinations of basis vectors
5. Essential for understanding subspaces in higher dimensions
