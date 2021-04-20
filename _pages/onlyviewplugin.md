---
title: OnlyView Plugin
permalink: /onlyviewplugin
---

{% include figure image_path="/assets/images/unreal/onlyviewplugins.png" alt=""%}

<h2>Project description</h2>

This is my other freelance project on Upwork. OnlyView Plugin receives real camera's data from networking via UDP socket. The plugin will parse received data (contains real camera's position, rotation, FOV, lens shift) and apply the data to list of tracking cameras. This project requires modifying Unreal camera's projection matrix for lens shifting feature. The plugin also streams RenderTarget from SceneCapture2D in Unreal Engine to any [Spout](https://spout.zeal.co/) receiver devices
