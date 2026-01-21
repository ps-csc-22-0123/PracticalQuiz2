# Project: A-Frame Solar System Assessment
**Course:** Computer Graphics - CSC 413

**Framework:** A-Frame (WebVR)  

## Project Description
This project is a 3D animated model of the Solar System. It features the Sun and the eight primary planets (Mercury through Neptune), each textured with high-resolution 2K maps. The project demonstrates the use of the A-Frame scene graph, asset management, and complex animations to simulate the solar system.

## Technical Implementation
- **Orbit Mechanics:** Used parent `<a-entity>` wrappers to create rotation pivots at the center of the Sun, allowing planets to revolve at different speeds.
- **Realistic Scaling:** Planets are scaled relative to each other (e.g., Jupiter and Saturn are significantly larger than the terrestrial planets).
- **Textures:** Applied 2K textures for all planetary bodies, including a specific added texture for Saturn's rings and a Milky Way skybox for the background.
- **Lighting:** Implemented a central Point Light at the Sun's position to create realistic shading on the "day" side of the planets, supplemented by a dim Ambient light to ensure the "night" sides remain visible.

## Problems Encountered & Solutions
1. **Saturn's Rings:** Initially, the rings were only visible from one side. I resolved this by setting the material property to `side: double`.
2. **Asset Loading:** To prevent the scene from loading before the large 2K textures were ready, I utilized the `<a-assets>` management system to pre-buffer images.
3. **Scale & Viewport:** Because the realistic distances made the system very large, I had to adjust the camera's initial Z-position and clipping plane to ensure the entire system was visible upon launch.

## Status of Code
The application is **fully functional**. 
All eight planets revolve at proportional speeds, the Moon orbits the Earth correctly, and the Milky Way background renders without seams.

## Time Spent
- **Research & Setup:** 1 hour  
- **Coding & Animation Logic:** 2 hours  
- **Texture Mapping & Troubleshooting:** 1.5 hours  
- **Total Time:** ~4.5 hours across 3 days
