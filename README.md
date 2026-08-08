# 🪐 3D WebVR Solar System

A fully functional, 3D animated model of the Solar System built with **A-Frame (WebVR)**. 

This project simulates the orbits and relative scales of the Sun and all eight primary planets (Mercury through Neptune), demonstrating advanced use of the A-Frame scene graph, asset management, and 3D animations directly in the browser.

## ✨ Features
- **Complete Planetary System:** Includes the Sun, all eight primary planets, and the Earth's Moon orbiting correctly.
- **High-Resolution Textures:** Utilizes 2K texture maps for all planetary bodies and a seamless Milky Way skybox for the background environment.
- **Proportional Orbit Speeds:** Planets revolve around the Sun at relative, proportional speeds.
- **Dynamic Lighting:** A central Point Light at the Sun's coordinates provides realistic shading on the "day" side of the planets, while a dim Ambient light ensures the "night" sides remain visible.

## 🛠️ Technical Implementation

- **Orbit Mechanics:** Implemented nested parent `<a-entity>` wrappers to create rotation pivots at the center of the Sun. This allows each planet to revolve independently at varying speeds while maintaining its own local rotation.
- **Realistic Scaling:** Planetary bodies are scaled relative to one another to emphasize the massive size differences between gas giants (Jupiter, Saturn) and terrestrial planets.
- **Asset Management:** Utilized A-Frame's `<a-assets>` management system to pre-buffer the large 2K image textures, ensuring the scene only renders once all heavy assets are fully loaded.

## 🧠 Challenges & Solutions

During development, I encountered and resolved several 3D rendering challenges:

* **Double-Sided Rendering (Saturn's Rings):** Initially, Saturn's rings were only rendering from the top down due to default face-culling. I resolved this by explicitly setting the material property to `side: double`.
* **Viewport & Scale Clipping:** Because realistic planetary distances made the scene exceptionally large, the camera was clipping through the environment upon load. I adjusted the camera's initial Z-position and modified the clipping plane parameters to ensure the entire system is visible on launch.

## 🚀 How to Run

**Step 1: Clone the repository**
```bash
git clone [https://github.com/yourusername/aframe-solar-system.git](https://github.com/yourusername/aframe-solar-system.git)
```

**Step 2: Navigate to the project directory**
```bash
cd aframe-solar-system
```

**Step 3: Open the project**
Open `index.html` in your browser. *(Note: Due to CORS policies with loading local textures, it is best to run this using a local server like VS Code's Live Server extension).*

---
*Note: This project was originally developed as a Computer Graphics application and has been adapted for my personal portfolio.*
