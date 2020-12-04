# FaceworxTool

Project forked from the original.

## What is Faceworx?
https://www.looxis.de/en/looxis-faceworx-tool
It used to be a somewhat popular tool for making 3D models of faces from front and profile pictures. 

## How to build Faceworx ?

I used Visual Studio C++ 2017, Windows 10, 64-bit.

1. Install the repository
2. Open the project
3. You will be prompted to install some libraries for MFC, install them
4. Install DirectX 10, add the library reference or add the files to the directory (Note: Even if the installation fails on Windows 10, you still get the .h and .lib files)
5. Update the include path and library paths
6. Change the name of/reference to the Directx9 specific files (eg: dxerr.lib to dxerr9.lib)
7. Add #include <memory> to use unique_ptr instead of auto_ptr
8. Add legacy_stdio_definitions.lib to the linker, or use #pragma comment(lib, "legacy_stdio_definitions.lib")
9. If everything went well, the file should compile
10. ???
11. Profit (?) Maybe not. The program is very buggy. 

## Improvements/Addons/To-do

I would rather prefer to learn from it to rewrite it in something else, but please consider the following if you wish to update it. (There seems to be no discussion regarding this source code anywhere. Kind of sad.)

### Bugs
- [ ] Document the bugs/issues somewhere.
- [ ] The program can literally not load its own file, possibly an issue with saving too?
- [ ] Obj export doesn't work.

### Bugs mentioned on the official site (Possibly related to the above bugs)
- [ ] Obj export makes the texture black. (Mentioned on the site, but I cannot replicate it)
- [ ] The tool does not seem to work under Windows 64bits. (Mentioned on the site, but if you follow the instructions above, it works fine)

### Codebase/General
- [ ] Update the references to libraries etc. (Original had no comments about this)
- [ ] Detailed documentation for the code. (Original seems to be auto generated)
- [ ] Comments to explain what is going on. (Most documentation and stackoverflow discussion about the directx functions is from the mid 2000s)

### Cross platfrom
- [ ] Switch from DirectX to OpenGL, reimplementing all DirectX functions to OpenGL (Yikes, a big task)
- [ ] Switch from MFC to a crossplatform library for GUI
- [ ] Decoupling of the GUI from core logics? Emscripten support?
