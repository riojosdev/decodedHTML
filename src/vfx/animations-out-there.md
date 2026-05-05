# Animations/CREATIVE-EXPERIENCES - How is it done?

## 
* Making the frame-by-frame animation workflow done using HTML components, in the project I maintain - Jaggery UI library
* 

### Problem
* One frame has multiple image/object/hero that needs to be animated
* The next frame also has multiple, but not the same number of image/object/hero as in the previous frame

This is animation workflow that needs to be done using the component (wc-diffuse-down-sprite) in Jaggery UI library. The animation programs listed below are listed to improve the ability of the component to support industry standards. So the people working in the industry would be able to use the component as seamlessly as possible. 

## How 2D animations are done
### Frame By Frame Animation tools




### 2D Animation/Art tools [^animation-programs]
#### Free
* Krita (2d) 
* OpenToonz (2d) 
* Digicel Flipbook 
* MonkeyJam 
* Synfig 
* Animation Paper 

#### Paid / Industry Standards
* After Effects (Motion graphics) 
* TV Paint 
* ToonBoom Harmony 
* Clip Studio 
* FlipaClip 
* Adobe Animate 
* Spine 
* Moho Studio Pro 
* Toon Boom StoryBoard Pro 
* Adobe Photoshop 
* Procreate Dreams 
* RoughAnimator 
* Linearity Move 
* Odyssey 

#### Related
* Procreate
* Gimp
* Pixel Studio
* Blender

### 3D Animation / Art tools
#### Paid / Industry Standards
* Maya
* 3Ds Studios Max
* Nuke
* Zbrush
* Houdini
* Cinema4D

#### Free
* Blender

#### Related
* Substance Painter/Designer
* Marvellous Designer

### Misc 
#### Project Management / Production
* Shotgrid / Shotgun
* Ftrack
* Frame.io
* Airtable

#### Editing
* Davinci Resolve

#### Stop Motion
* Dragonframe
* Stop Motion Studio

#### Game Development
* Unity
* Unreal Engine

#### Audio
* Audacity
* Cakewalk



# The different careers in animation
The component `wc-diffuse-down` should be built in such a way that is easily understandable by the people who are closely working with animations programs listed above. The common careers in animations are the following taken from reddit.[^careers-in-animation]




### Types it is being Imported to a specific Animation program
* SpriteSheet
    - Spritesheet can be made using the tools such as [^spritesheet-tools]
        * Aesprite
        * Krita
        * Gimp
* Individual Image Sequences

### How is it in game engines (Godot, Unreal, Unity)
* In [Godot](https://godotengine.org/), you can use [AnimatedSprite2D](https://docs.godotengine.org/en/stable/classes/class_animatedsprite2d.html#class-animatedsprite2d) and the [Animation Player](https://docs.godotengine.org/en/stable/classes/class_animationplayer.html#class-animationplayer). You can [import the different frames as a spritesheet](https://docs.godotengine.org/en/stable/tutorials/2d/2d_sprite_animation.html#sprite-sheet-with-animatedsprite2d) or as [individual images](https://docs.godotengine.org/en/stable/tutorials/2d/2d_sprite_animation.html#individual-images-with-animatedsprite2d)

* In Unreal Engine, all images you import is a texture asset. Using the Paper2D plugin you can use them as a sprites, tiles, animate it using flipbook (spritesheet)

* In Unity, 














#### Image Sequence (currently supported in Jaggery)
* Godot can use 
* Unreal


### How is different DCC softwares export the animation/frame(s)
* USD - which could be used in game engines pipelines, widely supported
* 
### How different game engines import it, and how do they use it to make an animation


### Each animation workflow defined by different game engines
[In unreal](https://dev.epicgames.com/documentation/en-us/unreal-engine/animating-characters-and-objects-in-unreal-engine)
#### How does it compare to Jaggery UI Component we are building
#### How do they import and use the asset to make an animation
#### What DCC softwares are the artist using to make these creative assets
#### What are the jobs the artist who make these assets are able to work on

## References
* [^spritesheet-tools]: [Reddit - /r/godot - How to make a spritesheet for godot?](https://www.reddit.com/r/godot/comments/o1wn5h/how_to_make_a_spritesheet_for_godot/h251r39/)
* [^animation-programs]: [Reddit - /r/animationcareer - Animation Programs (wiki)](https://www.reddit.com/r/animationcareer/wiki/index/resources/programs/)
* [^careers-in-animation]: [Reddit - /r/animationcareer - Careers In Animation (wiki)](https://www.reddit.com/r/animationcareer/wiki/index/resources/whatisananimationcareer/)
