# Theory questions
**Unit 1: Introduction**

1. **Advantages of Computer Graphics and Areas of Applications**
    
    - What are the primary advantages of using computer graphics in modern technology?
    - Discuss various application areas where computer graphics are extensively utilized.
2. **Hardware and Software for Computer Graphics**
    
    - Describe the essential hardware components required for computer graphics.
    - Explain different display technologies used in computer graphics.
3. **Random Scan Display System**
    
    - What is a Random Scan Display System? How does it differ from Raster Scan Display Systems?
    - Describe the role of a Video Controller in a Random Scan Display System.
    - Explain the function of a Random Scan Display Processor.
4. **Raster Graphics**
    
    - Define Raster Graphics. How do they differ from Vector Graphics?
5. **Scan Conversion Algorithms**
    
    - Explain the Digital Differential Analyzer (DDA) algorithm for line drawing.
    - Describe the Bresenham's line drawing algorithm.
    - How is the Midpoint Circle Algorithm used to draw circles in computer graphics?
    - Discuss the algorithm for drawing an ellipse using the Midpoint method.
6. **Area Filling and Clipping**
    
    - Describe the Flood Fill and Boundary Fill algorithms for area filling.
    - Explain the Sutherland-Hodgman algorithm for polygon clipping.
    - How is line clipping performed using the Cohen-Sutherland algorithm?
    - Discuss the challenges involved in clipping circles and ellipses.

**Unit 2: Two-Dimensional and Three-Dimensional Transformations**

1. **2-Dimensional Transformation**
    
    - What are the basic transformations in 2D graphics?
    - Explain the concept of Homogeneous Coordinates in 2D transformations.
2. **2-D Translation, Rotation, Scaling**
    
    - How is translation applied to a 2D object? Provide the transformation matrix.
    - Describe the process of rotating a 2D object about the origin.
    - Explain how scaling affects a 2D object. What is the significance of the scaling factors?
3. **Reflection and Shear Transform**
    
    - What is reflection in 2D graphics? Provide examples with transformation matrices.
    - Describe shear transformation and its effect on 2D objects.
4. **3-Dimensional Transformation**
    
    - List and explain the basic transformations in 3D graphics.
5. **3-D Translation, Rotation, Scaling, Reflection, Shear**
    
    - How is translation applied to a 3D object? Provide the transformation matrix.
    - Describe the process of rotating a 3D object about the principal axes.
    - Explain scaling in 3D and its impact on objects.
    - What is reflection in 3D graphics? Provide examples with transformation matrices.
    - Describe shear transformation in 3D and its applications.

**Unit 3: Clipping**

1. **Window to Viewport Transformation**
    
    - Explain the concept of window to viewport transformation in computer graphics.
    - Derive the formula for window to viewport transformation.
2. **Clipping**
    
    - What is clipping in computer graphics, and why is it necessary?
3. **Line Clipping**
    
    - Describe the Cohen-Sutherland line clipping algorithm.
    - Explain the Liang-Barsky line clipping algorithm and compare it with Cohen-Sutherland.
4. **Polygon Clipping**
    
    - Discuss the Sutherland-Hodgman polygon clipping algorithm.
    - What challenges arise in polygon clipping, and how are they addressed?

**Unit 4: Visible Surface Determination and Computer Graphics Algorithms**

1. **Image Space and Object Space Techniques**
    
    - Differentiate between image space and object space techniques for visible surface determination.
2. **Hidden Surface Removal**
    
    - Explain the Depth Comparison method for hidden surface removal.
    - Describe the Z-Buffer algorithm and its implementation.
    - What is Back-Face Removal, and how is it used in rendering?
    - Discuss the Painter's Algorithm for hidden surface removal.
    - Explain the Scan-Line algorithm and its application in visible surface determination.
3. **Light and Color Models**
    
    - Describe the RGB color model and its use in computer graphics.
    - Explain the CMY color model and how it differs from RGB.
    - What is the YIQ color model, and where is it commonly used?

**Unit 5: Animation and Virtual Reality**

1. **Basic Principles of Animation and Types of Animation**
    
    - What are the fundamental principles of animation?
    - Discuss different types of animation used in computer graphics.
