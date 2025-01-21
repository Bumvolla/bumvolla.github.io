---
layout: post
title: "I built a UE plugin updater"
subtitle: "UE_PluginBuilder uses Unreal Automation Tool to build a .uplugin to a greater engine version"
date: 2025-01-21
author: "Sora Mas"
post_type: "post"
header-img: "img/UE_PluginBuilder.png"
tags:
  - UE5
  - UAT
---


Lately, I’ve needed to upgrade different plugins to newer versions of Unreal: at work, where we had to rebuild a legacy plugin for a major engine version, and at home, where I was trying to publish a plugin I built for an older Unreal version on Fab.

I knew about UAT (Unreal Automation Tool) having a BuildPlugin command that allows you to do this, and I used that method the first few times. However, I eventually got tired of forgetting the required arguments and spent a few hours setting up a GUI for it.

I used QT Community to build the GUI, and in no time, I had it working as a standalone application on Windows.

I’ve published it as open source on my GitHub! Feel free to test it out!

[Latest release](https://github.com/Bumvolla/UE_PluginBuilder/releases/latest)

![image](/../img/UE_PluginBuilderWindow.png)