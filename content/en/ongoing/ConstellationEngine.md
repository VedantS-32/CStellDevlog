---
author: "Vedant Shahare"
title: "Constellation Engine"
date: 2024-01-14
uniqueID: 1
projectType: "Ongoing"
description: "3D game engine written in C++"
tags: ["Game Development", "Game Engine", "C++", "OpenGL", "Vulkan", "3D", "Premake"]
thumbnail: "/CStellDevlog/ConstellationEngine/CStell_tbn1.png"
CStellBlog: true
thumbnailArray:
 - "/CStellDevlog/ConstellationEngine/CStell_Pic0.png"
 - "/CStellDevlog/ConstellationEngine/CStell_Pic1.png"
 - "/CStellDevlog/ConstellationEngine/CStell_Pic2.png"

---


### Constellation Engine
Rendering Constellations!

3D Game Engine written in C++

### CGraphicsCore
Please visit CGraphicsCore repository for latest version Constellation Engine codebase
[CGraphicsCore](https://github.com/VedantS-32/CGraphicsCore)

3D renderer and framework for learning OpenGL. It is rewrite of Constellation Engine(CStell) for educational purpose and betterment of CStell.

~~[Old Version](https://github.com/VedantS-32/ConstellationEngine)~~


### Prerequisites
- C++ compiler(tested with gcc, clang and msvc)
- Make
- Python
- Git

### Clone repository
```shell
git clone --recursive https://github.com/VedantS-32/CGraphicsCore.git
```

### Build Instructions
- Go to "script" folder
- Note: Currently due to some platform specifics, CGraphicsCore doesn't compile on Unix platforms, it will be supported in future
- Run CGraphicsSetup script for your platform
- Then run GenerateProject for your platform
- By default it will generate Makefile, please change Script/GenerateProject to generate project files for your IDE
``` shell
vendor/premake/bin/premake5.exe gmake2 #<-- Replace gmake2 with vs2022 for Visual Studio Solution
```
- If you have generated Visual Studio Solution, .sln file will be in root directory
- if you have generated Makefile, open terminal in root directory and enter following command to build CGraphicsCore. After building go to CGraphicsSandbox and launch the binary (CGrpahicsSandbox.exe for Windows)
``` shell
make -j #Number of core you want to allocate for compilation
```
- Additionally you can specify build configuration and compiler
``` shell
make CC= C_Compiler CXX= C++_Compiler config=BuildConfig -j Cores
```
- Example
``` shell
    make CC=gcc CXX=g++ config=release -j 4
```

### Aims

- To learn how game engines work under the hood
- Creating massive open worlds
- To be able to handle the scale of universe
- Accurate rendering and simulation of galactic bodies like galaxies, constellation etc
- To render unique semi-realistic artstyle