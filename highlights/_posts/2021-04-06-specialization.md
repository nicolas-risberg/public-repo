---
layout: post
categories: highlights
title: "Volumetric Lighting: Light shafts from a directional light source in DirectX11"
featured-image: /images/shafts_gif.gif
tags: [specialization, volumetric lighting, rendering]
date-string: APRIL 06, 2021
---

## Introduction

Concurrently with our seventh game project at The Game Assembly, we had the opportunity to specialize; to plan an independent foray into a subject which we wanted to explore further.

For my specialization I chose to try and implement volumetric lighting in our custom game engine. My main goal was to implement a volumetric directional light, and to optimize it best I could.
Would there be time left, my secondary goal was to extend this implementation to point lights, spot lights and what I called "box" lights.

We had five weeks half-time to do this, as well as setting up our personal portfolio. I planned for letting my secondary goal slide, and to focus on my main goal.

## Implementation

I based my implementation on a **<a href="https://www.slideshare.net/BenjaminGlatzel/volumetric-lighting-for-many-lights-in-lords-of-the-fallen">talk</a>** at Digital Dragons by Benjamin Glatzel for Deck 13's Lords of The Fallen.[^1]

[^1]: <https://www.slideshare.net/BenjaminGlatzel/volumetric-lighting-for-many-lights-in-lords-of-the-fallen>

After loading the CryTek Sponza scene using our model loading pipeline, I set out to create a first working version of a volumetric directional light.

## Optimization

### Honorable Mentions

<center>
    <img src="https://i.gyazo.com/50f60e42af467e14210511b1872b1dbe.gif">
</center>

{::options parse_block_html="true" /}
<details><summary markdown="span">View Code</summary>

```c++
class CBoxLight 
{
public:
    CBoxLight();
    ~CBoxLight();
}
```

</details>
{::options parse_block_html="false" /}