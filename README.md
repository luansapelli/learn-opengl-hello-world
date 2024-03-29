# Learn OpenGL - Hello World

## Introduction

This is a simple project to learn OpenGL. It is based on the [LearnOpenGL](https://learnopengl.com/) tutorial.
The project is written in C++ and uses the [GLFW](https://www.glfw.org/) library for window management and the [GLAD](https://glad.dav1d.de/) library to load OpenGL functions.

I used my own boilerplate code to setup the project. It is available [here](https://github.com/luansapelli/opengl-gfx-boilerplate).

This project is a simple triangle rendered on the screen. It is the "hello world" of OpenGL.

## What I learned

- How to setup a project using GLFW and GLAD
- How to create a window and a OpenGL context
- What VBO and VAO are and how to create them
- What is a shader and how to create and use them
- How to render a triangle on the screen

## Final result
![imgopengl.png](/screenshot/imgopengl.png)

## Exercises
- [x] Try to draw 2 triangles next to each other using glDrawArrays by adding more vertices to your data.
- [x] Now create the same 2 triangles using two different VAOs and VBOs for their data.
- [x] Create two shader programs where the second program uses a different fragment shader that outputs the color yellow; draw both triangles again where one outputs the color yellow.
