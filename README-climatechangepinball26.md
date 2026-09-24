# 🌍 Pinball: Climate Change Emergency

> *"Wise Apes... Unwise? Restore Planetary Equilibrium."*

**Pinball: Climate Change Emergency** is a browser-based, high-fidelity retro arcade pinball experience built around planetary climate dynamics, regenerative ecological solutions, and real-time rigid-body vector physics. Players launch the Earth into a precarious biosphere balance, navigating industrial hazards, unlocking renewable energy infrastructure, activating global collaboration powers, and advancing from critical tipping points toward full planetary syntropy.

* **Live Deployment:** [https://adespress.github.io/climatechange-pinball/](https://adespress.github.io/climatechange-pinball/)
* **Primary Web Entrypoint:** `index.html`
* **Literary Publication Tie-In:** [Ade's Press](https://paragraph.com/@adespress)
* **Dedicated Soundtrack:** [Embertime on Spotify](https://open.spotify.com/artist/7ekDOUV7qs60NE5g1E7KaR?si=wHMZDPdhQ5GtaSCVS6q-aw)

---

## 🛠️ Developer Notes

> **Vibe Coding & Scope Note:**  
> The application seemed to become too large to vibe code, so the planned feature of more text appearing when obstacles are hit was not possible in this build.  
> 
> *Note: Alternative versions or modular builds may be available.*

---

## 🕹️ Game Overview & Modes

The arcade cabinet features distinct operational modes calibrated for different gameplay paces and ecological challenges:

### 1. ⚠️ Crisis Mode (Standard Arcade)
* **Objective:** Score **30,000 Biosphere Points** within **5 minutes** to avert ecological collapse.
* **Failure Condition:** Falling to **-500 points** triggers irreversible thermal runaway (*Climate Collapse*).
* **The Deniability Zone:** Striking industrial culprits (Coal Power, Big Oil, Mass Aviation, Deforestation) subtracts points and spikes global temperature anomalies.
* **Acoustics & Visuals:** Pulsing crimson bezel warnings, retro rising laser sweeps, and emergency siren alerts during final countdowns.

### 2. 🌱 Super Harmonious Mode
* **Trigger:** Unlocked automatically upon crossing the **30,000-point threshold** or entering the central transition portal.
* **Mechanics:**
  * Industrial hazards transform into regenerative solutions (Solar Arrays, Wind Turbines, Regenerative Agriculture, Permaculture, Circular Economies).
  * Timers disengage, granting unconstrained play to explore deep-game syntropic milestones.
  * **Biosphere Resilience:** For every 500 points earned above 10,000, invisible safety cushions build at the bottom drain to rebound the Earth safely back into play.

### 3. 🌿 Pure Harmonious Zen Mode
* **Dedicated Mode:** Accessible from the title screen via the **Harmonious Coin** slot.
* **Duration:** Relaxed **10-minute** exploration clock.
* **Physics Modulation:**
  * Flipper snap rate softened to `0.38` for smooth, cushioned sweeps.
  * Ball damping relaxed for floating, buoyant trajectory curves.
* **The Central Tree of Life:** An interactive arboreal bumper positioned in the basin with organic directional impact detection, deflecting rolls softly while repelling upward strikes toward high-canopy clean energy targets.
* **Sunset Drift Warning (9:00 - 10:00):**
  * Transition from dark slate to a warm amber gold pulse (`.clock-alert-zen`).
  * Dual-harmonic Tibetan singing bowl chimes ($528\text{ Hz}$ fundamental $+ 1056\text{ Hz}$ overtone) at 60s and 30s remaining.
  * Whisper-soft sine water-droplet ticks during the final 10 seconds (no harsh square waves or sirens).
* **Target:** Achieve **80,000 Biosphere Points** before sunset.

### 4. 🤖 AI-Generated Topical Table (BYOK)
* **Custom Scenarios:** Uses the Google Gemini API to synthesize custom, topical pinball tables generated from recent climate and environmental developments.
* **Tactical Briefing:** Delivers real-time mission dispatches detailing current ecological threats, bespoke hazard obstacles, and targeted clean mitigations before launch.
* **Bring-Your-Own-Key:** Secure client-side execution—API keys are stored strictly in session memory.

---

## 🎮 Mechanics & Controls

### Physical Controls

| Action | Keyboard | Touch / Arcade Controls |
| :--- | :--- | :--- |
| **Left Influencer (Flipper)** | `A` or `Left Arrow` | Left Arcade Button (`#leftFlipperBtn`) |
| **Right Influencer (Flipper)** | `D` or `Right Arrow` | Right Arcade Button (`#rightFlipperBtn`) |
| **Plunger (Earth Launch)** | `Spacebar` or `Down Arrow` | Launch Plunger Button (`#plungerBtn`) |
| **Global Collaboration Power** | Hold **Both Flippers** | Hold **Both Left & Right Influencer Buttons** |

### 🤝 Global Collaboration Power-Up
Holding down both flippers simultaneously engages the global collaboration pull-up mechanic, creating a sustained upward atmospheric tractor current that lifts the ball away from danger zones and propels it toward upper canopies.
* **In Crisis Mode:** Produces a retro rising laser power-up sweep ($110\text{ Hz} \to 1760\text{ Hz}$).
* **In Harmonious Mode:** Triggers an airy, bandpass-filtered wind sweep layered with an ethereal sine chord and a delicate leaf-rustle flutter.
* **In Zen Mode:** Dynamically scales audio volume down by approximately $45\%$ ($-5.2\text{ dB}$) to preserve a meditative state.

---

## 🏆 Scoring Milestones & Progression Ladder

| Milestone | Title | Unlocks & Ecological Impact |
| :--- | :--- | :--- |
| **30,000 PTS** | **Earth Is Healing** | Averts initial tipping point; neutralizes negative hazards; unlocks Super Harmonious mode. |
| **50,000 PTS** | **Solar Aurora & Climax Forest** | Ignites atmospheric auroral canopy; expands dense 15-tree rainforest; provides 100% Biosphere Resilience drain buffer. |
| **80,000 PTS** | **Syntropy & Permaculture** | Continental reforestation; opens wild pollinator pathways; cleans ocean dead zones; stabilizes zero-carbon grid. |
| **100,000 PTS** | **Green Wise Gamer Award** | Attains **Nature-Nurturer Mage** status. Celebrates ecological restoration and invites the player to step away from the screen and join the real-world Regenerative Age. |

---

## 🔊 Audio Architecture (`RetroSynthAudio`)

The application features a fully custom, zero-dependency procedural audio engine written entirely on the **Web Audio API**:
* **Zero External Audio Assets:** All sound effects, alarms, laser blasts, wind rushes, and chimes are synthesized directly in code via runtime mathematical oscillators and noise buffers.
* **Acoustic Smoothing Envelopes:** Every generated frequency is bounded under $600\text{ Hz}$ on standard pings, and exponential curves ramp from finite non-zero thresholds (`0.0001`) to eliminate digital clicking, harsh high-frequency fatigue, or audio pops.
* **Bespoke Acoustic Elements:**
  * **Biodiversity Slingshot (`playBeeBuzz`):** Dual detuned triangle waves with a $42\text{ Hz}$ LFO wing-flutter modulation.
  * **Wind Bumper (`playWindWhoosh`):** Bandpass-filtered white noise sweep layered over subtle harmonic flutes ($D_4, A_4, D_5$).
  * **Clean Energy Bumper (`playLowLaserSpaceyBlast`):** Low resonant triangle drop ($310\text{ Hz} \to 52\text{ Hz}$) through a $4.2\ Q$ resonant filter and spacey feedback delay.
  * **Central Tree (`playSpaceyBounce`):** Whisper-soft $440\text{ Hz}$ sine chime drifting into an atmospheric spatial delay loop.
  * **Tibetan Singing Bowl (`playZenWarningChime`):** Dual sustained harmonic sines at $528\text{ Hz}$ and $1056\text{ Hz}$ with a $2.4$-second exponential decay.
* **Soundtrack Integration:** Direct links to original music by **Embertime** on Spotify, coupled with a 4-stage in-engine volume control stepper and master mute toggle.

---

## 💻 Tech Stack & Architecture

* **Architecture:** Self-contained, single-file HTML5 web application (`index.html`).
* **Display Engine:** High-performance HTML5 `<canvas>` 2D rendering pipeline operating at a native 60 FPS with pixel-ratio scaling.
* **Styling & Typography:** Tailwind CSS (via CDN) paired with Google Fonts (*Orbitron*, *Press Start 2P*, and *Inter*).
* **Physics Subsystem:** Custom 2D rigid-body vector engine featuring raycast flipper interception, continuous circular collision resolution, kinetic bounce damping, and gravity scaling.
* **Persistence:** Browser `localStorage` retains local Top 10 High Scores, initials, and unlocked status tiers.

---

## 🚀 Deployment & Web Execution

### Running Live Online
Play directly via GitHub Pages:  
👉 **[https://adespress.github.io/climatechange-pinball/](https://adespress.github.io/climatechange-pinball/)**

### Local Execution
1. Clone or download the repository files.
2. Ensure the primary game file is named `index.html` (or `pinball_climate_emergency.html`).
3. Open `index.html` directly in any modern web browser (Google Chrome, Firefox, Safari, or Microsoft Edge).
4. No build tools, Node.js packages, npm installs, or external web servers are required.

### Touch & Mobile Optimization
The interface includes mobile viewport defenses (`touch-action: none;`, `-webkit-touch-callout: none;`) and iOS safe-area inset adaptation for edge-to-edge mobile play.

---

## 📖 Credits & Community

* **Creator / Design:** Ade mc (2026).
* **Literary Tie-In:** Discover more ecological literature and projects through [Ade's Press](https://paragraph.com/@adespress), including *The Power of Pruning: Your Mind and Your Life*.
* **Music:** Dedicated soundtrack integration featuring [Embertime on Spotify](https://open.spotify.com/artist/7ekDOUV7qs60NE5g1E7KaR?si=wHMZDPdhQ5GtaSCVS6q-aw).





Credits & Provenance Concept, Game Design & Direction: Ade M. Campbell Development & Tooling: Prompted and edited by Ade M. Campbell, September 2026, in Gemini Canvas principally using Flash 3.8 and Extended. Publication & Related Works: Produced in connection with Ade's Press (art, writing etc. by Ade mc). This project is open-source and distributed under the MIT License.
