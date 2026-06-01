# 12 — 3D Websites

## When to Use 3D

### 3D Adds Value When:
- **Product visualization** — Customers need to see product from all angles
- **Brand storytelling** — Immersive narrative experiences
- **Hero impact** — Memorable first impression
- **Interactive demos** — Users explore the product
- **Data visualization** — Complex data in 3D space
- **Games/ entertainment** — Inherently 3D

### 3D HURTS When:
- **Content is primary** — Reading text over 3D backgrounds (accessibility)
- **Performance is critical** — Ecommerce, high-traffic landing pages
- **Low-end devices** — Many users on old phones
- **No clear purpose** — "3D for the sake of 3D"
- **Slow loading is unacceptable** — 3D adds bundle size

## Technology Stack

### Three.js
The standard WebGL library. Raw JavaScript, maximum control.

**Best for:** Complex 3D scenes, custom effects, maximum flexibility
**Bundle size:** ~150kb gzipped (core + modules)

### React Three Fiber (R3F)
React renderer for Three.js. Declarative 3D.

**Best for:** React projects, component-based 3D, state-driven scenes
**Bundle size:** ~150kb + React overhead

**Key packages:**
- `@react-three/fiber` — Core renderer
- `@react-three/drei` — Helpers (controls, loaders, geometries)
- `@react-three/postprocessing` — Effects (bloom, depth)
- `@react-three/cannon` — Physics

### Spline
Visual 3D design tool. Export as code or embed.

**Best for:** Quick 3D, designers without coding, simple interactive scenes
**Bundle size:** 50-200kb depending on scene
**Limitations:** Less control than Three.js

### Model Formats

| Format | Best For | Notes |
|--------|----------|-------|
| **GLTF/ GLB** | Universal 3D | Standard web format, draco compression |
| **FBX** | Animation | Heavy, convert to GLTF for web |
| **OBJ** | Simple geometry | No animation support |
| **USDZ** | Apple AR | iOS Quick Look |
| **PLY** | Point clouds | Large data sets |
| **STL** | 3D printing | No color/ texture |

## Common 3D Web Patterns

### 1. Hero 3D Object
A single 3D object in the hero section. Rotates slowly or responds to mouse.

**Implementation:** Three.js/R3F with OrbitControls or custom rotation
**Performance:** 1 mesh, simple geometry, low poly count
**Best for:** Product showcase, brand mascots, geometric art

### 2. 3D Background
Full-screen 3D scene behind content. Subtle, never distracts.

**Implementation:** Particles, geometric shapes, low-poly landscape
**Performance:** Keep simple (shapes with emission, no heavy textures)
**Best for:** Premium landing pages, creative portfolios

### 3. Interactive 3D Gallery
Users click/ drag to explore 3D space with content items.

**Implementation:** Three.js with raycasting for click detection
**Performance:** Moderate — each item adds geometry
**Best for:** Portfolio, product showcase, real estate

### 4. 3D Data Visualization
Data represented in 3D space (bar charts, globe, network graphs).

**Implementation:** Three.js + data mapping
**Performance:** Depends on data points (use instancing for 1000+)
**Best for:** Analytics dashboards, scientific data, globes

### 5. 3D Product Viewer
Rotate, zoom, inspect product from all angles.

**Implementation:** OrbitControls + HDRI lighting
**Performance:** Model quality vs performance tradeoff
**Best for:** Ecommerce, automotive, furniture, fashion

### 6. Scroll-Triggered 3D
3D scene changes as user scrolls (camera moves, objects transform).

**Implementation:** R3F + useScroll (or GSAP ScrollTrigger with Three.js)
**Performance:** Calculate based on scene complexity
**Best for:** Storytelling sites, product launches, case studies

## 3D Performance Optimization

### Poly Count Guidelines
- **Mobile hero object** — < 10,000 polygons
- **Desktop hero object** — < 50,000 polygons
- **Complex product showcase** — < 100,000 polygons
- **Background/ decoration** — < 5,000 polygons

### Texture Optimization
- Maximum texture size on mobile: 1024x1024
- Maximum texture size on desktop: 2048x2048
- Use JPEG for color maps (smaller files), PNG for transparency
- Compress with Basis/ KTX2 for GPU compression
- Use mipmaps for textures viewed at different distances