2. **Introduction to the Flash Interface**
    
    - Describe the main components of the Flash interface used for animation.
3. **Setting Stage Dimensions, Working with Panels, Panel Layouts**
    
    - How do you set stage dimensions in Flash?
    - Explain the importance of panels and panel layouts in the animation workflow.
4. **Layers & Views**
    
    - What is the role of layers in animation?
    - How do different views assist in the animation process?
5. **Shaping Objects**
    
    - Provide an overview of shape tools available in Flash.
    - How can shapes be drawn and modified for animation purposes?
6. **Bitmap Images & Sounds**
    
    - Discuss the integration of bitmap images into animations.
    - How is sound incorporated and synchronized in animations?
7. **Animation Techniques**
    
    - Explain frame-by-frame animation and its applications.
    - What is tweening, and how does it facilitate animation?
    - Describe the use of masks in creating animation effects.
8. **Introduction to Virtual Reality**
    
    - Define Virtual Reality (VR) and its key components.
    - Discuss the applications of VR in various industries.

# Numerical questions:
**Unit 1: Introduction**

1. **Scan Conversion Algorithms**
    
    - _Line Drawing using DDA Algorithm_: Calculate the intermediate points to draw a line from (2, 3) to (10, 8) using the Digital Differential Analyzer (DDA) algorithm.
    - _Circle Drawing using Midpoint Algorithm_: Determine the points needed to draw a circle with a radius of 5 units centered at the origin using the Midpoint Circle Algorithm.
2. **Area Filling**
    
    - _Flood Fill Algorithm_: Given a 10x10 grid with a boundary defined by specific cells, apply the flood fill algorithm starting from a given interior point to fill the area.
3. **Clipping**
    
    - _Cohen-Sutherland Line Clipping_: Clip a line segment from (5, 5) to (15, 15) against a rectangular clipping window defined by (xmin=0, ymin=0) and (xmax=10, ymax=10) using the Cohen-Sutherland algorithm.

**Unit 2: Two-Dimensional and Three-Dimensional Transformations**

1. **2D Transformations**
    
    - _Translation_: Translate a point (3, 4) by (dx=5, dy=-2). Calculate the new coordinates.
    - _Rotation_: Rotate a point (4, 5) by 90 degrees counterclockwise about the origin. Determine the new position.
    - _Scaling_: Scale a rectangle with vertices at (1,1), (1,3), (4,1), and (4,3) by factors of 2 in the x-direction and 3 in the y-direction. Find the new vertex coordinates.
2. **3D Transformations**
    
    - _Rotation about the Z-axis_: Rotate a point (2, 3, 4) by 45 degrees around the Z-axis. Compute the new coordinates.
    - _Scaling_: Scale a cube with vertices at (±1, ±1, ±1) by a factor of 2 in all directions. Determine the coordinates of the scaled cube.

**Unit 3: Clipping**

1. **Line Clipping**
    
    - _Cohen-Sutherland Algorithm_: Clip a line segment from (12, 5) to (4, 15) against a clipping window with corners at (xmin=0, ymin=0) and (xmax=10, ymax=10). Identify the visible portion of the line.
2. **Polygon Clipping**
    
    - _Sutherland-Hodgman Algorithm_: Clip a polygon with vertices at (2, 2), (8, 2), (8, 8), and (2, 8) against a rectangular clipping window defined by (xmin=4, ymin=4) and (xmax=6, ymax=6). Determine the vertices of the clipped polygon.

**Unit 4: Visible Surface Determination and Computer Graphics Algorithms**

1. **Z-Buffer Algorithm**
    
    - Given two overlapping triangles in 3D space with specified vertex coordinates and depth values, apply the Z-buffer algorithm to determine which triangle's surface is visible at a particular pixel.
2. **Color Models**
    
    - _RGB to CMY Conversion_: Convert an RGB color with values (R=100, G=150, B=200) to its equivalent CMY representation.

**Unit 5: Animation and Virtual Reality**

1. **Frame-by-Frame Animation**
    
    - Calculate the number of frames required to animate an object moving from position (0,0) to (10,10) over 2 seconds, given a frame rate of 30 frames per second.
2. **Tweening**
    
    - Determine the intermediate positions of an object for a linear tween between (5,5) and (15,15) over 5 frames.