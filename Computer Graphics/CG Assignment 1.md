### 1. Define the following:

###### Resolution
- **Resolution** refers to the number of distinct pixels displayed on a screen or captured in a digital image, expressed as width x height (e.g., 1920x1080). Higher resolution means greater detail.
###### Pixel
- **Pixel** is the smallest unit of a digital image or display, representing a single point in a graphic. A combination of many pixels forms an image, each having color and brightness information.
###### Frame Buffer
- **Frame Buffer** is a dedicated memory area that stores the color and intensity values of pixels for an image or video frame. It is continuously updated to render images on the display.
###### Transformation
- **Transformation** in computer graphics involves changing the position, size, orientation, or shape of objects. Basic transformations include translation, scaling, rotation, and shearing.

### 2. Given the centre point coordinates (4, -4) and radius as 10, generate all the points using Mid Point Circle Drawing Algorithm to form a circle.

**Given:**
- Center: (4, -4)
- Radius: 10

**Midpoint Circle Drawing Algorithm:**
1. **Initialize:**
   - Starting point: (x, y) = (0, 10)
   - Decision parameter: \( p = 1 - \text{radius} \) = -9

2. **Loop until \( x \leq y \):**
   - Plot (x, y) in all octants relative to the center.
   - If \( p < 0 \):
     - Increment x: \( x = x + 1 \)
     - Update decision parameter: \( p = p + 2x + 1 \)
   - Else:
     - Increment x and decrement y: \( x = x + 1 \), \( y = y - 1 \)
     - Update decision parameter: \( p = p + 2x - 2y + 1 \)

**Points:**
- **Initial values:** \( x = 0 \), \( y = 10 \)
  - Plot points: (4, 6), (14, -4), (-6, -4), (4, -14)
- **Iteration 1:** 
  - Decision parameter \( p = -9 \)
  - \( x = 1 \), \( y = 10 \)
  - Plot points: (5, 6), (13, -4), (-5, -4), (3, -14)
- **Iteration 2:** 
  - \( p = -6 \)
  - \( x = 2 \), \( y = 10 \)
  - Plot points: (6, 6), (12, 6), (-4, -4), (2, -14)

Continue until \( x > y \).

### 3. Calculate the points using DDA Algorithm that would be plotted for a line whose endpoints are (12, 10) and (20, 20).

**Given:**
- Endpoints: (12, 10) and (20, 20)

**DDA Algorithm:**
1. **Calculate differences:** \( \Delta x = 8 \); \( \Delta y = 10 \)
2. **Determine steps:** \( \text{Steps} = 10 \)
3. **Calculate increments:** 
   - \( x_{\text{increment}} = \frac{\Delta x}{\text{Steps}} = 0.8 \)
   - \( y_{\text{increment}} = \frac{\Delta y}{\text{Steps}} = 1.0 \)
4. **Initial point:** (12, 10)

**Points Calculation:**
1. **Point 1:** (12, 10)
2. **Point 2:** (12.8, 11)
3. **Point 3:** (13.6, 12)
4. **Continue** until reaching (20, 20)

### 4. What is 3D Shearing Transformation? Given a 3D triangle with points A(0, 0, 0), B(1, 1, 2) and C(1, 1, 3). Apply shear parameter 2 on X axis, 2 on Y axis and 3 on Z axis and find out the new coordinates of the object.

**Definition:**
- **3D Shearing Transformation** involves shifting the coordinates of each point by a proportion depending on the coordinates of other points.

**Shear Matrix:**
$$
\begin{bmatrix}
1 & 2 & 2 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$

**Original Coordinates:**
- A(0, 0, 0), B(1, 1, 2), C(1, 1, 3)

**New Coordinates Calculation:**
1. **Point A:** (0, 0, 0)
2. **Point B:** 
   $$
   \begin{bmatrix}
   1 \\
   1 \\
   2 \\
   \end{bmatrix}
   +
   \begin{bmatrix}
   1 & 2 & 2 \\
   0 & 1 & 0 \\
   0 & 0 & 1 \\
   \end{bmatrix}
   \begin{bmatrix}
   1 \\
   1 \\
   2 \\
   \end{bmatrix}
   =
   \begin{bmatrix}
   7 \\
   1 \\
   2 \\
   \end{bmatrix}
   $$
