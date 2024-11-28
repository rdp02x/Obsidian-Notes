## 1. What is ActionScript? Write an ActionScript for a Login Page to validate a user’s Login.

**ActionScript** is an object-oriented programming language used primarily for the development of websites and software targeting the Adobe Flash platform. It is mainly used for creating interactive applications, games, and multimedia.

**ActionScript for Login Page Validation:**
```actionscript
// ActionScript code to validate login credentials
usernameInput.addEventListener(Event.CHANGE, validateInput);
passwordInput.addEventListener(Event.CHANGE, validateInput);
loginButton.addEventListener(MouseEvent.CLICK, validateLogin);

var validUsername:String = "user123";
var validPassword:String = "pass123";

function validateInput(e:Event):void {
    if (usernameInput.text != "" && passwordInput.text != "") {
        loginButton.enabled = true;
    } else {
        loginButton.enabled = false;
    }
}

function validateLogin(e:MouseEvent):void {
    if (usernameInput.text == validUsername && passwordInput.text == validPassword) {
        output.text = "Login Successful!";
    } else {
        output.text = "Invalid Username or Password";
    }
}
```

## 2. Explain Back-face Removal Method.

**Back-face Removal** is a method used in 3D computer graphics to improve rendering efficiency by eliminating polygons (faces) that are not visible to the viewer. These faces are called back-faces, and since they face away from the camera, they don’t contribute to the final image.

**Steps in Back-face Removal:**
1. **Normal Calculation:** Calculate the normal vector for each face.
2. **Dot Product:** Compute the dot product between the normal vector and the view vector.
3. **Visibility Check:** If the dot product is negative, the face is visible. If positive, the face is a back-face and can be discarded.

**Advantages:**
- Reduces the number of polygons to be rendered.
- Improves overall rendering performance.

## 3. What is the importance of color space in image processing? Explain 4 different color models.

**Color space** is important in image processing because it provides a way to represent colors numerically, allowing for the manipulation, analysis, and display of colors in images.

**Importance of Color Space:**
- Facilitates color comparison.
- Enables color correction and enhancement.
- Assists in color segmentation for object detection and tracking.

**Different Color Models:**
1. **RGB (Red, Green, Blue):**
   - Based on combining red, green, and blue light to create a wide spectrum of colors.
   - Used in digital displays like monitors, televisions, and cameras.
   
2. **CMYK (Cyan, Magenta, Yellow, Black):**
   - Subtractive color model used in color printing.
   - Cyan, magenta, and yellow are combined to produce colors; black (K) is added for depth and detail.

3. **HSV (Hue, Saturation, Value):**
   - Hue represents color, saturation represents the intensity of the color, and value represents brightness.
   - Used in image editing software for easier manipulation of colors.

4. **YCbCr:**
   - Used in video compression and broadcasting.
   - Y represents the brightness (luminance), while Cb and Cr represent chrominance (color information).

## 4. 
![[WhatsApp Image 2024-09-15 at 23.31.32.jpeg]]
   
## 5. Explain, giving an example, the Cohen-Sutherland Line Clipping Algorithm.

**Cohen-Sutherland Line Clipping Algorithm** is used to clip lines within a rectangular clipping window. It assigns outcodes to endpoints of the line, determines the visibility of the line based on the outcodes, and clips accordingly.

**Steps:**
1. **Assign Outcodes:** For each endpoint, assign a 4-bit outcode that represents whether the point lies inside or outside the clipping window.
2. **Check Trivial Acceptance or Rejection:** 
   - If both endpoints have outcodes of 0000, the line is trivially accepted.
   - If the logical AND of both outcodes is non-zero, the line is trivially rejected.
3. **Clip Line:** If the line is partially outside, calculate the intersection points with the clipping boundaries and update the endpoints.

**Example:**
For a line with endpoints (x1, y1) and (x2, y2), the algorithm computes outcodes, checks if the line is inside or outside, and clips if necessary. The line segment is drawn only within the window.

## 6. Explain Color Models RGB and HSV stating their implementation and use.

**RGB (Red, Green, Blue) Color Model:**
- RGB is an additive color model where colors are created by combining red, green, and blue light.
- Used in displays like monitors, TVs, and cameras.
- Colors are represented as a combination of three values (R, G, B), each ranging from 0 to 255.

**HSV (Hue, Saturation, Value) Color Model:**
- HSV represents colors in a cylindrical geometry where:
   - **Hue**: The type of color (0° to 360° around the color wheel).
   - **Saturation**: The intensity or purity of the color (0% to 100%).
   - **Value**: The brightness or lightness of the color (0% to 100%).

**Implementation and Use:**
- **RGB** is used in digital devices for displaying images because screens emit light.
- **HSV** is preferred in image editing software as it allows for more intuitive control over colors by separating chromatic content from intensity.

## 7. Explain the concept of Perspective Projection. How is it used to create a sense of depth in 3D scenes?

**Perspective Projection** is a method used in 3D graphics to project 3D objects onto a 2D plane (such as a screen) in a way that simulates depth, making objects farther from the viewer appear smaller.

**Concept:**
- It uses a **vanishing point** where parallel lines seem to converge.
- Objects are scaled according to their distance from the viewpoint, creating a realistic depiction of depth.

**Mathematical Representation:**
- The projection of a point (x, y, z) onto the 2D plane can be calculated as:
  $$
  x' = \frac{x}{z}, \quad y' = \frac{y}{z}
  $$
  where \( z \) is the distance from the viewpoint.

**Use in 3D Scenes:**
- In video games, perspective projection is used to create realistic 3D environments, making distant objects appear smaller and closer objects larger.

## 8. Explain the difference between timeline animation and motion tweening in Adobe Flash. Provide examples of when each technique would be used.

**Timeline Animation:**
- **Timeline Animation** involves creating a series of frames that show the object in different positions or states, and then playing them in sequence to create animation.
- Example: Frame-by-frame animation where a character changes position or expression in each frame. Used when you need full control over each frame.

**Motion Tweening:**
- **Motion Tweening** automates the process of animating an object from one position to another by defining the starting and ending positions. Flash automatically generates the intermediate frames.
- Example: Moving an object from one side of the screen to the other. Used when you need smooth transitions, like animating a moving car or ball.

**Key Differences:**
- **Timeline Animation** requires manually creating each frame.
- **Motion Tweening** generates the in-between frames, making it more efficient for simple, smooth movements.
