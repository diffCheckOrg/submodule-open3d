# submodule-open3d
The repository contains the binaries for Windows/MacOs for the library open3d

## Modifications to the original repository
These binaries have the main interface header of `Open3D` (`open3d/Open3d.h`) modified to not include the `visualization` source code. This is because in `diffCheck` we use another visualization and opengl visualizer, having those from `Open3D` would cause conflicts with the `OpenGL` context (glfw, glad etc). Hence all the functions are accessible except the visualization ones.