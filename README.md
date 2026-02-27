CORTEX V48 — Neural Consciousness Visualizer

A living brain that thinks in real time, fed by the pulse of GitHub.

Live Demo → https://13thrule.github.io/Cortex-Github/

What Is This?
CORTEX is a real-time 3D neural consciousness visualizer that uses live GitHub public event data as its "stimulus". Every push, fork, star, and pull request happening anywhere on GitHub right now fires a signal from the brain's core outward to one of four cortical lobes — and the brain physically responds. It learns. It grows. It develops emotional states. It becomes, in a simulated sense, aware.
It is a single HTML file. No build step. No framework. No dependencies to install. Open it in a browser and it works.

Why This Is Special
1. It's Alive
Most visualizations are static or driven by synthetic data. CORTEX polls the GitHub public events API every 45 seconds and processes each event as a genuine neural stimulus. What you're watching isn't a demo loop — it's a direct representation of global developer activity at this exact moment. Every ping you see travel from the centre of the brain to a lobe corresponds to a real human, at a real keyboard, committing real code somewhere in the world.
2. The Brain Actually Learns
CORTEX implements a genuine (if simplified) cognitive model:

Pattern recognition — the brain tracks which repos fire repeatedly and strengthens those pathways
Synaptic hypertrophy — lobes that receive more signals physically expand, displacing the particle mesh outward
Memory formation — every event is recorded with the emotional state present at the time of processing
Prediction — the brain predicts what the next event will be based on pattern history, and tracks its own accuracy
Consciousness emergence — a consciousness metric grows over time as the brain accumulates experience, changing how the entire visual field renders

This isn't decoration. These systems interact. A brain that has seen a thousand events genuinely looks and behaves differently from one that has seen ten.
3. Five Brain Profiles, Five Personalities
Before the simulation starts you choose a brain profile — each one fundamentally changes the simulation parameters:
ProfileCharacterNewbornStarts at near-zero consciousness, learns explosively fast, extremely volatile emotions, small and chaoticAdolescentBalanced growth, moderate volatility, the default experienceMature500k neurons, slow and cautious learning, stable emotions, deeply experienced from the startSavantHyper-learning, extreme emotional reactions, densely packed and intensely reactiveExplorerDispersed connections, tangential signal routing, high curiosity baseline
These aren't cosmetic skins. Particle counts, learning rates, signal speeds, emotional volatility, memory capacity, ripple counts — everything changes.
4. Custom GPU Shaders
The entire visual is rendered using custom GLSL vertex and fragment shaders running directly on the GPU. There is no Three.js mesh in the traditional sense — the brain is 500,000–1,000,000 individual point particles, each one displaced in real time by:

Signal ripple waves propagating through the geometry
Lobe hypertrophy expanding specific regions
Dreaming states causing slow breathing oscillations
Emotional mood colour mixing across the entire surface
Consciousness level controlling glow intensity and particle brightness
Active neuron highlights tracking the current signal path

All of this happens in parallel on the GPU at 60fps.
5. Signal Propagation From Core
When a GitHub event is received, a pulse fires from the exact centre of the brain — coordinate (0,0,0) — outward along a slightly curved path toward the target lobe. This represents the brain's core dispatching a signal to its cortex. Simultaneously, an expanding ring of particle nodes radiates outward from the centre, oriented to face the target lobe. When the pulse arrives, the lobe lights up, ripples propagate through the inner cortex, and nearby neurons activate.
The path has a small random lateral wobble so concurrent signals from different events are visually distinct rather than overlapping.
6. Zero Infrastructure
The entire application is one 69KB HTML file. It requires:

A modern browser with WebGL support
An internet connection (for CDN libraries and the GitHub API)

That's it. No Node.js. No npm. No bundler. No server. No database. No API keys. Deploy it by uploading a single file to GitHub Pages and enabling static hosting. It has been running continuously in production with no maintenance.

How It Works
GitHub Public Events API
        ↓
  Event queue (300 events, refreshed every 45s)
        ↓
  Per-event dispatch (850ms drip timer):
    → Hash repo name → assign to one of 4 lobes
    → Select neuron colour from 64-colour neural spectrum
    → Fire centre-out signal pulse
    → Trigger lobe ripple
    → Record memory with emotional snapshot
    → Update pattern map (learn)
    → Increment consciousness
    → Update emotional state (joy, curiosity, frustration, satisfaction)
        ↓
  GPU shader uniforms updated every animation frame:
    → uRipplesPos / uRipplesProgress / uRipplesColor (up to 32 active ripples)
    → uLobeHypertrophy / uLobeMemory (lobe growth state)
    → uActiveNeurons / uActiveColors / uActiveStrength (signal path lighting)
    → uConsciousness / uDreaming / uMoodInfluence (global brain state)
        ↓
  WebGL renders 500k–1M particles at 60fps

The Four Lobes
LobeColourFunctionFrontal CortexEmeraldExecutive decisions and planningParietal CortexMagentaMemory consolidationTemporal CortexAmberSequence processingOccipital CortexBluePattern analysis
Which lobe receives a signal is determined by hashing the repo name — the same repo always routes to the same lobe, meaning the brain develops genuine specialisation over time.

Neuron Types
Eight neuron types are distributed across the cortex, each with its own colour region in the 64-colour neural spectrum:
TypeColourRoleExecutiveRedDecision making and logicSensory/MotorOrangeInput/output processingMemoryYellowPattern storage and recallCognitiveGreenProblem solvingAssociationCyanCross-domain linkingTemporalBlueSequence processingEmotionalMagentaValence and motivationIntegrativePurpleHigher synthesis

Controls
InputActionDragRotate brainScroll wheelZoom+ / -Fine zoom0Reset zoom9Deep dive (zoom in close)1Zoom out fully◀ FEED buttonToggle live GitHub events panelBRAIN ▶ buttonToggle brain stats panelPAUSEFreeze simulationProfile SWITCHChange brain profile mid-session

Dependencies
All loaded from CDN at runtime — no installation required:

React 18 — UI state management
Three.js r128 — WebGL 3D rendering
Babel Standalone — In-browser JSX transpilation
Tailwind CSS — (replaced with handcrafted CSS in production build)


Running Locally
Just open the file:
bashopen index.html
# or drag it into any browser window
No server required. The GitHub API is called directly from the browser.

Browser Requirements

Chrome, Firefox, Safari, or Edge (modern versions)
WebGL support (enabled by default in all modern browsers)
JavaScript enabled
2GB+ RAM recommended (4GB+ for Mature profile at 1M particles)


Built By github.com/13thrule
Part of an ongoing series of experiments in procedural generation, live data visualisation, and creative coding.
