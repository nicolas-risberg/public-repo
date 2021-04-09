---
layout: post
categories: highlights
title: Deferred Decals
tags: [deferred rendering, decals, rendering]
date-string: MARCH 01, 2021
---

<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

## Introduction

I implemented deferred decals for our seventh game project at The Game Assembly.
The decals were exported from Unity and rendered to the GBuffer in three separate passes depending on which textures to use; albedo, normal or "material".

Using three separate passes, there is no need to copy the GBuffer and you have higher flexibility regarding which textures to use and how to alpha blend the results.

## Implementation

I chose to use a cube volume for projection due to its simplicity, held by the renderer and scaled by the game object transform component.

<center>
    <div class="photoset-grid-custom" data-layout="3">
        <img src="/images/decal_albedo.jpg">
        <img src="/images/decal_normal.jpg">
        <img src="/images/decal_material.jpg">
    </div>
</center>

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