# RLengine 7.0 — Official Release!

The wait is finally over—**RLengine 7.0** is officially live today! 

After a deep code audit, patching 7 internal vulnerabilities, and finishing the core systems to match the architectural specs, this release marks the biggest technological leap for the engine since 6.0.

---

## What's New in RLengine 7.0

* **PBR Rendering & ACES Tonemapping:** Upgraded from hardcoded Blinn-Phong to a physically-based **Cook-Torrance GGX** lighting pipeline with ACES tonemapping and realistic materials.
* **Hardware Z-Buffer (Depth Testing):** Full `D32_FLOAT` Depth-Stencil pipeline integration for accurate 3D occlusion across complex scenes.
* **Unified RHI (DirectX 12 + DirectX 11):** Dual-backend Render Hardware Interface supporting modern **DirectX 12 (RTX 2000–5000)** alongside a **DirectX 11 fallback (GTX 500+ Fermi/Kepler)** with multi-model shader compilation (SM 5.0 – 6.8).
* **Built-In Physics Engine:** Added custom physics simulation featuring gravity, floor collisions, and sphere-to-sphere dynamics.
* **GPU-Instanced Particle System:** New `ParticleSystem` capable of rendering massive particle effects via hardware instancing.
* **Expanded 12-Component ECS:** Tripled the Entity Component System capabilities (from 4 to 12 components), adding lights, PBR materials, colliders, and physics bodies.
* **Blender-Style Editor Suite:** Revamped workspace featuring a 3D Viewport (T-panel, Gizmo Compass, overlays), Outliner with collections and visibility filters, vertical Properties N-panel, interactive Timeline, and Lua REPL console.
* **Security & Multithreading Polish:** Patched 7 core vulnerabilities and optimized worker thread management.

---

## RLengine 6.5 vs. RLengine 7.0 — Comparison

| Subsystem / Feature | RLengine 6.5 | RLengine 7.0 |
| :--- | :--- | :--- |
| **Lighting & Shading** | Blinn-Phong (Hardcoded) | **PBR (Cook-Torrance GGX) + ACES** |
| **Depth Testing (Z-Buffer)** | Missing | **Full Hardware Z-Buffer (`D32_FLOAT`)** |
| **Graphics API (RHI)** | DirectX 12 Only | **Unified RHI: DirectX 12 + DirectX 11 Fallback** |
| **Shader Compiler** | Single Target | **Multi-Model SM 5.0 – 6.8** |
| **Physics System** | None | **Built-in (Gravity, Floor, Colliders)** |
| **Particle System** | None | **GPU-Instanced `ParticleSystem`** |
| **ECS Architecture** | 4 Core Components | **12 Components (Lights, Materials, Physics)** |
| **Editor UI** | Basic ImGui Panels | **Blender-Style Workspaces (Outliner, N/T-Panels, Gizmo, Timeline)** |
| **Scripting & Tools** | Basic Lua | **Interactive Lua REPL + Status Bar** |
