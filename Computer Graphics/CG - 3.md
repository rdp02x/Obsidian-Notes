# 2D Transformations

## Reflection

### Reflection on X-Axis

- **Equations:**
  $$
  \begin{bmatrix}
  X' \\
  Y'
  \end{bmatrix}
  =
  \begin{bmatrix}
  X \\
  -Y
  \end{bmatrix}
  $$

- **Matrix Representation:**
  $$
  \begin{bmatrix}
  1 & 0 \\
  0 & -1
  \end{bmatrix}
  $$

### Reflection on Y-Axis

- **Equations:**
  $$
  \begin{bmatrix}
  X' \\
  Y'
  \end{bmatrix}
  =
  \begin{bmatrix}
  -X \\
  Y
  \end{bmatrix}
  $$

- **Matrix Representation:**
  $$
  \begin{bmatrix}
  -1 & 0 \\
  0 & 1
  \end{bmatrix}
  $$

### Reflection About the Origin

- **Equations:**
  $$
  \begin{bmatrix}
  X' \\
  Y'
  \end{bmatrix}
  =
  \begin{bmatrix}
  -X \\
  -Y
  \end{bmatrix}
  $$

- **Matrix Representation:**
  $$
  \begin{bmatrix}
  -1 & 0 \\
  0 & -1
  \end{bmatrix}
  $$

## Shear

### X-Shear

- **Equations:**
  $$
  \begin{bmatrix}
  X' \\
  Y'
  \end{bmatrix}
  =
  \begin{bmatrix}
  X + Sh_x \cdot Y \\
  Y
  \end{bmatrix}
  $$

- **Matrix Representation:**
  $$
  \begin{bmatrix}
  1 & Sh_x \\
  0 & 1
  \end{bmatrix}
  $$

### Y-Shear

- **Equations:**
  $$
  \begin{bmatrix}
  X' \\
  Y'
  \end{bmatrix}
  =
  \begin{bmatrix}
  X + Sh_y \cdot Y \\
  Y
  \end{bmatrix}
  $$

- **Matrix Representation:**
  $$
  \begin{bmatrix}
  1 & 0 \\
  Sh_x & 1
  \end{bmatrix}
  $$

### Example

Given a triangle with points \( (1, 1) \), \( (0, 0) \), and \( (1, 0) \):

- **Shearing Parameters:**
  - \( Sh_x = 2 \)
  - \( Sh_y = 2 \)

  **Shearing in X Axis:**

  - For \( A(1, 1) \):
    $$
    \begin{bmatrix}
    X' \\
    Y'
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 + 2 \cdot 1 \\
    1
    \end{bmatrix}
    =
    \begin{bmatrix}
    3 \\
    1
    \end{bmatrix}
    $$

  - For \( B(0, 0) \):
    $$
    \begin{bmatrix}
    X' \\
    Y'
    \end{bmatrix}
    =
    \begin{bmatrix}
    0 + 2 \cdot 0 \\
    0
    \end{bmatrix}
    =
    \begin{bmatrix}
    0 \\
    0
    \end{bmatrix}
    $$

  - For \( C(1, 0) \):
    $$
    \begin{bmatrix}
    X' \\
    Y'
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 + 2 \cdot 0 \\
    0
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 \\
    0
    \end{bmatrix}
    $$

  **Shearing in Y Axis:**

  - For \( A(1, 1) \):
    $$
    \begin{bmatrix}
    X' \\
    Y'
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 \\
    1 + 2 \cdot 1
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 \\
    3
    \end{bmatrix}
    $$

  - For \( B(0, 0) \):
    $$
    \begin{bmatrix}
    X' \\
    Y'
    \end{bmatrix}
    =
    \begin{bmatrix}
    0 \\
    0 + 2 \cdot 0
    \end{bmatrix}
    =
    \begin{bmatrix}
    0 \\
    0
    \end{bmatrix}
    $$

  - For \( C(1, 0) \):
    $$
    \begin{bmatrix}
    X' \\
    Y'
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 \\
    0 + 2 \cdot 1
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 \\
    2
    \end{bmatrix}
    $$

---

# 3D Transformations

3D transformations are essential for manipulating and visualizing three-dimensional objects in computer graphics. They allow for the movement, scaling, rotation, and shearing of objects in a 3D space.

## Translation

Translation moves an object from one position to another in 3D space.

- **Translation Equations:**
  $$
  \begin{bmatrix}
  x' \\
  y' \\
  z'
  \end{bmatrix}
  =
  \begin{bmatrix}
  x + T_x \\
  y + T_y \\
  z + T_z
  \end{bmatrix}
  $$

- **Matrix Representation:**
  $$
  \begin{bmatrix}
  1 & 0 & 0 & T_x \\
  0 & 1 & 0 & T_y \\
  0 & 0 & 1 & T_z \\
  0 & 0 & 0 & 1
  \end{bmatrix}
  $$

- **Example:**

  Given a 3D object with coordinates \( A(0, 3, 1) \), \( B(3, 3, 2) \), \( C(3, 0, 0) \), and \( D(0, 0, 0) \) with translation vector \( (T_x, T_y, T_z) = (1, 1, 2) \):

  - For \( A(0, 3, 1) \):
    $$
    \begin{bmatrix}
    x' \\
    y' \\
    z'
    \end{bmatrix}
    =
    \begin{bmatrix}
    0 + 1 \\
    3 + 1 \\
    1 + 2
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 \\
    4 \\
    3
    \end{bmatrix}
    $$

  - Similarly, calculate for \( B \), \( C \), and \( D \).

## Scaling

Scaling changes the size of an object in 3D space. Different scaling factors are applied along the X, Y, and Z axes.

- **Scaling Equations:**
  $$
  \begin{bmatrix}
  x' \\
  y' \\
  z'
  \end{bmatrix}
  =
  \begin{bmatrix}
  x \times S_x \\
  y \times S_y \\
  z \times S_z
  \end{bmatrix}
  $$

- **Matrix Representation:**
  $$
  \begin{bmatrix}
  S_x & 0 & 0 & 0 \\
  0 & S_y & 0 & 0 \\
  0 & 0 & S_z & 0 \\
  0 & 0 & 0 & 1
  \end{bmatrix}
  $$

**Steps for Scaling with Fixed Point (a, b, c):**

1. Scale the object relative to the origin.
2. Translate the object back to its original position.
3. Translate the fixed point to the origin.

## Rotation

Rotation changes the orientation of an object around the X, Y, or Z axis.

### Rotation Around X-Axis

- **Equations:**
  $$
  \begin{bmatrix}
  x' \\
  y' \\
  z'
  \end{bmatrix}
  =
  \begin{bmatrix}
  x \\
  y \cos \theta - z \sin \theta \\
  y \sin \theta + z \cos \theta
  \end{bmatrix}
  $$
