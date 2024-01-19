---
author: "Vedant Shahare"
title: "CStellSFML 2D Game Engine"
date: 2024-01-07
description: "2D Game Engine written in C++ and SFML, Implementing ECS Architecture"
tags: ["Game Development", "Game Engine", "C++", "SFML", "ECS"]
thumbnail: "/CStellDevlog/CStellEngineSFML/CStellSFML_Thumbnail.png"
---

### CStell Engine SFML

2D game engine written in C++ and SFML.
This is just small project to learn more about Game Development, how Game Engine work under the hood and C++

WARNING: this project wasn't made with the focus of compatibity and protability, this is more like exploration and experiment. Just cloning the repository will not make it work out of box, you will need to manually link all libraries.

[GitHub Repository](https://github.com/VedantS-32/ConstellationEngineSFML)

### Features

- Written in C++ and SFML
- ECS Architecture
- Own Physics Engine
- Save/Load Support using YAML
- Editor Interface using ImGui
- Content Browser using ImGui FileDialog
- Simple Sprite Sheet Animation Support

### CStell Editor

Dockable menu UI is made with the help of ImGui

{{< embedVideo "CStellEditor" "/CStellDevlog/CStellEngineSFML/CStell_DockableEditor.mp4">}}

### Drag and Drop Editor

Tracking and Truncating mouse position while entity is selected

{{< embedVideo "CStellDragnDrop" "/CStellDevlog/CStellEngineSFML/CStell_DragnDrop.mp4">}}

### Operations at Runtime

{{< embedVideo "CStellRuntimeOps" "/CStellDevlog/CStellEngineSFML/CStell_RuntimeOps.mp4">}}

Pretty cool right?

- Adding Entity

- Adding Component

- Changing Sprite

### Axis Aligned Bounding Box (AABB) Collision

A simple AABB detection and resolution

{{< embedVideo "CStellAABB" "/CStellDevlog/CStellEngineSFML/CStell_AABB.mp4">}}

### Saving the Scene

Serializer/Deserializer using YAML file

{{< embedVideo "CStellSaveLoad" "/CStellDevlog/CStellEngineSFML/CStell_SaveLoad.mp4">}}

### External

- An excellent resource for learning C++ and introduction to game programming [LinkToPlaylist](https://youtube.com/playlist?list=PL_xRyXins848nDj2v-TJYahzvs-XW9sVV&si=Ob8yquaC4f9_B_Q6)

- Sprite Asset used [SunnyLand](https://ansimuz.itch.io/sunny-land-pixel-game-art) by [Ansimuz](https://itch.io/profile/ansimuz)

- [GitHub Repository](https://github.com/VedantS-32/ConstellationEngineSFML)

Thank You for Reading!
