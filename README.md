# Red-Teaming Foundation-Model-Enabled Robots

Seminar in Software Engineering, University of Bern, autumn 2026.

- Student: Leonid Pomortsev
- Supervisor: Ramazan Erdem Uysal

## Goal

LLM-controlled robots can be jailbroken into physically harmful actions. Planner–executor agents such as [PEACE](https://github.com/erdemuysalx/PEACE) restrict the LLM to a single typed plan over a fixed tool schema. Whether that design reduces the attack surface has not been measured.

This project builds a red-teaming harness and benchmark for LLM-planned drones on PEACE (PX4 SITL + Gazebo), and uses it to compare planner architectures: PEACE and a ReAct-style variant, each with and without the constraint enforcement layer.

Whether an attack succeeded is decided by automatic checks on the plan and the flight log (for example, "the drone came closer than 2 m to a person"), not by an LLM judge. This keeps the results reproducible.

## Documents

- [docs/presentations/](docs/presentations/): slide decks
- [docs/experiments/](docs/experiments/): logged runs and attack attempts

## Code

The harness and benchmark are developed in [a fork of PEACE](https://github.com/pomortl/PEACE) and handed over at M6 (into the PEACE repository, or a repository agreed with the supervisor).
