---
layout: post
title: "Easy power lines"
subtitle: "Procedural power lines generation for UE5"
date: 2025-02-20
author: "Sora Mas"
post_type: "documentation"
thumb-img: "/img/EasyPowerLines.png"
header-img: "img/EasyPowerLinesDocs/powerlinesbg.png"
hidden: true
tags:
  - UE5
  - Procedural
  - Power Lines
  - Code Plugin

---

<p align="center">
  <a href="https://github.com/Bumvolla/UE_EasyPowerLines">
    <img src="/img/EasyPowerLines.png" alt="Logo" width="80" height="80">
  </a>
<h3 align="center">Easy power lines</h3>

# Features

- Performant power lines procedural generation
- Acurate paralel catenary calculation
- Class preset based construction
- Randomization
- Terrain snaping

# Prerequisites

## Installation

The plugin can be adquired in [Fab](https://www.fab.com/listings/df95fe55-b016-46e1-9ffa-fd6e26241a61) or cloned or downloaded for free from [GitHub](https://github.com/Bumvolla/UE_EasyPowerLines).

If you got Git installed on your computer you can clone the repository by typing this command in a terminal in your project "Plugins" folder:


~~~
git clone https://github.com/Bumvolla/UE_EasyPowerLines.git
~~~

or, if you already got your unreal project in a git repository:


~~~
git submodule add https://github.com/Bumvolla/UE_EasyPowerLines.git
~~~

If not, you can download the .zip file in the [latest release](https://github.com/Bumvolla/UE_EasyPowerLines/releases/latest) and extract it in your project "Plugins" folder

## In engine

For this pluign to work you'll need:
 - An static mesh for the pole
 - An static mesh for the wire
 - Setup a blueprint that inherits from *Catenary pole preset*

 You have examples for all of them in the Plugin content folder.

 ## Catenary pole preset

 #### Blueprint creation

  1. Right click in the content browser.
  2. Select create basic asset -> Blueprint class
  3. Open the *All classes* dropdown and search for *UtilityPolePreset*
  4. Press the select button.

  ![image](img/EasyPowerLinesDocs/UtilityPolePresetCreation.png)

 #### Blueprint setup

  1. Drag and drop the blueprint in the scene.
  2. In the details panel, fill the values:
    - Pole mesh : The static mesh that the pole will have.
    - Wire targets : Add as many items to the array as connections the pole will have, then move each one of the widgets to the positions where the connections will be.
  3. Press the *Copy to class defaults* button in the details pannel.
  4. Make sure the values have refreshed inside the blueprint, if not, they will once the editor is restarted.

  ![image](img/EasyPowerLinesDocs/UtilityPolePresetWithTargets.png)


 # Plugin usage

 ## Spline utility pole
 
 Open the add actors to scene tab and drag and drop a *Spline utility pole* actor.
 Fill out the exposed values:

 ### Generation
 |*Parameter*|*Description*|
 |Actor distance|Distance between each pole that will be created|
 |Pole preset|Any class that inherits from UtilityPolePreset, determines the pole mesh and conection points|
 |Slack|The min ammount of slack the wires will have|
 |Slack variation|The max ammount of random slack that will be added to the slack value (Higher values will take longer to calculate)|
 |Spline resolution|Precision of the catenary curve that will be created|
 |WireMesh|Static mesh that will be used for the spline mesh construction|
 |Wire mesh axis|Which is the long axis of the static mesh|
 |RandomTilt|Max random rotation that will be applied in the X axis of the pole|
 |bAutoGenerate|Run or not logic in construction script(beta)|
 |||
  ### Snaping
 |*Parameter*|*Description*|
 |bSnapToTerrain|Determines if the pole will try to snap to the terrain or not|
 |RayLength|Ray of the ray that will search for collision to snap the pole to it|
 |CollisionChannel|The collision channel the ray will test for|
 |bDrawDebugLines|Wether or not debug lines will be drawn for the raycast|

