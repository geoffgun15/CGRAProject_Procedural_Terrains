# CGRA OpenGL Base Project

## Overview

A C++ graphics programming framework built on OpenGL v3.3 for real-time 3D graphics applications. This project includes a terrain rendering system with mesh generation and custom shader support, designed for the CGRA 350 course.

## Project Structure

### `/work` Directory - Main Application

The core application resides in the `work` folder and contains:

#### Source Code (`src/`)
- **main.cpp** - Application entry point and main render loop setup
- **application.hpp/cpp** - Application class for managing the graphics window and lifecycle
- **terrainRenderer.hpp/cpp** - Main terrain rendering engine (14KB)
- **terrain_mesh.hpp/cpp** - Terrain mesh generation and management
- **opengl.hpp** - OpenGL utility functions and wrapper classes
- **cgra/** - CGRA library namespace with helper utilities

#### Resources (`res/`)
- **shaders/** - GLSL vertex/fragment shader files for rendering
- **textures/** - Texture assets used in the application

#### Build Configuration
- **CMakeLists.txt** - Main CMake build configuration for the project
- **cmake/CGRAFunctions.cmake** - Helper CMake functions for CGRA projects

## Key Features

- **Terrain Rendering System** - Efficient mesh-based terrain visualization
- **Custom Shaders** - Modular shader system for flexible rendering
- **Cross-Platform** - Supports Linux, Windows, and macOS development
- **OpenGL Integration** - Direct OpenGL v3.3 API access
- **CGRA Library** - Utility classes for:
  - Shader compilation and management
  - Mesh building and manipulation
  - Image loading/saving
  - Geometry utilities (primitives, spheres, etc.)
  - ImGui UI integration
  - Wavefront OBJ file loading

## Requirements

- CMake 3.10+
- OpenGL v3.3+
- C++11 compliant compiler
- Platform-specific IDE (Visual Studio, Eclipse, Xcode, or command line)

## Building

### Quick Start (Linux/macOS)
```sh
$ ./runcmake.sh
```

### Manual Build
```sh
$ mkdir build
$ cd build
$ cmake ../work
$ make
$ cd ..
$ ./build/bin/base [args...]
```

### Windows (Visual Studio)
```cmd
> cmake -G "Visual Studio XX Win64" ..\work
```

## IDE Setup

- **Linux/macOS**: Eclipse or command line
- **Windows**: Visual Studio 2017 or later
- **macOS**: Xcode

See the full README for detailed IDE configuration instructions.

## Notes

- Add new source files to `/work/src` - they are automatically compiled based on file extension
- Place shader files in `/work/res/shaders`
- Place textures in `/work/res/textures`
- Only submit the `work` directory when completing assignments - do not include the `build` directory
- Camera controls follow Maya-style navigation
