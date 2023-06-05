---
title: 3D Model
---

This page demonstrates in-browser 3D rendering using the html `<model-viewer>` tag. The HTML to implement model viewing can be found [here](https://modelviewer.dev/)

`<model-viewer>` only works with **GLTF** files, which can be saved from Inventor 2023 (although I wasn't able to save them from SOLIDWORKS). For displaying [crystal lattices](lattice.md), JSmol is used instead, since it can directly display CIF files.

<!-- Import the component -->
<script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/3.1.1/model-viewer.min.js"></script>

<!-- Use it like any other HTML element -->
<model-viewer alt="The MatLib logo" src="assets/matlib.glb" ar shadow-intensity="1" camera-controls touch-action="pan-y"></model-viewer>

