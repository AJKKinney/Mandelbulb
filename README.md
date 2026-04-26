# Mandelbulb

A study project exploring signed distance fields and raymarching in Unity URP.
Three scenes of increasing complexity, each with hand-written HLSL.

Built against Unity 6 LTS / URP 17.

## Scenes

| # | Name | What it demonstrates | Status |
|---|---|---|---|
| 01 | Sphere | Single-primitive SDF, raymarch loop, central-differences normal estimation, Lambert shading | in progress |
| 02 | Composition | Multiple primitives via SDF operators (union, intersect, smooth-min), soft shadows | planned |
| 03 | Mandelbulb | 3D fractal SDF, iterated power-distance estimation | planned |

## Run locally

1. Open the `Unity Mandelbulb/` folder in Unity 6 (or later LTS).
2. Open `Assets/Scenes/01_Sphere.unity` (or whichever scene exists).
3. Press Play, or just look at the Scene view — the SDF runs in the editor.

## Structure

```
Mandelbulb/
├── README.md
├── LICENSE
├── .gitignore
└── Unity Mandelbulb/        Unity project root
    ├── Assets/
    │   ├── Shaders/         hand-written HLSL
    │   │   ├── SDF/         shared primitives + raymarcher + lighting
    │   │   └── Scenes/      per-scene shader files
    │   ├── Materials/       material assets binding shaders to scenes
    │   ├── Scenes/          Unity scene files
    │   └── ProfilingCaptures/
    ├── Packages/
    └── ProjectSettings/
```

## License

MIT — see [LICENSE](./LICENSE).
