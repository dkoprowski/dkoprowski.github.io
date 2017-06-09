---
excerpt: ""
header:
  overlay_color: "#333"
  overlay_filter: 0.5

title: Organize your Unity project directories!
date:   2016-03-24 23:00:00 -0600
categories: unity
---

Organize your workplace! Unity devs do not dispose of any common solution for this issue. It's time to change it.

Work on multiple projects, together with many developers taught me that some general solutions have to be developed due to the fact that now most frequent pattern is a *mess*. I have lost few hours of my life just because files were in the wrong place. One can think this is only cosmetic improvement or it can be done later.  But this minor detail can improve your team work and save unnecessary confusion.
![Mess image](https://upload.wikimedia.org/wikipedia/commons/3/39/Messy_storage_room_with_boxes.jpg)

## Keep your files in proper directories
This is where I could finish but... In Unity we get an empty `Assets` folder so we can do and use it to whatever we want. That's what I call freedom :) But be responsible! 

* Bad idea: Put everything into this folder without any order.
* Good idea: Create some directory structure
* The best idea: Create universal structure where everything has its place

### But how should I prepare such structure?
Look at your last projects. Which files could be packed together? Which of them you had used most frequent?   
Also think about your team. Solution should be intuitive for everyone.

I mostly work on small projects - few scenes, few team members. For bigger games I would rather adjust files per scene/level or functionality. Despite this in my case the best directory structure is as below:
```
|- Assets
    |- Editor       //special folder
    |- Resources    //special folder
    |- Plugins      //special folder
    |- Extensions
    |- Scenes
    |- Scripts
    |- StaticAssets
        |- Animations
        |- Animators
        |- Effects 
        |- Fonts
        |- Materials
        |- Models
        |- Prefabs
        |- Shaders
        |- Sounds
        |- Sprites
        |- Textures
        |- Videos
```

Here you have full list of so-called [Special Folders](http://docs.unity3d.com/Manual/SpecialFolders.html).
We are using such order with my team from about year now and it works well. I don't remember any situation that we needed to add some new folder *(of course we use some subfolders with this)*

### Automatic solution
Don't worry. You don't have to create all these folders manually. I'm creating few tools facilitating starting up with new project. One of them is [UnityProjectTreeGenerator](https://github.com/dkoprowski/UnityProjectTreeGenerator).

This little plugin will generate mentioned directory structure in few moments. It will also add `.keep` file to each folder just because `git` ignores empty directories. If you have existing project with some structure created - it's OK - it will only create new folders if you don't have them. It will not edit or remove anything.

Of course it is your project so you can change your directory tree as you want. 
To do this just look at `GenerateDirectory` method in `CreateProjectTree` class.