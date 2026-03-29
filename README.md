# n-body

Simple web-based animation of the n-body gravitational problem. Bodies interact through Newtonian gravity, integrated with the velocity-Verlet method, and rendered in real time using D3.js.

## Features

- Adjustable number of bodies, simulation speed, trail length, and gravitational constant
- Drag bodies to reposition them during the simulation
- Edit body properties (position, velocity, mass) in the sidebar table
- Preset and random initial configurations
- Real-time display of simulation time, total energy, and per-body tooltips

## Download and Installation

### Prerequisites

- [Python 3.8+](https://www.python.org/downloads/)
- [pip](https://pip.pypa.io/en/stable/installation/) (included with most Python installations)
- [Git](https://git-scm.com/downloads) (to clone the repository)

### Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/boswald314/n-body.git
   cd n-body
   ```

2. **Create a virtual environment (recommended)**

   ```bash
   python -m venv venv
   source venv/bin/activate        # Linux / macOS
   venv\Scripts\activate           # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**

   ```bash
   python app.py
   ```

   The server starts at **http://127.0.0.1:5000**. Open that URL in a browser to use the simulator.

5. **Enable debug mode (optional)**

   ```bash
   FLASK_DEBUG=true python app.py
   ```

## Usage

- Use the **Bodies** slider to choose how many bodies appear.
- Click **▶ Start** to begin the simulation and **⏸ Pause** to stop it.
- Click **↺ Reset** to return bodies to their last saved state.
- Click **⚄ Random** for a random configuration or **☀ Preset** for a curated one.
- Drag any body in the viewport to move it; its velocity resets to zero on release.
- Edit exact values in the sidebar table, then click **↺ Reset** to apply them.

## Future Work

- **3D visualization** — extend the renderer to three dimensions using WebGL or Three.js.
- **Collision detection and merging** — allow bodies to merge on close approach, conserving momentum and mass.
- **Barnes–Hut optimization** — implement the Barnes–Hut tree algorithm to scale the simulation to thousands of bodies.
- **Importable scenarios** — let users save and load body configurations as JSON files.
- **Adaptive time-stepping** — automatically adjust the integration time step based on closest-pair distance to improve accuracy during close encounters.
- **Performance metrics** — display frames per second and integration error over time.
- **Mobile-friendly layout** — make the control panel responsive so the simulator works well on tablets and phones.
