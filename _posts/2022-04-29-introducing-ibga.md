---
layout: post
title: Introducing IBGA
description: IBGA is IB Gateway in headless mode. It is a container image preloaded with scripts for automating user interactions with IBG.
---

<a href="https://heshiming.github.io/ibga/" target="_blank">IBGA</a> is <a href="https://www.interactivebrokers.com/en/trading/ibgateway-latest.php" target="_blank">IB Gateway</a> in headless mode. It is a container image preloaded with scripts for automating user interactions with IBG.

<img src="https://heshiming.github.io/ibga/images/ibga-video.gif">

## Benefits:

* A "docker compose" flavored configuration
* Store username, password, time zone and other options in one place
* Automatic installation and easy upgrade of IBG
* Automatic handling of daily restarts beyond the one week limit, upon exit or crash
* Automatic handling of paper trading confirmation and options dialog
* Automatic daily export of logs
* Retaining of settings after an upgrade
* A disposable container design

## Under the hood:
* IBGA runs in a set of bash scripts.
* IBGA relies on <a href="https://heshiming.github.io/jauto/" target="_blank">JAuto, a JVMTI agent</a> to determine screen locations of windows, text boxes, and buttons.
* IBGA relies on <a href="https://github.com/jordansissel/xdotool" target="_blank">xdotool</a> to simulate keyboard and mouse input.
* IBGA relies on <a href="https://en.wikipedia.org/wiki/Xvfb" target="_blank">Xvfb</a>, <a href="https://github.com/LibVNC/x11vnc" target="_blank">x11vnc</a>, <a href="https://novnc.com/" target="_blank">novnc</a> to provide a VNC-capable <a href="https://en.wikipedia.org/wiki/X_Window_System" target="_blank">X11</a> environment for IBG.
