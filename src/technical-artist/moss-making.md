# Moss Making

## Material Maps
### Albedo Texture
Base color of a surface, without any highlights or shadows. It represents the pure reflection of a material

## Masks & Maps
* 

## Texture Baking
Two basic approaches to Texture Baking in that maps are rendered relative to 
* Objects
* Scenes

To bake standard textures, that is render objects relative to themselves, first we have to make sure the meshes are shaped as they need to be, and are fully UV Unwrapped and UV mapped, and have materials appropriately setup and assigned for the desired effect.

---

I made the initial model in blender. The stickers in real life have a very tiny bump, so moisture gets trapped in it. And this causes moss/rust to build up. 
In actual 3d rendering, the very minute details, such as a bump caused by a sticker. Is actually very CPU/GPU intensive task. So automating this, is not usually what the industry does. But if it did, it would have created a more realistic models.

## Issue: Make a procedural system that can generate rust/moss growth
I made the initial model - the walking sign. This model is created referencing an actual image. The moss growth was identified to be because of the small embossed edges of the stickers. The water/moisture that was trapped in these edges were the cause of the moss growth being higher in certain zones. 
Our task is to create the model, and be able to identify the zones in the UV where there are more embossed surfaces. 

Most of the aesthetics of Kerala are shown to be more worn out, abandoned and aged. By accurately representing this aging we would be able to create more realistic aged assets.

* Tried creating different PBR Texture maps, but none of them were able to detect the small embossed surfaces. 
[ ] -  gonna try to change baking setting for each maps, starting with the normal map 

But due to the asset not being the hero asset and is mostly not given enough screen time or real estate, makes the requirement for having these embossed surfaces to be non-existent. 
> What about if the case of the asset being like a semi-hero asset. In the game, the asset is equiped with the ability to have a screentime or closeup, if the player chooses.


---

# Unity

Shaders are specific to different render pipelines in Unity
## Render Pipelines
### Built In Render Pipeline
### Universal Render Pipeline
### High Definition Render Pipeline



---
## Meh Tags
* ShaderGraph
* Built in Render Pipeline
* GLSL
* 

## Tags
* HLSL
* ShaderLab
* DirectX 12
* URP
* ShaderGraph
* 

## ohyea Tags
* OpenGL
* Vulkan
* WebGPU
* Metal

## Resources
* https://www.katsbits.com/codex/texture-bake/
* https://docs.unity3d.com/6000.3/Documentation/Manual/render-pipelines.html
* https://danielilett.com/2025-10-15-tut10-01-your-first-shader/
* https://docs.unity3d.com/6000.0/Documentation/Manual/SL-Properties.html
* https://learn.unity.com/tutorial/shaderlab-anatomy-of-a-shader
* https://superuser.com/questions/519969/why-do-lots-of-games-have-direct-x-9-and-11-options-but-not-dx10
* https://learn.microsoft.com/en-us/windows/win32/direct3dhlsl/dx-graphics-hlsl-semantics
* https://docs.unity3d.com/6000.0/Documentation/Manual/shaders-reference.html
* https://learn.microsoft.com/en-us/windows/win32/direct3dhlsl/dx-graphics-hlsl
* https://learnopengl.com/Getting-Started/Coordinate-Systems

## Resources SideQuest
* https://www.tutorialspoint.com/directx/index.htm
* https://www.reddit.com/r/Unity3D/comments/1bze6xc/do_jobs_exist_for_shader_programmers/
* https://www.reddit.com/r/TechnicalArtist/comments/1qdslg6/jobs_for_high_level_shaders_outside_of_gamedev/

