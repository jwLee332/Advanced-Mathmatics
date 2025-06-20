Using MATLAB's PDE Toolbox, a basic geometry for defining a Noise Barrier in a two-dimensional space was constructed. 
Each code creates a wall with a thickness of 0.1 m and a height of 5 m. 
This barrier is used to analyze diffraction and reflection effects in sound wave simulation, and has the advantage of being able to observe complex wave phenomena separately through a simple structure.

In the PDE Toolbox, geometric shapes are defined using a unique format. 
For example, a vector starting with R = [3, 4, ...] represents a rectangle, followed by four x-coordinates and four y-coordinates that specify the positions of its vertices. 
To construct a noise barrier with a curved shape, the curved section is approximated by dividing it into ten small rectangular regions. 
The defined geometric data is stored in gd (geometry description matrix), while the names of each shape are specified as a character array called ns.
The sf element, or set formula, is a string that describes how these shapes are combined.

These three components (gd, ns, and sf) are processed using the decsg function, which converts them into a format usable by the PDE Toolbox. 
Finally, the geometry is applied to the PDE model object using the geometryFromEdges function, allowing the shape to be visualized and analyzed.
