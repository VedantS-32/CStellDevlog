---
author: "Vedant Shahare"
title: "Constellation Engine Blog0"
date: 2024-08-07
projectType: "Ongoing"
description: "Added model and material system"
tags: ["Game Development", "Game Engine", "C++", "OpenGL", "Vulkan", "3D", "Premake"]
thumbnail: "/CStellDevlog/ConstellationEngine/CStell_tbn1.png"
---

### Loading models in CStell!
CStell uses .csmesh file to hold metadata to 3D intermediate format. Model class is container for these imported meshes and hold information about material associated with it.
{{<embedVideo "LoadingModels" "/CStellDevlog/ConstellationEngine/Blog0/CStell_LoadingModel.mp4">}}

### Drag N' Drop model and material system
You can drag n' drop meshes(.csmesh) and materials(.csmat) to change them.
{{<embedVideo "DragNDrop" "/CStellDevlog/ConstellationEngine/Blog0/CStell_DragNDrop.mp4">}}

### Shader uniform reflection
Shader uniforms are automatically reflected to editor
{{<embedVideo "ShaderReflection" "/CStellDevlog/ConstellationEngine/Blog0/CStell_ShaderReflection.mp4">}}

### Instantaneous material reload
Shaders can be recompiled without restarting the whole engine.
{{<embedVideo "MaterialReload" "/CStellDevlog/ConstellationEngine/Blog0/CStell_MaterialReload.mp4">}}

### External
[GitHub Repository](https://github.com/VedantS-32/ConstellationEngine.git)