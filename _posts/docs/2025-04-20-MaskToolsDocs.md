---
layout: post
title: "Mask tools"
subtitle: "Common tools for working with mask textures"
date: 2025-04-20
author: "Sora Mas"
post_type: "documentation"
thumb-img: "/img/MaskTools.png"
header-img: "img/MaskTools/MaskToolsHeader.png"
hidden: true
tags:
  - UE5
  - Editor
  - Mask
  - Optimization
  - Code Plugin

---


# Introduction

Mask textures are usually used in game development and 3D art to compress up to 4 grayscale textures into a single RGBA texture. Using this industry standard method you can reduce drawcalls and improve your game performance. 

For more information refer to these documentation pages:
[Using texture masks](https://dev.epicgames.com/documentation/en-us/unreal-engine/using-texture-masks-in-unreal-engine)


# Motivations

Texture masks are pretty usefull for 3D artists, VFX artists, Technical artists and kinda anyone working in a 3D environment. I've always been confused about why the creation method for this widespread workflow was so ofuscated, usually relying on paid 3rd party software (I'm looking at you, Adobe) or very niche open source software that, even solving the budget problem, still needs to be downloaded, installed and set up for not even offering your texture ready in engine.

I was missing the ability for the game engine to handle this mask texture creation process, so I implemented it and released for all of you to enjoy in-engine mask texture manipulation tools :D

# Features

- Texture Mixer - Merge up to 4 grayscale textures into one single RGBA texture using an editor built-in interface.
![image](/img/MaskToolsDocs/ChannelMixerScreen.png)

- Texture Splitter - Split any texture into it's RGBA channels, creating one single grayscale texture for each one of them. 

# Prerequisites

## Installation

The plugin can be adquired in [Fab](https://www.fab.com/listings/0d7fb6db-b5ad-4375-9330-f659a633ffd1) or cloned or downloaded for free from [GitHub](https://github.com/Bumvolla/MaskTools).

If you got Git installed on your computer you can clone the repository by typing this command in a terminal in your project "Plugins" folder:


~~~
git clone https://github.com/Bumvolla/MaskTools.git
~~~

or, if you already got your unreal project in a git repository:


~~~
git submodule add https://github.com/Bumvolla/MaskTools.git
~~~

If not, you can download the .zip file in the [latest release](https://github.com/Bumvolla/MaskTools/releases/latest) and extract it in your project "Plugins" folder

# Plugin usage

## Texture Mixer

You can find the texture mixer navigating to the "Tools" dropdown on the upper, and clicking on the "**Texture Mixer**" button.

![image](/img/MaskToolsDocs/MaskToolsScheme.png)