# CSCI 4810 Final Project
## RayTracer using WebGPU
I built a ray tracer that runs on the GPU with options to customize the scene, camera, lighting, and the ray tracing Bounding Volume Hierarchy (BVH). It allows controlling camera position and rotation when the canvas is clicked. W,A,S,D keys move the camera along the x-z axis, space moves it up, C or ctrl moves it down.
It has two scenes: each scene has a square floor (represented as two triangles) and a number of spheres. Scene 1 has six spheres with different properties and positions. Scene 2 can allow a variable number of spheres- it has a sphere count slider to control the number of spheres, each with random properties. There is also a controls panel on the left that allows controlling the position, radius, color, and material properties of each sphere, as well as the width, color, and checkerboard pattern for the floor (quad 0). The floor is also customizable: can switch between checkerboard and flat color. The UI can also show the FPS (frames per second) and ms per frame (SPF = 1 / FPS). One can also toggle the bounding hierarchy visual, which shows the actual hierarchy of bounding boxes color coded based on depth, with boxes at the root being red, and leaf nodes being green, and nodes in between root and leaves interpolated between (red to orange). Also, one can toggle on temporal accumulation which stores cumulative frame buffers so that when averaged out in the compute shader, it removes the noise.
### How to Run
This project was built using typescript and requires node.js or npm to run

How to run:
go to directory with index.html 
run $ npm install
then $ npm run dev
then go to browser 
on http://localhost:5173 

Alternatively: if you dont have node.js or npm
I used a library that allows packaging this project into a single index.html file
drag the index.html from the dist directory into the browser or double click on the file.


How to move in scene:
hold left click on canvas,
look using mouse, 
W A S D for x-z plane movement, 
C or ctrl to go down,
space to go up