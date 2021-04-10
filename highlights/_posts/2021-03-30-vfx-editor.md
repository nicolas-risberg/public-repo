---
layout: post
categories: highlights
title: "VFX Editor using ImGui"
featured-image: /images/vfx_editor_gif.gif
tags: [vfx, imgui, tools]
date-string: MARCH 30, 2021
---

<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

## Introduction

For our seventh game project at The Game Assembly, I made a VFX Editor using **<a href="https://github.com/ocornut/imgui">ImGui</a>** based on the VFX and Particle Systems I designed for the project prior.
With ImGui it was easy and fast to get a graphical user interface running and rendering in our custom engine, and features like the color picker and curve editing were essential in the workflow designed in concert with the graphical artists.

## Implementation

The VFX Editor works on a component called `VFXSystemComponent`. This component holds a list of data structures called `VFXEffect`s. 
Each effect holds data associated with any number of what we call VFX meshes and particle emitters, where a VFX mesh is simply some geometry using shaders to scroll textures across it. These meshes and particle emitters are rendered using alpha blending and with depth writing turned off in a late render pass.
The system is defined this way to allow a single game object with this component to store several collections of meshes and particle emitters in different configurations, and to activate any one of these collections as an "effect" at any time.



{::options parse_block_html="true" /}
<details><summary markdown="span">**View Code**</summary>

```hlsl
```

</details>
{::options parse_block_html="false" /}



<script src="/assets/js/jquery.photoset-grid.js"></script>
<script type="text/javascript">
    $('.photoset-grid-custom').photosetGrid({
    // Set the gutter between columns and rows
    gutter: '5px',
  
    // Wrap the images in links
    highresLinks: true,
  
    // Asign a common rel attribute
    rel: 'print-gallery',

    onInit: function(){},
    
    onComplete: function(){
        // Show the grid after it renders
        $('.photoset-grid-custom').attr('style', '');
    }
});
</script>