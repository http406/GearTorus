# GearTorus

The **GearTorus** is a 3D geometric shape that resembles a torus (a doughnut-shaped surface) but with a gear-like structure on its surface. The gear-like appearance is achieved by modulating the radius of the torus in a periodic manner, creating ridges and valleys that mimic the teeth of a gear.

### GearTorus Equation

The parametric equations used to define the GearTorus are:

![Image](https://github.com/user-attachments/assets/ad2e1918-6470-4296-91a4-a3843a347645)

### Explanation of the Code

1. **Parametric Equations in Code**:
   - The code iterates over the angles \( u \) and \( v \) to generate the vertices of the GearTorus.
   - For each combination of \( u \) and \( v \), the coordinates \( (x, y, z) \) are calculated using the parametric equations.
   - The varying minor radius \( r \) is computed using the modulation equation \( r = \frac{a \tanh(b \sin(nv))}{b} \).

2. **Vertices and Indices**:
   - The vertices are stored in an array and used to define the geometry of the GearTorus.
   - Indices are used to connect the vertices, forming lines or triangles to render the shape.

3. **Three.js Geometry and Material**:
   - The `THREE.BufferGeometry` is used to store the vertices and indices.
   - A `THREE.LineBasicMaterial` is used to render the GearTorus as a wireframe.

4. **Animation**:
   - The GearTorus is animated by rotating it around the \( x \) and \( y \) axes in the `animate` function.

### Constants in the Code

- \( R = 2.5 \): The major radius of the torus.
- \( a = 3.2 \): Controls the amplitude of the modulation.
- \( b = 2.6 \): Controls the sharpness of the gear teeth.
- \( n = 7 \): The number of gear teeth (lobes) around the torus.

The GearTorus is a visually interesting shape that combines the smoothness of a torus with the periodic structure of a gear. The parametric equations and modulation function create the gear-like appearance, and the code uses Three.js to render and animate this shape in 3D. The constants \( a \), \( b \), and \( n \) allow you to control the shape and number of gear teeth, making the GearTorus customizable for different visual effects.
