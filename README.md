# 3D printing as a process

**From intention to object** — *Artefact × Software × Hardware* — and how they talk to each other.

This repository hosts an interactive **Excalidraw** canvas for the diagram [`public/3d-printing-as-process.excalidraw`](public/3d-printing-as-process.excalidraw). The web app loads that scene so you can pan, zoom, and explore the full map. The sections below mirror the ideas captured in that file.

---

## Artefact

*What role does it play?*

The physical outcome is not “just a shape”: it carries **role**, **requirements**, **geometry**, and **connections** into the rest of the system.

### 1. Role / purpose

Examples called out in the diagram:

- **Final object** — the piece is the goal.
- **Mold / scaffold** — receives another material.
- **Platform for a process** — hosts a workflow beyond the print itself.
- **Negative or physical structure** — cavities, sacrificial geometry, or spatial definition.
- **Connector / node** — sometimes *the piece is the joint*.

### 2. Requirements

Requirements steer both software and hardware:

- **Structural** — load, impact, flex.
- **Environmental** — heat, UV, water.
- **Aesthetic** — layer lines, surface quality.
- **Dimensional** — tight fit, tolerances.
- **Interface / tool** — adapter, grip, jig.
- **Experimental carrier** — growth, flow, texture.
- **Economic** — cost, speed, weight.
- **Life cycle** — repair, recycle.

### 3. Geometry & volume

- **Solid / shell / lattice / gyroid** — how matter is distributed.
- **Scale & decomposition** — one piece or a tiled kit.
- **Printability** — watertight / manifold models.
- **Repair** — holes, normals.
- **Checks** — wall thickness, dimensions.

### 4. Connections

Connections link the artefact to modules, other materials, or bodies (wearables, interfaces):

- **Type** — fixed (glue, screw), reversible (snap, magnet, press), dynamic (hinge, gear, living hinge).
- **2D → 3D** — overhangs and supports.
- **Modularity** — tiles, parametric kits.

> Sometimes the connection is not secondary — **the artefact is the joint.**

*Requirements drive choices in hardware and software. Connections emerge from geometry and materials.*

---

## Software (pipeline)

The diagram frames software as the bridge **from geometry to slicing** — translating intention into machine-ready instructions.

### ① Geometry creation

- **CAD / sculpt / scan** — classical modeling, organic forms, or captured reality.
- **Mesh** — watertight, suitable for the next steps.

**Geometry creation tools** (examples in the diagram):

- Classical CAD — e.g. Fusion, SolidWorks.
- Polygon / sculpting — e.g. Blender, ZBrush.
- Parametric / generative — e.g. Grasshopper, OpenSCAD.
- Captured 3D — scan / photogrammetry.

### ② Model preparation

- **Orientation / supports** — printability on the machine.
- **Model preparation checks** — printability, wall thickness, dimensions.

### ③ Slicing — core step

Slicing **defines toolpath logic**. Parameters called out include:

- Layer height, part orientation, infill pattern, toolpath perimeters, temperature, support strategy — culminating in **G-code / machine files**.

### ④ Simulation & monitoring

- **Structural simulation** — bend, deform, break.
- **Process simulation** — warp, shrink, stress.
- **Cameras & sensors** — error detection, warping, process monitoring.

*Same logical pipeline can describe many different machines and materials — the diagram links this idea to “infinite variations” once the relationships are understood.*

---

## Hardware

### Materials — by family

| Family | Examples (from the diagram) |
|--------|-----------------------------|
| Metals | Steel, titanium, aluminum |
| Polymers | PLA, ABS, PETG, nylon, TPU, resins (SLA/DLP) |
| Minerals | Ceramics, concrete, plaster |
| Biomaterials | Bio-inks, hydrogels |
| Edible | Chocolate, sugar, dough |
| Composites | Carbon fiber, wood fill |

### Materials — by physical state

- Solid filament — typical of **FDM / FFF**
- Granules / pellets — large-format extrusion
- Powder — **SLS**, **SLM**, binder jet
- Liquid resin — **SLA**, **DLP**, LCD vat processes
- Paste / gel — clay, food, bio
- Sheet — lamination approaches

### Processes = material × machine

**Extrusion** — FDM / FFF: nozzle deposition with filament and pastes; strong fit for prototypes and custom parts.

**Powder bed** — SLS, SLM, binder jet: powder fused or bonded selectively; complex shapes and metal parts.

**Resin vat** — light-cured resin (SLA / DLP / LCD).

**Special** — jetting, sheet lamination, DED (e.g. droplets, cut-and-bond stacks, metal repair).

---

## Key idea (from the diagram)

> 3D printing is not just a way to make forms. It is a way to think about **matter**, **function**, and **process** as one system. Every choice — material, geometry, connection — is also a **design decision**.

---

## About this app

The bundled viewer is a **Vite + React + TypeScript** shell around **`@excalidraw/excalidraw`**. On load it fetches `3d-printing-as-process.excalidraw` from `public/` and opens it in the native Excalidraw UI.

### Prerequisites

- Node.js 16+

### Install and run

```bash
npm install
npm run dev
```

Open **http://localhost:3000** (port is set in `vite.config.ts`).

### Build

```bash
npm run build
npm run preview   # optional: preview production build
```

---

## Credits & contact

- **Web:** [schoolai.linalopes.info](https://schoolai.linalopes.info)
- **Address:** Schönaustrasse 13, 8620 Wetzikon, Zürich

## License

MIT
