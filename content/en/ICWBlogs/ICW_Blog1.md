---
author: "Vedant Shahare"
title: "In a Corner of the World Blog1"
date: 2024-08-07
projectType: "Ongoing"
description: "Added dialog system and inventory system"
tags: ["Game Development", "Unreal Engine", "Blueprint", "Horror", "Puzzle", "Story", "RPG", "Game", "Pixel Art", "3D", "Blog"]
thumbnail: "/CStellDevlog/InACornerOfTheWorld/ICW_tbn2.png"
---

### Maintaining same pixel size across all materials
Shader parameter collection and world aligned texture has helped alot with majority of materials.

{{<embedVideo "ShaderParameter" "/CStellDevlog/InACornerOfTheWorld/Blog1/ICW_ShaderParameter.mp4">}}

### Dialog system
Inkpot plugin is used to integrate Ink narrative scripting language into our game. With Ink it is incredible that how easily we separated programming part with design part.
Inkpot is added as git submodule to our development repositary.
{{<embedVideo "DialogSystem" "/CStellDevlog/InACornerOfTheWorld/Blog1/ICW_DialogSystem.mp4">}}
Dialog system is designed as blueprint component, also designer doesn't need to tinker with blueprints, he just need to change Ink script asset and give what items npc holds.
{{<embedVideo "ChangingInkScript" "/CStellDevlog/InACornerOfTheWorld/Blog1/ICW_ChangingInkScript.mp4">}}

### Narrative driven inventory system
All the transactions to inventory is triggered by Ink scripts. When designer wants to check or request for items from inventory or give an item to player, he just need to mention it in the Ink script.
{{<embedVideo "InventoryTransaction" "/CStellDevlog/InACornerOfTheWorld/Blog1/ICW_InventoryTransaction.mp4">}}