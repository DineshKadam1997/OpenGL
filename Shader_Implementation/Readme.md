OpenGL Shader Implementation
Overview
This graphical application, implemented in C++ using the Qt framework and OpenGL for rendering, functions as a visualization tool to illustrate the workings of Computer-Aided Geometric Design (CAGD) algorithms.

Algorithms and Equations
Sutherland Line Clipping Algorithm
The Sutherland-Hodgman line clipping algorithm efficiently determines and outputs the visible portion of a line segment within a specified rectangular window in computer graphics.

Bezier Curve
A Bézier curve is a smooth curve defined by control points, commonly used in computer graphics and design. Its shape is influenced by the positions of these points, and it comes in various degrees, with quadratic and cubic being most common.

Hermite Curve
A Hermite curve is a type of spline curve defined by two points and their associated tangent vectors. It is commonly used in computer graphics and computer-aided design to create smooth and predictable curves. The curve interpolates the given points and follows the specified tangent vectors at those points, providing control over both position and direction along the curve.

BSpline Curve
A B-spline curve is a smooth and flexible mathematical curve defined by control points and basis functions, widely used in computer graphics and design for its local control and versatility in approximating complex shapes.

File Structure
Libraries
SutherlandAndCohenAlgo.lib

Includes sutherlandAndCohenAlgo.h and sutherlandAndCohenAlgo.cpp
Bezier.lib

Includes Bezier.h and Bezier.cpp
Hermite.lib

Includes Hermite.h and Bezier.cpp
BSpline.lib

Includes BSpline.h and BSpline.cpp
Geometry.lib

Includes various geometry classes:
Point3D.h and Point3D.cpp
Line.h and Line.cpp
Rectanglee.h and Rectanglee.cpp
Visualizer App
Visualizer.h and Visualizer.cpp

GUI components are implemented in these files.
OpenGLWindow.h and OpenGLWindow.cpp

Responsible for handling OpenGL rendering.
main.cpp

Entry point for the application, initializes and runs the graphical line clipping tool.
Sharing Implementation
Added button "Sharing" in GUI.

Defined two connectors setSharingFactor in Visualizer.cpp, passes rotation, translation, and scaling factor to OpenGLWindow.cpp.

Defined setSharingFactor function.

Created QMatrix4x4 scaleMatrix; to scale drawing.

Created QMatrix4x4 translateMatrix; to translate drawing.

Created QMatrix4x4 rotateMatrix; to rotate drawing.

Updated vertexShader.glsl.
