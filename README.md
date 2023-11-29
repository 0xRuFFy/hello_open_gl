# HelloOpenGL

This is a simple setup for an OpenGL project with glfw and glad as the OpenGL loader.
This project is setup for simple multi platform development. No localy installed dependencies are needed.
This is achived with CMake.

The dependencies are `GLFW` and `GLAD`.

- `GLFW` The OpenGL abstraction layer
    - included as a submodule and will be build with CMake alongside the project.
- `GLAD` The OpenGL loader 
    - included as a local library and gets linked to the project as a static library with CMake.

## Building

First you need to clone the repository and update its submodules:

```bash
git clone https://github.com/0xRuFFy/hello_open_gl.git
cd hello_open_gl
git submodule update --init --recursive
```

Then you can build the project with CMake:

```bash
cmake -S . -B build
cmake --build build
```

Or

```bash
mkdir build
cd build
cmake ..
make
```


