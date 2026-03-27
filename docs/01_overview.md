# Overview

This guide explains how to preprocess inputs for **SCHISM** without relying on SMS as the primary GUI workflow. The focus is on building a practical, reproducible, and script-friendly process that can be shared across projects and teams.

## What is SCHISM?

**SCHISM** (Semi-implicit Cross-scale Hydroscience Integrated System Model) is an unstructured-grid hydrodynamic model used for coastal, estuarine, and inland water simulations. It supports flexible meshes, multiple forcing types, and large-scale operational or research workflows.

## Why this repository exists

Many SCHISM users still depend on manual SMS-based setup steps. While SMS can be useful for visual editing, purely GUI-driven preprocessing often causes:

- low reproducibility,
- hard-to-track configuration changes,
- difficulty automating repeated runs,
- and onboarding friction for new team members.

This repository is designed to address those issues with documented, version-controlled preprocessing steps.

## Scope of this guide

The guide covers the practical preprocessing path from mesh and boundary setup to forcing and run-ready input packaging.

Typical scope includes:

1. Understanding SCHISM preprocessing concepts and required files.
2. Organizing grid, bathymetry, and boundary definitions.
3. Preparing forcing datasets (atmospheric, tides, rivers, etc.).
4. Validating consistency before model execution.
5. Producing reproducible run directories.

## Intended audience

This repository is for:

- SCHISM beginners moving from GUI workflows,
- analysts and engineers building repeatable project pipelines,
- and teams that need transparent, auditable model preparation.

## Workflow philosophy

The project follows four core principles:

- **Reproducible**: every preprocessing decision should be documented and version-controlled.
- **Automatable**: repetitive preparation steps should be scriptable.
- **Inspectable**: generated files should be easy to validate.
- **Portable**: workflows should be adaptable across environments and projects.

## Recommended project structure

A typical SCHISM project using this guide may look like:

```text
project/
  mesh/
  boundaries/
  forcing/
  templates/
  runs/
  scripts/
```

You can adapt naming conventions as needed, but keeping data and generated artifacts separated is strongly recommended.

## What comes next

After this overview, continue with the next chapters in order:

- Numerical core and assumptions
- Grid system and mesh handling
- Input file definitions
- Boundary condition setup
- Forcing preparation
- Run execution and output interpretation

These chapters will help you move from concept to an end-to-end preprocessing workflow.
