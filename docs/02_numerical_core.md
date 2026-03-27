# Numerical Core

The **Numerical Core** defines the foundational math and signal-processing primitives used by the Schism preprocessor. This document serves as the canonical reference for numerical behavior and implementation expectations.

## Goals

- Provide deterministic, reproducible numerical operations.
- Keep primitive operations composable and testable.
- Favor explicit behavior over implicit coercion.
- Define precision and stability expectations clearly.

## Scope

The Numerical Core includes:

1. Scalar arithmetic conventions.
2. Vector and matrix operation contracts.
3. Normalization and clipping rules.
4. Error tolerances for floating-point comparisons.
5. Shared constants used across preprocessing pipelines.

## Design Principles

### 1) Determinism

Given the same input and configuration, results should be identical across runs in the same execution environment.

### 2) Numerical Stability

Implementations should minimize catastrophic cancellation and avoid unstable transformations where possible.

### 3) Explicit Precision

All core operations should define expected precision behavior (for example, `float32` vs `float64`) and avoid silent downcasts.

### 4) Safe Defaults

Default operations should prioritize robustness and correctness over micro-optimizations.

## Core Conventions

- Use epsilon-based comparisons for floating-point equality checks.
- Clamp outputs where domain boundaries are required.
- Validate shape and dimensionality before vectorized operations.
- Document units and expected ranges for all public numerical interfaces.

## Future Extensions

- Add reference formulas for each primitive operation.
- Include benchmark baselines for stability/performance trade-offs.
- Define cross-platform reproducibility criteria.
- Add examples for edge-case handling and tolerance selection.
