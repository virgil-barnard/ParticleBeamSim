# ParticleBeamSim

Browser-based WebGPU experiments for evolving particle populations. Each HTML file is a self-contained simulator branch: particles belong to species, experience local force fields, run compact neural policies, and are selected into new generations from their survival and task performance.

`index.html` opens the current default: [Hierarchical Force Chambers](xenospecies_swarm_hierarchical_force_chambers.html).

## Run it

Open `index.html` or any version listed below in a current browser with WebGPU enabled. Chrome and Edge generally work best. The simulations are GPU-intensive; reduce particle count, interaction samples, or GPU ticks per frame if needed.

The default branch begins simulation automatically. Use **pause**, **reset**, and **seeded** in the HUD to control a run. A reset applies particle/species-count changes; seeded creates a fresh randomized population.

## Start here: Hierarchical Force Chambers

[`xenospecies_swarm_hierarchical_force_chambers.html`](xenospecies_swarm_hierarchical_force_chambers.html) is the current, most complete workspace for studying how neural evolution, inter-species forces, and environments affect one another.

Use it when you want to:

- Evolve multiple particle species with neural controller variants and population-level selection.
- Inspect or edit the species-by-species attraction/repulsion matrix, including matrix evolution, protection of elite relationships, correlation mating, and learned correlation bonds.
- Build a hand-authored curriculum or a seedable generated Forge Lane that ramps behavior targets, complexity, fairness, and terrain geometry.
- Test food, goals, hazards, walls, moving fields, gravity, pheromone trails, and custom arenas.
- Use the compartmentalized Evolution, World Forge, Utility, Brain, Gravity, and Auto-Discovery chambers. Panels can be opened from the glyph menu; many accordions can be reordered or detached.

### Suggested first run

1. Let the default `fg3` arena run for a few generations.
2. Open **Evolution** and tune mutation, selection pressure, or species count. Reset after changing species or particle counts.
3. Open **Force** to inspect the relationship matrix, or lock it to test brains against a fixed ecology.
4. Open **World Forge** to generate a reproducible environment from a seed, or build a Forge Lane for a longer unattended run.
5. Open **Auto-Discovery** to review its adjustments. It is enabled by default in this branch and makes conservative changes after enough generation history has accumulated.

## Also recommended: Alien Nursery Forge

[`xenospecies_swarm_alien_nursery_forge_fixed.html`](xenospecies_swarm_alien_nursery_forge_fixed.html) is a more direct, consolidated version of the same evolutionary simulation. It is a good choice for hands-on environment design and for learning the model without the chamber-oriented layout.

Its main capabilities are:

- A procedural World Forge with behavior targets, controlled complexity/fairness, terrain geometry, seeds, and outcome heatmaps.
- A Nursery Forge editor for a custom canvas: place, move, and erase food wells, goal regions, hazards, and barriers; choose circular or polygonal glyph shapes.
- Species selection, chemistry evolution, neural-controller inspection, pheromone fields, gravity, analytics, champions, agent reports, and experiment import/export.
- A prescribed curriculum lane that can advance through increasingly difficult environments.

Choose this version when manual nursery construction matters more than reorganizable workspaces, a generated multi-lesson Forge Lane, or the specialized brain/force chambers.

## Version Guide

| Version | Best for |
| --- | --- |
| [`xenospecies_swarm_hierarchical_force_chambers.html`](xenospecies_swarm_hierarchical_force_chambers.html) | Current default; full chamber workspace, force-matrix and brain inspection, editable/generated curricula, and automated discovery. |
| [`xenospecies_swarm_alien_nursery_forge_fixed.html`](xenospecies_swarm_alien_nursery_forge_fixed.html) | Consolidated evolutionary sandbox with a strong custom Nursery Forge editor. |
| [`xenospecies_swarm_auto_forge_editable_curriculum.html`](xenospecies_swarm_auto_forge_editable_curriculum.html) | Earlier editable hand curriculum plus generated Auto Forge Lane. |
| [`xenospecies_swarm_cognitive_matrix_lab.html`](xenospecies_swarm_cognitive_matrix_lab.html) | Expanded cognitive and force-matrix lab with detailed species analysis. |
| [`xenospecies_swarm_worldforge_generative_worlds.html`](xenospecies_swarm_worldforge_generative_worlds.html) | Procedural, seedable world-generation experiments. |
| [`xenospecies_swarm_biodiversity_lab.html`](xenospecies_swarm_biodiversity_lab.html) | Biodiversity, species survival, and selection-pressure experiments. |
| [`xenospecies_swarm_ecology_intelligence_lab.html`](xenospecies_swarm_ecology_intelligence_lab.html) | Ecology and neural-policy evolution foundation. |
| [`xenospecies_swarm_research_lab.html`](xenospecies_swarm_research_lab.html) | Earlier general-purpose swarm research interface. |
| [`xenospecies_swarm_chemistry_physics_lab.html`](xenospecies_swarm_chemistry_physics_lab.html) | Focused force-chemistry and particle-physics prototype. |
| [`xenocell_genesis_environments.html`](xenocell_genesis_environments.html) | Separate Xenocell environment experiment. |
| [`particle_audio_polygon_alien_cockpit_relinked.html`](particle_audio_polygon_alien_cockpit_relinked.html) | Particle simulation with audio-reactive beacons and an alternate cockpit UI. |

## Concepts

- **Species:** particle populations that carry neural-controller parameters, population share, and fitness history.
- **Force matrix:** per-species-pair attraction/repulsion radius and strength. It can remain fixed or evolve alongside species.
- **Arena:** an environment containing rewards, goals, hazards, walls, or moving fields that shapes fitness.
- **Curriculum:** an ordered sequence of arenas. It can be edited manually or generated from reproducible Forge settings.
- **Pheromone fields:** species-tagged trails which controllers can emit and sense.
- **Auto-Discovery:** a conservative tuning agent that monitors recent survival and progress, then adjusts pressure when the run stalls.

## Saving Experiments

Use the HUD save controls or the experiment controls in the relevant interface to copy JSON, download an experiment, import it later, or save it in browser storage. Exports preserve the experiment recipe and evolutionary state; particle positions are typically respawned when loaded.
