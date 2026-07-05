

https://github.com/user-attachments/assets/2afdd0ad-aa20-4150-ae99-3ab14c4f59d3

<h1>Autonomous Car Simulation with Neural Network AI.</h1>

This is a browser-based simulation where virtual cars attempt to drive autonomously on a road. The key idea is to train cars using a neural network, enabling them to steer clear of traffic and borders using sensor input.
</br>
<h3>🚗 Core Features</h3>
Self-driving cars using a neural network

Obstacle detection with simulated sensors

Learning via mutating models & saving best models

Interactive keyboard-controlled test car

</br>

<h3>🧠 Project Architecture</h3>
index.html: Sets up the canvas and loads all scripts

style.css: Styles the two canvases and buttons

main.js: Orchestrates the simulation: spawns cars, animates them, and handles saving/loading NN data

car.js: Core car logic including movement, collision detection, and AI behavior

sensor.js: Simulates sensors for obstacle detection

network.js: Implements a basic feedforward neural network

road.js: Draws roads and lane borders

controls.js: Enables manual car control using arrow keys

utils.js: Contains geometric functions and utilities

visualizer.js: Draws the neural network on screen

</br>

<h3>📘 Important JavaScript Concepts Covered</h3>

1. Object-Oriented Programming (OOP)
Use of ES6 class syntax for modular design (Car, Sensor, Road, Controls, NeuralNetwork, etc.)

   Constructor methods, private methods (#method()), instance properties, inheritance of responsibility across classes

2. Encapsulation and Private Methods
Modern JS feature # used for private functions like #createPolygon, #move, etc. in Car

3. Canvas API
Drawing cars, roads, sensor rays, and the neural network

   Transformations (e.g., translate, rotate) used for rotating/drawing cars based on direction

4. Animation Loop
requestAnimationFrame(animate) for smooth rendering

   Dynamic canvas resizing (canvas.height = window.innerHeight)

5. Collision Detection
   Geometry-based collision detection using polygons and intersections (getIntersection(), polysIntersect())

6. AI & Neural Networks
Custom-built feedforward neural network with adjustable weights and biases

   Input: Sensor distances; Output: Steering decisions

   Simple activation threshold: output = sum > bias ? 1 : 0

   Mutation for learning (NeuralNetwork.mutate())

7. Sensor Simulation (Ray Casting)
Car sensors implemented via ray casting

   Each ray is checked for intersection with road borders and traffic cars

8. User Interaction
Buttons to save/discard best-performing neural networks using localStorage

9. Functional Programming Elements
Use of array methods like .map(), .forEach(), .find(), Math.min(...) with spread operator
</br>

<h3>🧮 Neural Network Details</h3>
Structure: inputs -> hidden layer -> outputs

Example: [5 sensor inputs] → [6 hidden] → [4 outputs] (forward, left, right, reverse)

Outputs direct control & movement

Uses hard threshold activation 

Mutated over generations to improve performance