3. **Point C:** 
   $$
   \begin{bmatrix}
   1 \\
   1 \\
   3 \\
   \end{bmatrix}
   +
   \begin{bmatrix}
   1 & 2 & 2 \\
   0 & 1 & 0 \\
   0 & 0 & 1 \\
   \end{bmatrix}
   \begin{bmatrix}
   1 \\
   1 \\
   3 \\
   \end{bmatrix}
   =
   \begin{bmatrix}
   9 \\
   1 \\
   3 \\
   \end{bmatrix}
   $$

**New Coordinates:**
- A'(0, 0, 0), B'(7, 1, 2), C'(9, 1, 3)

### 5. Find the new coordinates of a triangle A (0, 0), B (1,1),C (5,2) after it has been reduced to half of its size?

**Original Triangle:**
- A(0, 0), B(1, 1), C(5, 2)

**Scaling Transformation:**
- **Scaling Factor:** \( S = 0.5 \)
- **Scaling Matrix:** 
$$
\begin{bmatrix}
0.5 & 0 & 0 \\
0 & 0.5 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$

**New Coordinates Calculation:**
1. **Point A:** (0, 0)
2. **Point B:** (0.5, 0.5)
3. **Point C:** (2.5, 1)

**New Coordinates:**
- A'(0, 0), B'(0.5, 0.5), C'(2.5, 1)

### 6. Draw and explain the construction and working of CRT. Also write its advantages and disadvantages.

**Construction:**
1. **Electron Gun:** Produces a beam of electrons.
2. **Control Grid:** Controls the flow of electrons by adjusting the potential difference.
3. **Focusing System:** Focuses the electron beam to a fine point.
4. **Deflection System:** Controls the direction of the electron beam.
   - **Electrostatic Deflection:** Uses electric fields.
   - **Magnetic Deflection:** Uses magnetic fields.
5. **Phosphor-Coated Screen:** Emits visible light when struck by electrons.

**Working:**
- The electron gun emits electrons, which are accelerated and focused into a beam.
- The control grid regulates the number of electrons and their intensity.
- The deflection system directs the beam to specific points on the screen.
- The beam strikes the phosphor-coated screen, producing light and creating an image.

**Advantages:**
- High color accuracy and contrast ratio.
- Capable of displaying multiple resolutions.
- Fast response time and low motion blur.

**Disadvantages:**
- Large and bulky.
- Consumes more power compared to modern displays.
- Susceptible to magnetic interference.

### 7. Differentiate between Vector Display and Raster Display.

**Table: Vector Display vs. Raster Display**

| **Feature**                | **Vector Display**                                      | **Raster Display**                                    |
|----------------------------|--------------------------------------------------------|------------------------------------------------------|
| **Image Representation**   | Lines and curves (vectors)                             | Grid of pixels                                       |
| **Screen Rendering**       | Electron beam traces lines (stroke writing)            | Electron beam scans pixels row by row (raster scanning) |
| **Memory Usage**           | Less memory required                                   | More memory required                                 |
| **Resolution and Scaling** | Resolution-independent; scalable without quality loss | Resolution-dependent; may lose quality when scaled   |
| **Application**            | Used in specialized devices like oscilloscopes         | Common in modern monitors, TVs, and smartphones      |

### 8. Discuss 2D transformations with its basic types along with example.

**2D Transformations:**
1. **Translation:** Shifting an object from one position to another.
   - **Matrix:** 
$$
\begin{bmatrix}
1 & 0 & Tx \\
0 & 1 & Ty \\
0 & 0 & 1 \\
\end{bmatrix}
$$
   - **Example:** Moving a point (2, 3) by Tx = 4, Ty = 5 results in (6, 8).

2. **Scaling:** Changing the size of an object.
   - **Matrix:** 
$$
\begin{bmatrix}
Sx & 0 & 0 \\
0 & Sy & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$
   - **Example:** Scaling a point (1, 1) by Sx = 2, Sy = 3 results in (2, 3).

3. **Rotation:** Rotating an object about a point.
   - **Matrix:** 
$$
\begin{bmatrix}
\cos \theta & -\sin \theta & 0 \\
\sin \theta & \cos \theta & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$
   - **Example:** Rotating a point (1, 0) by 90° results in (0, 1).

4. **Shearing:** Distorting an object by shifting its points in one direction.
   - **Matrix (X-Shear):** 
$$
\begin{bmatrix}
1 & Shx & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$
   - **Example:** Shearing a point (1, 1) with Shx = 2 results in (3, 1).
