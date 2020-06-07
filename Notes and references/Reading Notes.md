# Reading Notes

***



## 6.3

### Cp1

1. *Application Program Interface*(API) is  a collection of functions to perform operations
   * Graphics API is part of using computer graphics libraries
   * Graphics API performs basic operations(drawing images and 3D surfaces into windows on screen)
2. Two graphics APIs 
   * Visual output -- visual output
   * User interface -- input from user
3. Two dominent approaches
   * Integrated approach -- Java
   * Separate approach -- OpenGL/Direct3D
4. 4D coordinate system
   * Manipulated by 4*4 matrices and 4-vectors
   * One of the most beautiful constructs in CS
   * Biggest intellectual hurdle to jump
5. Three "special" values for real numbers in IEEE floating-point
   * *Infinity $\infty$* 
   * *Minus infinity $-\infty$*
   * *Not a number $NaN$*
6. For $NaN$
   * Any arithmetic expression that includes NaN results in $NaN$
   * Any Boolean expression involving $NaN$ is false
7. Debugging method
   * Set a trap
   * Use asserts

### Lec4 

1. $$
   Linear\  Transform\ =\ Matrices
   \\ x'=ax+by\\y' = cx+dy
   \\ \begin{bmatrix} x'\\y'
   \end{bmatrix}=\begin{bmatrix}
   a&b\\c&d
   \end{bmatrix}\begin{bmatrix}
   x\\y
   \end{bmatrix}
   $$

2. $$
   Affine \ Transformation\\
   \begin{pmatrix}
   x'\\y'
   \end{pmatrix}=
   \begin{pmatrix}
   a&b\\c&d
   \end{pmatrix}
   \begin{pmatrix}
   x'\\y'
   \end{pmatrix}+
   \begin{pmatrix}
   t_x\\t_y
   \end{pmatrix}\\Homogenous \ Coordinate\\
   \begin{pmatrix}
   x'\\y'\\1
   \end{pmatrix}=\begin{pmatrix}
   a&b&t_x\\c&d&t_y\\0&0&1\\
   \end{pmatrix}.\begin{pmatrix}
   x\\y\\1
   \end{pmatrix}
   $$

3. 2D transformations

   * Scale $s_x,s_y$
   * Rotation $R_{\theta}$
   * Translation $T_{(x,y)}$ 

4. Transform ordering matters

   * Matrices are applied right to left

5. Two interpretations of a transform

   * Transform object
   * Transform coordinate system

----

## 6.4

### Cp2

1. $atan2(s,c)$ 
   * Takes an $s$ value propotional to $sinA$ and a $c$ value that scales $cosA$ by the same factor and returns A.
2. Implicit lines are useful for triangle rasterization
3. Ray 
   * All lines, line segments, rays
4. Linear interpolation 
   * most common mathematical operation in graphics
5. Triangles 
   * fundamental modeling primitive
   * 2D triangle with vertices $a,b,c$ used to set up a nonorthogonal coordinate system in which any point $p$ can be expressed as the following
     * $p(\alpha,\beta,\gamma)=\alpha a+\beta b+\gamma c$
     * $\alpha + \beta + \gamma=1$
6. Barycentric coordinate
   * Given a point $p$, a way to compute its barycentric coordinate
     * 1. Write equation $p(\alpha,\beta,\gamma)=\alpha a+\beta b+\gamma c$
       2. $\alpha + \beta + \gamma=1$ 

___

## 6.5

### Cp3

1. Raster display

   * Show images as rectangular array of pixels

2. Raster image 

   * A 2D array that stores the pixel value for each pixel

3. Vector image

   * By storing description of shapes
   * Amouts to storing the instructions for displaying the image rather the pixels needed to display it
   * Resolution independent

4. Raster devices

   * Output: display, hardcopy
   * Input: 2D array sensor, 1D array sensor

5. Images stored with floating-point numbers

   * High dynamic range(HDR)--wide range of values
   * Low dynamic range(LDR)--fixed range of values

6. Two key issues for producing correct images on monitors

   * Monitors are nonlinear with respect to input
     display intensity = (maximum intensity)$a^\gamma$ 

     > $a$ is the input value
     > $\gamma$ is to characterize nonlinearity

7. The $\alpha$ value for all pixels in an image might be stored as a fourth channel in an RGB image, in which case it's called *alpha channel* and the image can be called an RGBA image

---

## 6.6

### Cp8.1-8.3

1. the second major approach to render
   * Drawing objects one by one onto the screen/$object-order\ rendering/rendering\ by\ rasterization$
2. $Rasterization$
   * The processing of finding all pixels in an image that are occupied by geometric primitive
3. $graphics\ pipeline$ 
   * Starting with objects and ending by updating pixels in the image
4. Two examples of graphics pipeline
   * ***Hardware pipeline*** is used to support interactive rendering via APIs 
   * ***Software pipelines*** is used support APIs in film industry
5. Four stages of pipeline
   * *Vertex processing*
   * *Rasterization*
   * *Fragment processing*
   * *Blending*
6. Two jobs of rasterizer
   * *enumerates* the pixels that are covered by the primitive 
   * *Interpolates* values(attributes) across the primitive
7. Output of the rasterizer is a set of *fragments*
8. *Gouraud* interpolation
   * The color at a point in the triangle with barycentric coordinate$$\\c=\alpha c_0+\beta c_1 + \gamma c_3$$
9. The most common way to rasterize triangle that avoids the order problem and eliminate holes
   * Pixels are drawn if and only if their centers are inside the triangle
10. Dealing with pixels on triangle edges
    * *Worst* -- not draw the pixel
    * *Better* -- have both triangles draw
    * *Better than Better* -- one of the triangles draw
11. One approach
    * The edge which off-screen point is on
12. Two  common approaches for implementing clipping
    * Using six planes that bound the truncated viewing pyramid
    * in the 4D transformed space before the homogeneous divide
13. Before a primitive can be rasterized 
    * The vertices that define it must be in screen coordinates
    * Attributes must be known
14. Date preparing is the job of *vertex precessing stage* of the pipeline
    * Vertices are transformed, mapped
    * Other information is transformed 
15. Simple 2D drawing
    * Does nothing in the *vertex* and *fragment* stage
    * The value of fragment overwrites the value of the previous one in the blending stage
    * Direct supply primitives in the pixel coordinates
16. *z-buffer* algorithm
    * Add a value *z* as depth
    * Track the distance to the closest surface
    * Throw away fragments that are farther away
17. * Per-vertex shading
      * perform in vertex stage, computes shading once for each vertex and never in between vertices
    * Per-fragment shading
      * Geometric information needed for shading is passed through the rasterizer as attributes

---

## 6.7

### Cp9

1. Property of convolution
   * *a* is the sequence
   * *b* provides the weights