### Draw Calls
Keep draw calls under:
- **Mobile:** 50-100
- **Desktop:** 100-200
- Strategies: Instancing, merging geometries, texture atlases

### Mobile-Specific
- Detect mobile: `navigator.maxTouchPoints > 0`
- Lower pixel ratio: `renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2))`
- Disable post-processing effects on mobile
- Reduce shadow map resolution
- Simplify or remove particle systems
- Use lower-poly LOD (Level of Detail) models

### Fallback Strategy
Always provide a non-3D fallback:
1. Detect WebGL support — `try/catch` on canvas creation
2. Detect performance — Check framerate after 2 seconds
3. Provide static image or reduced animation
4. Show a meaningful message if 3D fails

## Three.js Starter Patterns

### 1. Floating Object
```js
// Scene, camera, renderer setup
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera(75, width/height, 0.1, 1000);
const renderer = new THREE.WebGLRenderer({ antialias: true });

// Geometry with material
const geometry = new THREE.IcosahedronGeometry(1, 1);
const material = new THREE.MeshPhysicalMaterial({
  color: '#8B5CF6',
  metalness: 0.3,
  roughness: 0.2,
});
const mesh = new THREE.Mesh(geometry, material);
scene.add(mesh);

// Float animation
function animate() {
  requestAnimationFrame(animate);
  mesh.rotation.x += 0.005;
  mesh.rotation.y += 0.01;
  mesh.position.y = Math.sin(Date.now() * 0.001) * 0.2;
  renderer.render(scene, camera);
}
animate();
```

### 2. Particle System
```js
const particleCount = 1000;
const geometry = new THREE.BufferGeometry();
const positions = new Float32Array(particleCount * 3);

for (let i = 0; i < particleCount * 3; i++) {
  positions[i] = (Math.random() - 0.5) * 10;
}

geometry.setAttribute('position', new THREE.BufferAttribute(positions, 3));
const material = new THREE.PointsMaterial({
  color: '#ffffff',
  size: 0.05,
  transparent: true,
  opacity: 0.8,
});
const particles = new THREE.Points(geometry, material);
scene.add(particles);
```

### 3. Mouse-Responsive Scene
```js
document.addEventListener('mousemove', (e) => {
  const x = (e.clientX / window.innerWidth) * 2 - 1;
  const y = -(e.clientY / window.innerHeight) * 2 + 1;
  mesh.rotation.y = x * 0.3;
  mesh.rotation.x = y * 0.3;
});
```

## 3D Animation Tools

### Spline (No-Code 3D)
- Visual editor for 3D scenes
- Export to React component or vanilla JS
- Events: hover, click, mouse enter/leave, collision
- State machine for interactive behaviors
- Embed via iframe or npm package

**Best for:**
- Designers who can't code 3D
- Quick interactive prototypes
- Simple product showcases
- Animated backgrounds

### Blender → Web Pipeline
1. Model in Blender
2. Rig and animate (if needed)
3. Export as GLTF/ GLB with Draco compression
4. Use Three.js GLTFLoader to import
5. Apply transforms, materials, animations in code

## 3D Accessibility

### 3D Accessibility Rules
- Don't auto-rotate 3D objects (provide play/pause)
- Provide reduced-motion alternatives
- Ensure content is readable over 3D backgrounds
- Don't require 3D interaction for key functionality
- Keyboard-navigable 3D interactions where possible
- Alt text for 3D content

## 3D Decision Checklist

- [ ] 3D serves a clear purpose (visualization, storytelling, impact)
- [ ] Mobile performance tested (< 50 draw calls, < 10k polys)
- [ ] WebGL fallback provided (static image, 2D animation)
- [ ] Reduced motion alternative exists
- [ ] 3D asset optimized (Draco compression, mipmaps)
- [ ] Loading state shown while 3D loads
- [ ] Bundles are code-split (3D loaded after main content)
- [ ] Interaction doesn't interfere with page functionality
- [ ] Content is readable above/below 3D scene
- [ ] Battery impact considered (reduce on low power mode)
