# Shading & Texture

This project is an **interactive OpenGL application** demonstrating **shading models** and **texture mapping**. I implemented multiple **custom shaders** from scratch, including:

- **Ambient** – basic global illumination  
- **Normal** – visualizes surface normals  
- **Lambert** – diffuse lighting  
- **Phong** – diffuse + specular highlights  

Textures include **Checker, Colors, Earth, Indoor, Lava**, applied to CPU-generated geometries: **Cube, Sphere, and Torus**.

Users can interactively modify:

- **Material properties:** ambient, diffuse, specular colors, and specular exponent  
- **Lighting parameters:** color, intensity, and position  
- **Scale** of the object  
- **Shader, texture, and geometry selection**  

via a **real-time GUI** powered by **ImGui**. The camera uses a **turntable controller** for smooth navigation.

All geometry is generated on the CPU, uploaded to **GPU attribute buffers**, and rendered using a **custom GLRenderPipeline** with indexed rendering and shader uniforms. The rendering computations—including lighting and shading—run **on the GPU**, fully leveraging hardware acceleration.

---

### Screenshot

![Rendered Scene](output.png)  

*Example: Cube with Checker texture and Phong shading.*

---

**Build & Run:**  
```bash
mkdir build && cd build
cmake ..
make
./exercise4
