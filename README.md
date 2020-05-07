# FaceworxTool

Project forked from the original.

## What is Faceworx?
https://www.looxis.de/en/looxis-faceworx-tool
It used to be a somewhat popular tool for making 3D models of faces from front and profile pictures. 

## How to build Faceworx ?

I used Visual Studio C++ 2017

1. Install the repository
2. Open the project
3. You will be prompted to install some libraries for MFC, install them
4. Install DirectX 10, add the library reference or add the files to the directory (Note: Even if it fails on Windows 10, you still get the .h and .lib files)
5. Update the include path and library paths
6. Change the name of/reference to the Directx9 specific files (eg: dxerr.lib to dxerr9.lib)
7. Add #include <memory> to use unique_ptr instead of auto_ptr
8. Add legacy_stdio_definitions.lib to the linker, or use #pragma comment(lib, "legacy_stdio_definitions.lib")
9. If everything went well, the file should compile
10. ???
11. Profit (?) Maybe not. The program is very buggy. 

## Improvements/Addons

I would rather prefer to learn from it to rewrite it in something else, but please consider the following if you wish to update it. (There seems to be no discussion regarding this  source code anywhere, what the heck?)

### Bugs
- [ ] Document the bugs
- [ ] The program can literally not load its own file
- [ ] Obj export doesn't work?

### Codebase/General
- [ ] Update the references to libraries etc
- [ ] Detailed documentation for the code
- [ ] Comments to explain what is going on

### Cross platfrom
- [ ] Switch from DirectX to OpenGL, reimplementing all DirectX functionst to OpenGL (Yikes)
- [ ] Switch from MFC to a crossplatform library for GUI
- [ ] Decoupling of the GUI from core logics? Emscripten support?
