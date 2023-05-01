Download Link: https://assignmentchef.com/product/solved-cap4730-assignment-1-ray-tracing
<br>
<h1>Goal of this exercise</h1>

In this exercise you will write a raytracer, and use it to render spheres and more complex triangulated surfaces.

Eigen

In all exercises you will need to do operations with vectors and matrices. To simplify the code, you will use <a href="http://eigen.tuxfamily.org/">Eigen</a><a href="http://eigen.tuxfamily.org/">.</a> Have a look at the <a href="http://eigen.tuxfamily.org/dox/GettingStarted.html">”Getting Started”</a> page of Eigen as well as the <a href="http://eigen.tuxfamily.org/dox/group__QuickRefPage.html">Quick Reference</a> page for a reference of the basic matrix operations supported.

Submission

Follow the instructions by TA.

Questions

We advise all non-private questions be posted on <a href="https://github.com/FSU-ComputerGraphics/CAP4730-Spring19/issues">https://github.com/FSU-ComputerGraphics/ </a><a href="https://github.com/FSU-ComputerGraphics/CAP4730-Spring19/issues">CAP4730-Spring19/issues</a> as reference for all students. For other questions, please email or come to the office hours.

<h1>1           Mandatory Tasks</h1>

For each tasks below, add at least one image in the readme demonstrating the results. The code that you used for all tasks should be provided.

Xifeng Gao                                                                                                                                                                                        1

January 21, 2019

1.1        Ray Tracing Spheres

Modify the given program to support the rendering of multiple spheres in general position. Note that the provided code is only an example and the collision code that it uses is not general. You need to reimplement it from scratch. For this step, use simple Lambertian shading.

1.2      Shading

Extend your ray tracer to support ambient and specular lighting. Render a scene with multiple spheres with different colors and different material properties (one sphere should be purely diffuse, another one specular). Add a second light source to your scene.

1.3        Perspective Projection

Extend your ray tracer to support perspective projection, and re-render the scenes you created in the previous tasks, showing the difference between the two projections.

1.4         Ray Tracing Triangle Meshes

Extend your ray tracer to load meshes in <a href="https://en.wikipedia.org/wiki/OFF_(file_format)">off format</a><a href="https://en.wikipedia.org/wiki/OFF_(file_format)">.</a> Load the two meshes provided in the <em>data </em>folder and add them to your scene. Render them with different colors. Suggestion: You can store your mesh with two Eigen arrays V and F. V is a float array (dimension #V × 3 where #V is the number of vertices) that contains the positions of the vertices of the mesh, where the i-th row of V contains the coordinates of the i-th vertex. F is an integer array (dimension #faces × 3 where #F is the number of faces) which contains the descriptions of the triangles in the mesh. The i-th row of F will contain the indices of the vertices in V that form the i-th face, sorted counter-clockwise.

1.5      Shadows

Add shadows to the previous scene.

1.6        Reflections on the floor

Add a mirror that reflects all objects in the scene. To simplify this task, you can simply transform the entire ”floor” of the scene into a mirror.

Optional Tasks.

These tasks are optional. Each one of these tasks is worth 2.0% of the final grade.

Xifeng Gao                                                                                                                                                                                        2

January 21, 2019

1.7       Parallelization

Each pixel of the scene can be rendered independently. Integrate <a href="https://www.threadingbuildingblocks.org/">Intel TBB</a> in your project and use the <em>parallel for </em>to distribute the computation over all the available cores.

1.8       Animation

Create a simple animation by rendering multiple frames while moving the position of the camera and of the light source.

Xifeng Gao                                                                                                                                                                                        3

January 21, 2019