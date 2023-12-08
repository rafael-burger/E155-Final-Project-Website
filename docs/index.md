---
layout: page
title: Project Overview
permalink: /
exclude: true
---

# Project Abstract
<p align = "center">
<img src="./assets/img/IMG_1737.jpg" alt="cube_im" width="300"/>
</p>

This website presents the ENGR-155 final project completed by Rafael Burger and Tjaard Van Löben Sels. The project aimed to provide a platform for displaying images in 3 dimensions. To achieve this effect, a two-dimensional array of LEDs was spun quickly about its long axis such that the plane of LEDs traced out a cylindrical volume. This LED array was updated at 64 steps within each rotation to generate "pixels" for the desired image. An Ice40 FPGA was used to drive LED array updates and a STM32 microcontroller was used to control the spin rate and monitor user input. Two ESP32 WiFi modules were used to facilitate wireless communication between the stationary components (microcontroller, user input circuit) and the spinning ones (FPGA, LED array).

# Project Motivation

From Star Wars to Blade Runner 2049, holograms have been a staple within pop-culture's imagined futuristic realities. There seems to be some expectation, given the recurrence of the hologram, that an image should not be constrained to two dimensions, but rather should be interacted with in the same manner as physical objects. Whether or not you buy that take, you've got to admit that they look pretty cool. So why do we see them so seldom? It was with a goal of bringing this classic futuristic aesthetic into existence within our every-day lives that we began the project. 

# System Block Diagram

<p align = "center">
<img src = "assets/img/VolDispSystemBD.png" alt = "block_diagram" width = "600"/>
</p>

The design is composed of two sub-systems, a spinning assembly and a static assembly. The spinning assembly comprises the LED array (which must spin) and all other hardware required to drive the LED array (FPGA). The static assembly consists of components to physically support the spinning assembly (mounting supports, motor), as well as hardware to handle user input and drive the spinning assembly (interactive circuit, microcontroller, motor encoder). Both sub-systems include an ESP32 WiFi module which wirelessly transfer information between the static and spinning assemblies. Due to complications involving coupling between rotating and stationary systems, no physical electrical connection exists between the two sub-assemblies. 
