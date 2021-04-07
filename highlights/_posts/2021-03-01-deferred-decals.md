---
layout: post
categories: highlights
title: Deferred Decals
tags: [deferred rendering, decals, rendering]
date-string: MARCH 01, 2021
---

## Introduction

I implemented deferred decals for our seventh game project at The Game Assembly.
The decals were exported from Unity and rendered to the GBuffer in three separate passes depending on which textures to use; albedo, normal or "material".

Using three separate passes, there is no need to copy the GBuffer and you have higher flexibility regarding which textures to use and how to alpha blend the results.

## Implementation

I chose to use a cube volume for projection due to its simplicity, held by the renderer and scaled by the game object transform component.