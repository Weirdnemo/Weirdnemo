<div align="center">

# Nimesh

`Weirdnemo` &nbsp;|&nbsp; `nemo.dev`

Reinforcement learning for spacecraft autonomy, guidance and control.

[![Portfolio](https://img.shields.io/badge/Portfolio-nemo--sol.vercel.app-black?style=for-the-badge&logo=vercel&logoColor=white)](https://nemo-sol.vercel.app)

</div>

---

## 01 / Overview

```text
FOCUS        RL-based spacecraft autonomy, astrodynamics, GNC
STAGE        Final-year engineering student
METHODS      PPO, curriculum learning, custom physics environments
LEARNING     C++, PyTorch internals, SLAM and state estimation (KF, EKF, UKF)
LOOKING FOR  Collaborators on RL and robotics, help deploying large-scale ML systems
NEXT         Fully funded master's programs abroad
```

I build learning agents for problems where the physics is unforgiving: hypersonic reentry, tumbling satellites, and exploration in unmapped space. Most of the work is in the simulator and the reward design rather than the network itself.

---

## 02 / Projects

| Project | Domain | Stack | Status |
|---|---|---|---|
| Starship Reentry | Atmospheric reentry control | Gymnasium, PPO, LSTM | Active |
| Drone RL | Autonomous exploration | Genesis, rsl-rl, PPO | Active |
| UnTumble | Satellite detumbling | MuJoCo, PPO | Complete |
| ExoRL | Exoplanet detection | scikit-learn, batman, Streamlit | Complete |
| Paddock | Multiplayer game | Unity 6, Mirror | Ongoing |

### Starship Reentry

A custom Gymnasium environment with a realistic atmosphere model, aerodynamics, Detra-Kemp-Riddell heating, and g-load constraints. The first 3D formulation ended in overheat termination on every episode, so I moved to 2D, which produced a roughly 20% success rate. Advancing the curriculum into a stochastic atmosphere then caused catastrophic forgetting. Current work focuses on stricter advancement thresholds, gentler uncertainty ramps, and resetting LSTM weights at stage transitions.

### Drone RL

PPO on Genesis using rsl-rl. Waypoint-following collapsed into a zero-mean reward signal, so the task became SLAM-driven exploration: a per-episode occupancy grid with a reward for coverage gained.

### UnTumble

A MuJoCo PPO agent that detumbles a satellite using two chaser vehicles with 20 RCS actuators. Training plateaued near 0.08 rad/s because of a mathematical ceiling created by the fuel penalty. A three-phase curriculum with a temporary entropy bump got it past the plateau.

### ExoRL

Hackathon exoplanet detection on TESS data: BLS/TLS signal search, Random Forest classification, batman transit fitting, and a Streamlit dashboard.

### Paddock (nemo.dev)

A multiplayer hangout and driving game in Unity 6 with Mirror networking. WheelCollider proved unstable at toy scale, so the car uses a raycast and spring model. Also includes an orbital camera rig with SphereCast collision avoidance.

---

## 03 / Toolchain

```text
LEARNING       PyTorch, Stable-Baselines3, rsl-rl, Keras, TensorFlow
SIMULATION     Gymnasium, MuJoCo, Genesis, NumPy, SciPy
VISION         OpenCV
ESTIMATION     Kalman filters (KF, EKF, UKF), SLAM
SCIENCE        scikit-learn, BLS/TLS, batman
TRACKING       MLflow, Streamlit
GAME DEV       Unity 6, Mirror, Godot 4, Blender, C#
DESIGN         Figma, GIMP
LANGUAGES      Python, C++, C, JavaScript
ENVIRONMENT    Fedora, Git, PowerShell
```

---

## 04 / Contact

If you work on RL for spacecraft, drones, or robotics and want a collaborator, get in touch.

[![Portfolio](https://img.shields.io/badge/Portfolio-nemo--sol.vercel.app-black?logo=vercel&logoColor=white)](https://nemo-sol.vercel.app) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/nimesh-chauhan-15348b2b8)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
